

# Project description
NuFix is Visual Studio plugin, which helps .NET developers automatically repair Dependency Maze (DM) issues (i.e., conflicting constraints on package or target platform versions such as NU1107, NU1202, etc).

Its main features are: 1) building on top of a comprehensive study of developers’ preferences in fixing DM issues (e.g., installing fewer packages, inducing fewer risky build warnings); 2) seeking for the global optimal fixing solution based on a linear optimization model; 3) allowing developers to customize and iteratively refine the search scope of package versions based on their requirements; 4) visualizing dependency graph after adopting the derived fixes. A video demo is available at: https://youtu.be/8NECIM0wjhw 



Figure 1.  An overview of NuFix
# Background
With the rapid evolution of the .NET ecosystem, managing dependencies in .NET projects becomes a critical challenge. Due to the fragmentation of .NET ecosystem, developers often suffer from DM issues when updating a project’s platform or dependency versions. DM issues are serious, since they can block the package installations, causing build errors. 

Fixing a DM issue can be challenging. Multiple DM issues often occur in a project at the same time. For those projects with large dependency graphs, fixing such issues is a time-consuming and error-prone process that exercises a series of changes in dependency constraints in response to newly induced DM issues. More importantly, when deciding a fixing solution, developers often consider their desired properties of configuration (e.g., installing fewer packages, inducing fewer risky build warnings). However, it is difficult for developers to imagine all possible dependency graphs affected by dependency changes, to figure out an optimal solution that satisfies their preferences.
# Evaluation
Our evaluation shows that NuFix can generate fixes for a given .NET project within 12.5 seconds and achieves a 100% fixing ratio for 262 real DM issues. We invited ten experienced .NET experts working in a leading IT company (anonymize for review) to evaluate the quality our generated fixes. Their feedback indicates that the generated fixes meet the developers’ desired properties for the build management. Encouragingly, 20 projects (including affected projects such as Dropbox) have approved and merged our generated fixes, and shown great interests in our technique (the merged PRs are available on NuFix’s website, e.g., [PR#43 of MicroservicesBuffet](https://github.com/MicroservicesBuffet/Email/pull/31)).
