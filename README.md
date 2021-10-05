
# PEPDROID force field

A force field for peptoids by Hoyas et al.

Reference: https://onlinelibrary.wiley.com/doi/10.1002/adts.201800089

These force field parameters were developed based on the DREIDING force field by Mayo et al. (https://pubs.acs.org/doi/10.1021/j100389a010).
The basis force field and the reparametrization was carried out in Materials Studio 6.0 and 18.0 (same results).
The parameters were adapted for peptoids by mainly reparametrizing dihedrals (backbone dihedrals vs. side chain dihedrals) 
based on quantum mechanical calculations (MP2/cc-pVDZ).
The strategy was to decouple the backbone dihedrals from the side chain dihedrals. In this manner, any new side chain can be added.

Currently support: Nsar, Nspe, Nnpr, Npm, Nph, Ns1tbe, NtBu, Nscp, Nsce, Nazb

In this repository, the topology and parameters are currently available for (S)-1-phenylethyl side chain (Nspe) in the CHARMM format.

Notes:

a) DREIDING has an explicit term for hydrogen bonds that is not present in the NAMD software.
Hopefully, not many side chains can form hydrogen bonds.
Nonetheless, the N terminus extremity can still be involved in hydrogen bond. 
Therefore, the parameters were slightly adjusted at the N terminus to account for the lack of hydrogen bonds
and reproduce the correct dihedral potential compare to MP2/cc-pVDZ.

b) The equation for impropers is different between Materials Studio and NAMD (cosine term vs. harmonic term).
Therefore, the conversion of the parameters prevent to obtain a perfect match for impropers, but the difference is negligeable.
