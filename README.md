# Magnesium Force Fields for OPC Water with Accurate Solvation, Ion-Binding, and Water-Exchange Properties: Successful Transfer from SPC/E

[Link](https://github.com/bio-phys/Magnesium-FFs) to parameters in TIP3P.

[Link](https://github.com/bio-phys/optimizedMgFFs) to parameters in SPC/E, TIP3P-fb, TIP4P/2005, TIP4P-Ew, and TIP4P-D.


## Introduction

We have previously developed two sets for 6 different water models. Here we report the parameters for SPC/E water, that are transferable to OPC. The parameters shown here are exactly the same as the ones for SPC/E. 

We have developed two sets of force field parameters each for Magnesium Mg2+, `microMg` and `nanoMg`, for use in combination with the one of the above mentioned water model. Both optimized force field sets simultaneously reproduce thermodynamic and structural properties of aqueous solutions (hydration free energy, radius of the first hydration shell, and coordination number of the first hydration shell).

The parameter sets `microMg` furthermore reproduce the experimental water exchange rate on the microsecond timescale, while `nanoMg` yield water exchange up to the nanosecond timescale (10^7 exchanges per second)

Upon fine tuning of the Lorentz-Berthelot combination rules, additional thermodynamic and structural properties are reproduced (activity coefficient derivative, binding affinity, and distance towards the binding sites) for the interaction towards Chloride and RNA.

Our optimized parameters aim to precisely capture the role of Magnesium in all-atom molecular dynamics simulations of biological processes including ion specific binding and ion binding kinetics.

## Quick start guide

Our parameters are optimized for the SPC/E, TIP3P-fb, TIP4P/2005, TIP4P-Ew, or TIP4P-D water models. The parameters are optimized for use with the Smith-Dang parametes for Cl (SPC/E) or the Cloride parameters optimized alongside the Mg2+ parameters and `parmBSC0chiOL3` RNA force fields (e.g. `amber14sb.ff`). All parameter sets here are to be used with the Lorentz-Berthelot combination rule (otherwise modifications are required). Note that we have chosen unique names for the optimized parameters to avoid errors in overwriting atom names:

    `mMg` - MG with water exchange as in experiment
    `nMg` - MG with accellerated water exchange

To get started: Replace the standard ion names in your .gro file by our unique names. Modify the given topology file according to your system. The topology file includes the optimized force field parameters via

    `ff_Mg_opc.itp` and `Mg_opc.itp`,

# Examples

Examples can be used similar as for TIP3P water. To test the parameters for the selected water model (here spce as an example, works the same for the other parameters):

    download the example files from: [Link](https://github.com/bio-phys/Magnesium-FFs)
    add the new force field parameters (`ff_Mg_opc.itp` and `Mg_opc.itp`) to `ions.ff`
    change the names of the ions force field parameter file `.itp` in the topolology file `.top` from `ff_Mg.itp` to `ff_Mg_opc.itp` and from `Mg.itp` to `Mg_opc.itp` follow the description for TIP3P.

Citation

If you use our optimized parameters for Magnesium please refer to: K. K. Grotz, N. Schwierz (t.b.a.)

Implementation has been tested by Kara K. Grotz. USE AT YOUR OWN RISK!!
