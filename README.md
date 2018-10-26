# namd_profile_patch
Patch file for NAMD 2.12 source to modify production of lateral pressure profile

Hello!

As of 10/26/2018 I have not fully analyzed whether this patch fixes bugs or not.
Right now I prefer not to make claims one way or the other, but if you email me and ask I might have a better answer.
It produces the same profile as my previous implementation into CHARMM.

With my CHARMM implementation, increasing the z dimension by adding additional water did not significantly perturb the observable I was computing (first moment).
I believe I saw inconsistent results with NAMD.
I am 99% sure this is due to the constraint force contribution to the pressure profile and has nothing to do with the multibody terms which I also brought into alignment with my previous CHARMM terms.


To use this patch:

Copy prof.patch into the src directory of NAMD version 2.12. 

Move into that same src directory.

Apply the patch:

patch -p1 < prof.patch

then compile as per the NAMD docs.

If you have any questions or problems feel free to email
alexander.sodt@nih.gov 
or 
alexsodt@gmail.com
Because I am a human I cannot guarantee a timely reply.
