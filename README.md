# eclipseproblem
eclipseproblem

This is the source for the minimal example to reproduce the issue stated in stackoverflow question:

https://stackoverflow.com/questions/61962956/eclipse-m2e-plugin-issue-for-cyclic-dependent-projects

This minimal example demonstrates successfull import of two cyclic maven projects , projecta and projectb, in neon version. 

Steps to achieve successfull import path in neon:

1. Checkout initial commit 541f447. This initial version contains no cycles between projects projecta and projectb 
1. Run maven clean install in both projects
1. Set circular dependency buildpath problem preference to warning (java->Compiler->Building->Buildpath problems->Circular dependencies)
1. Checkout commit 791ec7f or latest version. The latest version has cycles between projects  bu can be imported successfully

![NeonSuccess](/attachments/neon_cyclicmavenprojectssuccess.png)

Execution of same steps fail in eclipse Version: 2020-03 (4.15.0) Build id: 20200313-1211

m2elogs are attached for both versions

Thanks in advance!

