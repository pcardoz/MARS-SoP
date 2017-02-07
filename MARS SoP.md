**MiSeq Library Prep SOP**
**MARS Facility**
Peter Cardoz
Dr. Kendra Maas
Version 1
Date: 2016-12-15


----------
#**Table of Contents** 
[TOC] 


----------
##**Workflow**


### **1.1.) Published Protocols**

 >The following methods and references are used in the workflows below.
	 - [MiSeq System User Guide](http://support.illumina.com/content/dam/illumina-support/documents/documentation/system_documentation/miseq/miseq-system-guide-15027617-01.pdf)
	 - [Preparing DNA Libraries for Sequencing on the MiSeq](http://support.illumina.com/content/dam/illumina-support/documents/documentation/system_documentation/miseq/miseq-denature-dilute-libraries-guide-15039740-01.pdf)
	 - [QIAgility User Manual](https://www.qiagen.com/us/resources/resourcedetail?id=6578e70d-9cfe-457e-be13-3b15556b41ca&lang=en)
	 - [QIAxcel Advanced User Manual](https://www.qiagen.com/us/resources/resourcedetail?id=e3edf734-1e5a-4ebf-957e-a35e120d6290&lang=en)
	 - [epMotion 5075 Operating Manual](https://www.eppendorf.com/US-en/service-support/knowledge-base/literature/manuals/?knowledgebase%5Bsort%5D=fileSize&knowledgebase%5Border%5D=descending&knowledgebase%5Bcontroller%5D=Assets&cHash=c51463e9b5f165456b98b563bc47786c#top)
	 - [MoBio PowerMag Soil DNA Isolation Kit](https://mobio.com/media/wysiwyg/pdfs/protocols/27100-4-EP.pdf)
	 - [OMEGA bio-tek Mag-Bind RXNPure Plus](http://omegabiotek.com/store/wp-content/uploads/2014/06/M1386-Mag-Bind-RXNPure-Plus-Combo-Online-1.pdf)
	 - [Nextera XT DNA Library Preparation Kit](http://support.illumina.com/content/dam/illumina-support/documents/documentation/chemistry_documentation/samplepreps_nextera/nextera-xt/nextera-xt-library-prep-guide-15031942-01.pdf)
	 - [Qubit dsDNA HS Assay Kit](https://tools.thermofisher.com/content/sfs/manuals/Qubit_dsDNA_HS_Assay_UG.pdf)
	 - [Quant-iT PicoGreen dsDNA Assay Kit](https://tools.thermofisher.com/content/sfs/manuals/mp07581.pdf)
	 - [BioTek Synergy HT User Manual](http://www.mbl.edu/jbpc/files/2014/05/Bio-Tek_Synergy_HT_User_Manual.pdf)


----------


### **1.2.) Initial Set up**
#### **1.2.1.) Dual Index Plates**

 2. Indexed primers shod be ordered to 200nM in a 96-well plate. See Appendix D for primer design.
 3. Using epMotion 5075 protocol **PrimerStocktoMaster** (*MARS/MARS COMMON*), array undiluted 200nM indexed primer plates into a BioRad 96-well semi-skirted plate using the scheme found in the Primers folder (*Z: MarsData/Primers*). Label each plate with primer arrangement, master plate, and date (v4.SASB 10μM Master Plate 2016-12-15, v4.SASC 10μM Master Plate 2016-12-15, etc). This 10μM Master Plate will allow you to make approximately 40 10μM working plates.
 4. Using epMotion 5075 protocol **PrimerAliquot** (*MARS/MARS COMMON*), aliquot 4.8μL of each forward and reverse indexed primers into the corresponding well of an Eppendorf 96-well full-skirted plate. This protocol will make 3 working plates. Label the plates using the label maker like so: v4.SASB 10μM Working Plate 2016-12-15
**NOTE**: These 10μM plates can be stored at -20°C and used for subsequent runs.

####**1.2.2.) 16S Sample intake and extraction:**

 5. Requestors must submit raw samples in 2mL barcoded tubes (supplied by MARS) and extracted DNA in 1mL barcoded tubes (supplied by MARS) or plates that will be barcoded by MARS (preferred). Investigators must submit a [Project](http://mars.uconn.edu/project-submission/) and [Sample](http://mars.uconn.edu/upload-sample/) submission form via [mars.uconn.edu](mars.uconn.edu) that identifies investigator PoC, lab name, sample name, sample ID (barcode on 1mL and 2mL tubes), and any other pertinent information (polymerase preferences, negative controls, etc.).
	 6. If submitting samples in a plate, MARS will assign a SampleID for each sample in the plate.
 6. Extraction plates will be barcoded (EID#####) using the TSC BarTender labeler. Racks containing raw environmental or fecal samples will also be barcoded (RS####) and their contents (well position and tube barcode) uploaded to the LIMS prior to transferring samples to the MoBio PowerMag Bead plate.
 7. The "Transfer Book" function within the LIMS (under Workflow) will show the wells of the MoBio bead plate, allowing you to scan the sample barcode and touch the sample's destination well.
 8. Extract template DNA following the MoBio PowerMag Soil DNA Isolation Kit protocol into 96-well format leaving one well for a negative control (95 samples max).
 9. Wipe down the surfaces of the epMotion and the tools with 100% ethanol. Follow the provided MoBio Extraction protocol, loading the worktable of the epMotion as outlined in the protocol **PowerMag_Extraction** (*MARS/MARS COMMON*). This protocol has several user intervention steps, as well as a tip replacement step, and takes approximately 3 hours to complete.

> For eDNA submissions, upload the samples to Workflow/Sample Plate Book in the LIMS after uploading the initial project submission and sample submission. After, move directly to section 1.4.) eDNA Quantification.

----------

### **1.3.) Extraction**
>A full extraction of 94 Samples + 1 Extraction blank + 1 empty well for PCR negatives will take ~4 hours to run on the epMotion. If samples are not preloaded into the bead plate, the extraction will approximately 6 hours to complete from start to finish.
>**When loading the plate, use no more than 0.25g of solid sample (or no more 250μL of liquid sample).**
>If your centrifuge doesn't achieve the desired speed, use this to calculate the appropriate time and speed necessary: $\frac{4500}{Max \ centrifuge \ speed} = Centrifugation \ time$

1. Before starting, wipe down the biosafety cabinet. Pull out 3x 100mL epMotion Reservoirs, 2x 30mL epMotion Reservoirs, the necessary amount of weighing funnels (~1 per sample), and 2x foil plate seals (1 for sealing prior to loading the plate and the other sliced into strips for covering up each row after loading samples) and place them in the hood to UV (15-30 minutes minimum). Once the reservoirs have been UV'd, fill the prerobot reservoirs with the correct volumes, making sure to label which reservoir contains what solution.
2. Go to the LIMS $\to$ Workflow $\to$ Transfer book, type in the extraction ID (EID#####) and click begin transfer. Scan each barcode and select the destination well. Pierce the well with a 1mL tip, place a funnel into the destination well (if necessary/desired), and transfer no more than 0.25g of sample into the well. At the end of each row, reseal the row with the sliced foil plate seals that were made earlier. Click confirm to save the destination well. Do this for the entire plate. For extraction blanks, you must manually type in the sample ID (e.g., EID17BlankA01).
3. Once the entire plate has been loaded and each row has been resealed, spin down the bead plate at 4500 RCF (or as close to 4500 RCF as possible) for 30s to 1 min. Remove the foil seals in the hood.
4. Add 750μL of the PowerMag Bead Solution to each well.
5. Add 60μL of the PowerMag Lysis Solution to each well. Secure the Square Well Mat (originally on the plate prior to loading) tightly to the Bead Plate. If this is not properly sealed, the plate WILL leak during the bead beating step.
6. Place the Bead plate within the bead beater (place the label facing forward), making sure to place a balance in the other arm. Shake at speed 20 for 10 minutes. After the first 10 minute cycle, rotate the block so that the label is facing the back of the shaker and shake again for 10 minutes on speed 20.
7. Centrifuge the Bead plate for 6 minutes at 4500 x g.
8. Carefully remove the Square Well Mat without splashing and transfer ~500μL of the supernatant to a clean 1mL Collection Plate.
9. Add 450μL of PowerMag IRT Solution to each well and apply sealing tape to the 1mL Collection Plate. Vortex the plate horizontally for 5s to ensure the plate is well mixed. Incubate at 4C for 10 minutes. Centrifuge the plate for 6 minutes at 4500 x g.
10. Carefully remove the sealing tape and transfer ~850μL of the supernatant to a new clean 1mL Collection Plate. Reseal the plate with sealing tape and centrifuge at 4500 x g for 6 minutes.
11. Transfer ~850μL of the supernatant to a clean 2mL Deep Well Plate, avoiding any residual pellet.
12. Fill the robot reservoirs with the necessary solutions and place them within the robot. Add the beads to the binding solution last, as the beads will separate from the binding solution within 3 minutes. Place the 2mL Deep Well Plate within the robot and begin the protocol.
13. There are 3 intervention steps that must be confirmed to continue the protocol.
14. Upon completion, seal the 96-well elution plate with a foil seal and label the plate with the extraction ID using the label maker.



|Solution|Volume of Solution (96 Samples)| Reservoir type | Manual (Prerobot) or Robot?| 
|:-----------------:|:----------------------------:|:------------------:|:-------:|
|Bead Solution| 75mL| 100mL Reservoir| Prerobot|
|Lysis Solution| 6mL| 30mL Reservoir| Prerobot|
|IRT Solution| 45mL| 100mL Reservoir| Prerobot|
|Wash Solution| 174mL| 400mL Reservoir| Robot|
|Elution Buffer| 11mL| 30mL Reservoir| Robot|
|Binding Solution| 85mL| 100mL Reservoir| Robot|
|Beads| 2mL| 100mL Reservoir (Add to binding solution)| Robot|



----------

### **1.4.) eDNA Quantification**


####**1.4.1.) DNA Dilution and eDNA quantification**

 1. All DNA submissions to MARS and DNA extractions will be quantified using the PicoGreen Protocol.
 2. Dilute DNA 1:200 with the epMotion protocol **1-200_DNAdilution** (*MARS/MARS COMMON*), using Molecular Biology Grade water.
 3. Prepare standards from the 100 μg/mL PicoGreen stock in concentrations of 2, 1, 0.5, 0.2, 0.1, 0.02, 0.01, and 0 ng/μL in 1XTE and aliquot 100μL from each concentration into an 8-well PCR strip (store unused aliquots in -20C until needed). 
 4. Make working solution by diluting PicoGreen reagent 1:200 with 1XTE in a 30mL reservoir. Total solution in reservoir: 75 μL x (8 standards + # samples) + extra). Keep protected from light by wrapping in foil and in drawer until prompted to add to worktable. 
 5. Populate epMotion worktable according to **pico384_2016Nov16** protocol (*MARS/MARS COMMON*). Be sure that the correct labware is loaded for the DNA plate (tubes, plate, etc.). This protocol adds 25μL picogreen working solution and 25μL 1:200 DNA or 25μL standard into each well in triplicate (50μL total volume) creating an assay plate from the 1:200 DNA for reading in the Synergy Plate reader. Run program.
 6. During incubation, create experiment on the Synergy Plate Reader by clicking New Task $\to$ Read Now $\to$ **picogreen_384.prt**. Be sure plate 1 shows the correct configuration and click Read New to begin.
 7. Create export of concentrations by choosing the plate wanted and the page with blue arrow icon at the top of the screen. Accept the defats chosen, and start the export. This will create an excel file with concentrations, as well as a graphical output of the standards. Save this file on USB and paste the values into **template.picogreen.2016Sep09** (*Z: MarsData/Synergy*) to calculate sample concentrations.
 8. Discard the 1:200 dilution plate. Create a 1:10 dilution plate if DNA concentrations are above 30ng/μL (or higher dilution if necessary).
 9. After creating the 1:10 dilution plate, upload the original plate ID, dilution plate ID, and dilution factor (eg. 1:10 dilution should be entered as 10) to the LIMS under Workflow/DNA Plate Dilutions.

>A working solution for a full plate of 96 samples + 8 standards requires 43μL picogreen reagent and 8507μL 1XTE.


 |Concentration|Volume of Standard | Volume of 1X TE |
| :-----------------: | :----------------------------: | :------------------:| 
| 2ng/μL|10 of **100μg/mL Stock**|490μL 1X TE|
|1ng/μL|10 of **100μg/mL Stock**|990μL 1X TE|
|0.5ng/μL|250 of **1ng/μL dilution**| 250μL 1X TE|
| 0.2ng/μL|100 of **1ng/μL dilution**|400μL 1X TE|
|0.1ng/μL|50 of **1ng/μL dilution**|450μL 1X TE|
|0.02ng/μL|10 of **1ng/μL dilution**|490μL 1X TE|
| 0.01ng/μL|5 of **1ng/μL dilution**| 495μL 1X TE|
|0ng/μL|0μL| 500μL 1X TE|


----------


### **1.5.) PCR**
>A full plate of 96 samples will take ~1 hour to prep using the epMotion.
>This section below will cover setup on the epMotion 5075. This PCR protocol and associated calcations are for triplicate reactions with GoTaq or Accuprime polymerases.

1. Using eDNA concentration found from the Synergy reader, calculate the amount of DNA needed per reaction to give 30 ng/μL. Do not use less than 1μL or more than 6μL of input DNA.
2. Calculate the amount of MBG water per sample by subtracting the volume of DNA from 6μL.
3. Use **EPmotion_PCR1DNA_Template.csv** and **EPmotion_PCR1H2O_Template.csv** (*Z:MarsData/EPmotion*) for the EpMotion for the addition of water and DNA . Save files as csv.
4.	On epMotion, load **2Plate_PCR_template** (*MARS/MARS COMMON*) program. Wipe down surfaces of the epMotion with 100% ethanol. Popate the worktable in the given arrangement. Keep covering closed when not loading worktable.
5.	For initial sample transfer, load the csv file coordinating to the water volume to be added for each reaction.
6.	For the second sample transfer, load the csv file coordinating to the DNA volume to be added for each reaction (Eppendorf full-skirted plates into DNA position, Biorad semi-skirted plates into DNA2 position). Be sure to check "change tips after each aspiration" when prompted. 
7.	Create master mix in a 30mL reservoir using the polymerase specific template below. Thoroughly mix contents and place in designated spot on the epMotion.
8.	Place the 10μM Working Primer plate onto the worktable and start the program. When prompted, remove the DNA plate seals, reseal completed plates, and after all samples have been added, centrifuge the Working Primer plate briefly using the plate spinner.
9.	Upon completion of the program, seal the 384 well plate using a ThermoFisher Adhesive PCR Plate Foil. Centrifuge the plate briefly and place in the thermocycler using the saved program, outlined below.
10.	Pool the PCR products to 96 well format on the epMotion using **PCR_384to96** (*MARS/MARS COMMON*). Load the worktable with the appropriate labware. This will pool triplicate reactions back into single wells.

####**1.5.1.) Common PCR Master Mixes**

> For 2-step reactions, bead clean the submitted PCR samples to use as input and reduce the reaction volume by half (to 25μL reactions).

   |PROMEGA GoTaq Master Mix (50μL Reaction)| Volume per sample |
| :-----------------: | :----------------------------: |
| GoTaq Buffer|10μL |
|GoTaq Polymerase |0.8μL |
|10mM dNTPs |1μL| 
| 50mM MgSO4 |0.1μL|
|BSA |2μL|
|0.1mM Non-Illumina Forward (515F) |0.1μL|
| 0.1mM Non-Illumina Reverse (806R) |0.1μL| 
|Master Mix Water | 21.1μL|
|**Total Master Mix**| **35.2μL**|

   |Accuprime PFX Master Mix (50μL Reaction)| Volume per sample |
| :-----------------: | :----------------------------: |
| Accuprime PFX Reaction Mix|5μL |
|Accuprime PFX Polymerase |0.5μL | 
| 50mM MgSO4 |0.1μL|
|0.1mM Non-Illumina Forward (515F) |0.1μL|
| 0.1mM Non-Illumina Reverse (806R) |0.1μL| 
|Master Mix Water | 34.4μL|
|**Total Master Mix**| **40.2μL**|

   |Accuprime PFX Supermix Master Mix (48.2μL - 53.2μL Reaction)| Volume per sample |
| :-----------------: | :----------------------------: |
| Accuprime PFX SuperMix|45μL |
|BSA |2μL | 
|0.1mM Non-Illumina Forward (515F) |0.1μL|
| 0.1mM Non-Illumina Reverse (806R) |0.1μL| 
|**Total Master Mix**| **47.2μL**|


####**1.5.2.) Thermocycler Conditions**

**2-step Accuprime**
| Step | Temp | Time (mm:ss) | 
| :- | :-: | :-: |
| Initial Denaturation| 95&deg;C | 02:00 |
| 8 Cycles | 95&deg;C | 00:15 |
| | 55&deg;C | 00:30 |
| | 68&deg;C | 01:00 |
|Final Extension | 68&deg;C | 05:00 |
| Hold | 4&deg;C | $\infty$ |
 

**2-step GoTaq**
| Step | Temp | Time (mm:ss) | 
| :- | :-: | :-: |
| Initial Denaturation| 95&deg;C | 02:00 |
| 8 Cycles | 95&deg;C | 00:30 |
| | 55&deg;C | 00:30 |
| | 72&deg;C | 01:00 |
|Final Extension | 72&deg;C | 05:00 |
| Hold | 4&deg;C | $\infty$ |


**v4/ITS Accuprime**
| Step | Temp | Time (mm:ss) | 
| :- | :-: | :-: |
| Initial Denaturation| 95&deg;C | 02:00 |
| 30 Cycles | 95&deg;C | 00:15 |
| | 55&deg;C | 01:00 |
| | 68&deg;C | 01:00 |
|Final Extension | 68&deg;C | 05:00 |
| Hold | 4&deg;C | $\infty$ |



**v4 Accuprime Supermix**
| Step | Temp | Time (mm:ss) | 
| :- | :-: | :-: |
| Initial Denaturation| 95&deg;C | 05:00 |
| 30 Cycles | 95&deg;C | 00:15 |
| | 55&deg;C | 01:00 |
| | 68&deg;C | 01:00 |
|Final Extension | 68&deg;C | 05:00 |
| Hold | 4&deg;C | $\infty$ |



**v4/ITS GoTaq**
| Step | Temp | Time (mm:ss) | 
| :- | :-: | :-: |
| Initial Denaturation| 95&deg;C | 02:00 |
| 30 Cycles | 95&deg;C | 00:30 |
| | 55&deg;C | 01:00 |
| | 72&deg;C | 01:00 |
|Final Extension | 72&deg;C | 05:00 |
| Hold | 4&deg;C | $\infty$ |



**v4 Phusion**
| Step | Temp | Time (mm:ss) | 
| :- | :-: | :-: |
| Initial Denaturation| 94&deg;C | 03:00 |
| 30 Cycles | 94&deg;C | 00:45 |
| | 50&deg;C | 01:00 |
| | 72&deg;C | 01:30 |
|Final Extension | 72&deg;C | 10:00 |
| Hold | 4&deg;C | $\infty$ |

 





----------


### **1.6.) PCR Quantification**

>A full plate will take approximately 30 minutes to run on the QIAxcel. Samples must be arranged in rows prior to running.

 1. All samples are run on the QIAxcel to check for PCR products.
 2. If a PCR has less than 96 samples, it must be configured into **ROWS** as each run on the QIAxcel is a row.
 3. Dilute 2μL of PCR product into 10μL of QX DNA Dilution Buffer. Every row that is run on the QIAxcel must have the buffer in each of the wells in that row, even if there is no sample in that well.

####**1.6.1.) QIAxcel Quantification:**

>For initial cartridge setup and buffer tray set up, please refer to the QIAxcel Advanced User Manual.

1.  Ensure that the cartridge, alignment marker, and size marker are at room temperature prior to running samples. 
2. Load the cartridge (generally Fast Analysis) into the machine. If there isn't already an alignment marker strip, prepare and load the alignment marker strip (15μL alignment marker per well, with a drop of mineral oil on top) into the Marker 1 position of the buffer tray.
3. If there isn't a recent Size Marker Table saved (the QIAxcel will have a green circle next to the saved Size Marker Table if it is recent), load 10μL of Size Marker (50bp - 1.5kb) into an empty well on your plate. If you are running a full plate, load a 12-tube strip containing 10μL of water or buffer in 11 tubes and 10μL  of size marker in the last tube. Save this size marker for use as a future Size Marker Table.
	1. In the Analysis tab at the top, choose the experiment just run (usually at the bottom on the left side) and the lane in which the size marker was run. Click the reference marker tab at the top of the gel image. Check to make sure the number of bands in the size marker chosen matches the manufacturer number. Choose the Save As button and name the size marker table (Ex. 2016Dec15_FAMarker).
4. Run samples under Defat Fast Analysis v2.0, with V4 Peak Calling Instruction. This will create a log of peaks and concentration that fall within 15% of 400 bp to transfer back to LIMS. Choose "saved reference marker table" if you previously ran and saved a size marker. If you loaded a size marker onto the QIAxcel dilution plate, choose "run marker side by side".
5. Select the rows with samples and identify the size marker by using the right mouse button (if loaded onto the plate). Check and pre-run warnings or checks, and hit "run".
6. Upon completion, export peak calling table from *Computer/localdisk/programdata/Qiagen/QiaxcelScreenGel/Data/Export*.
7. Record PCR concentrations on the sample summary sheet and upload to the LIMS.


----------


### **1.7.) Normalization, Pooling, and Cleanup**

####**1.7.1.) epMotion Normalization**
1. Calculate the volume required per sample to pool 10ng of PCR product. Pooling is done to the samples with concentrations >0.5ng/μL AND to all negative controls (use the same volume as required for the lowest concentration sample, but do NOT exceed 10μL). 
2. After calculating the required volumes to get 10ng per sample, paste the volumes and PCR well positions into the **EPmotion_PCR_Normalization_Template.csv** (*Z:MARSData/EPmotion*) and put this file on a USB. 
3. On the epMotion, open **PostPCR_Pooling** (*MARS/MARS COMMON*) and import the previously saved csv into the sample transfer step, making sure to choose pipette samples individually.
4. Populate the workdeck with the appropriate labware and run the protocol.
5. Using the LIMS, download the pooling template (*Reports/Templates tab*). Make sure to add the PCR negative to this sheet as the LIMS will not add it. 
6. Type in the sequencing run ID (label as Run Date, Flowcell ID, Sequencing ID; ex. 20161215AV688SID16020). For samples that were not pooled, type "yes" under the exclude column. Upload this sheet to the LIMS for Sample Sheet creation.

####**1.7.2.) PCR Clean Up** 

>Prior to cleaning the samples, you MUST allow the OMEGA bio-tek Mag-Bind RXNPure Plus beads to reach room temperature. Failure to do so will not clean your samples properly and may cause the sequencing run to fail. Wait times will vary depending on how weak or strong your magnet is. If you find that the beads aren't separating properly, increase the separation time accordingly.

1. Clean pooled PCR products using the OMEGA bio-tek Mag-Bind RXNPure Plus to remove DNA fragments <150bp from PCR products.
2. Using a Biorad semiskirted plate (or a 0.5mL tube strip), add 50μL of the pooled PCR product to 40μL of beads (1:0.8 ratio), pipette a few times to mix, and incubate at room temperature for 5 minutes.
	3. Amplicon pools can be cleaned with less than 50μL, but do not go below a total reaction volume of 20μL (12μL of sample).
3. Place the plate on a magnet for 3 minutes, and once the beads separate, discard the supernatant.
4. Without removing the plate from the magnet, wash with 200μL 70% ethanol, incubate for 1 minute, and then discard the supernatant. Do not resuspend the beads during this step. Repeat this for a total of 2 washes.
5. Using a p-20, remove excess ethanol. Allow the sample to air dry for 5 minutes and then remove the plate from the magnet.
6. Add 25μL of water and resuspend the beads by pipetting. Incubate at room temperature for 3 minutes.
7. Place the plate on the magnet for 3 minutes and then transfer the supernatant. This is the cleaned PCR product.
8. Run on the QIAxcel to check if the <150bp fragments were removed (optional).

####**1.7.3.) Quantification of Cleaned PCR Pools**
1. Quantify cleaned library using the Qubit. Prepare working solution for n+2 tubes, 200μL buffer: 1μL dye. Generally, you will need to quantify each sample at least twice.
2. Prepare standards 1 and 2 by using two Qubit assay tubes with 10μL of standard 1 or 2 and 190μL of working solution. Incubate at room temperature, in the dark for 3 minutes.
3. Prepare samples and 1.5ng standard (user prepared) by using Qubit assay tubes with 2μL of sample and 198μL of working solution. Incubate at room temperature, in the dark, for 3 minutes.
4. Read standards, then samples, and calculate concentrations on the Qubit by selecting the sample volume used (2μL).
5. Libraries should be adjusted to 4nM (1.5ng/μL for MARS' V4 primers) with Molecular Biology Grade water. If samples are amplified using non-MARS' V4 primers, calculate the ng/μL required by using the formula below.

>Calcating ng/μL required to get to 4nM:
>$$
		(\frac{μg}{μL}) DNA * (\frac{1 \ pmol}{660 \ pg}) * (\frac{10^6 \ pg} {1 \ μg}) * (\frac {1}{N}) = \frac {pmol}{μL} \ DNA
		$$
		$$
		0.004 \  \frac {pmol}{μL}  = 4 \ nM 
		$$
		$$
		\frac {ng}{μL} \ DNA = (\frac {0.004 \ pmol}{μL} \ DNA) * (\frac {660 \ pg}{pmol}) * (\frac {1 \ μg}{10^6 \ pg}) * (\frac {1 \ ng}{10^6 \ μg}) * N
		$$
		Where N is the number of nucleotides (bp) and $\frac {660pg}{pmol}$ is the average molecular weight of a nucleotide pair.
		**NOTE: Illumina suggests to dilute samples down to 4nM, however we have noticed that this concentration leads to an underclustered run. If you experience the same issues, dilute the samples down to 6nM rather than 4nM.**
> Common sample concentrations:
> |Sample Type| Concentration|
> |--|--|
> |V4 Amplicons (16S)| 1.5ng/μL|
> |V9 Amplicons (18S)| 1.0ng/μL|
> |V2 Amplicons| x ng/μL|
> |V3 Amplicons| x ng/μL|
> |Genomes| 1.5ng/μL|
		
	

----------


### **1.8.) Genome quantification, preparation, and cleanup**

#### **1.8.1.) Nextera XT Sample Preparation**

> For this protocol, multiple reagents must be pulled out of the freezer ahead of time. 
> Tagment Reagents: **ATM** & **TD** reagents must be thawed on ice. Pull these reagents out before starting the reactions.
> Amplification Reagents: **Indices** must be thawed at room temperature. **NPM** reagent must be thawed on ice. Pull these reagents out after placing the samples in the thermocycler for the tagmentation step.
> We reduce the reaction volumes for all steps by half to reduce the cost per sample.

1. Samples submitted for small genome sequencing shod be quantified using the Qubit protocol and use the Nextera XT Kit for preparation and clean up.
2. Qubit quantify submitted DNA and dilute to 0.2 ng/μL (concentrations between 0.17ng/μL and 0.3ng/μL are acceptable).
3. Use 2.5μL of the ~0.2ng/μL dilution to enter into the Nextera XT preparation. Reactions can be completed in 0.5mL PCR tubes, strips, or a 96 well semi skirted plate, depending on the number of genomes to be prepared.
4.  Add 5μL of TD to each sample and pipette to mix.
5. Add 2.5μL of ATM to each sample and pipette to mix.
6. Place the plate in Thermocycler **CT019662**. Use protocol **NEXTERA_TAG** found in the <*Root*> folder.
7. Upon completion, **IMMEDIATELY** remove the plate from the thermocycler.
8. Add 2.5μL of NT and pipette to mix. Quickly centrifuge the plate and incubate at room temperature for 5 minutes.
9. Add 7.5μL NPM to each sample.
10. Add 2.5μL of the Forward Primer and 2.5μL of the Reverse Primer and pipette to mix. Centrifuge briefly.
11. Place the plate in Thermocycler **CT019662**. Use protocol **NEXTERA_PCR** found in the <*Root*> folder.
	12. You may stop at this point.
	13. Do not proceed with library normalization or sequencing protocol as written in the Nextera Protocol. 
6. PCR clean-up and size select amplified tagments as outlined above. Use the OMEGA bio-tek Mag-Bind RXNPure Plus found in the 4C fridge. Use the Alpaqua Magnum FLX magnet to clear the supernatant. 
8. Genomes shod be brought to 4nM (1.5ng/μL) for sequencing using the Qubit.


----------


### **1.9.) Sequencing **

1. Remove a 500 cycle reagent cartridge from the -20C freezer. Place in room temperature water bath for 1 hour. Place HT1 buffer tube in 4C fridge. While reagent cartridge is thawing, create the Sequencing Run csv by going to the LIMS Workflow and select Sequences. Fill in the required fields (Run Date, Sequence Run ID, Flowcell ID, and Reagent Cartridge) and click submit. Next go to Reports/Templates and select Sample Sheet. Find and select your Sequencing Run ID and select the correct flow cell (if the Sequencing Run was named correctly, the flowcell ID shod match with the 5 middle alphanumeric values). Open this file and CAREFULLY make sure that there are **NO SPACES, PERIODS, DASHES, OR UNDERSCORES** and that all samples have **UNIQUE SAMPLE NAMES AND SAMPLE IDS**. Forgetting to do so will cause issues for the MiSeq during the Indexing QC. Once you are sure that the sample sheet is correct, save this file to **Z:MarsData/SeqSampleSheet**.
2. Prepare fresh 0.1N NaOH by diluting the provided 0.2N NaOH aliquots with 475μL of nuclease free H2O and vortex.
3. Denature and dilute 16S library and any other libraries. All similar samples - 16S, genomes, etc - shod be combined according to the number of samples in each single library (i.e. if a library has 37 samples, 37μL should be added to the 4nM pooled libraries tube). Keep these libraries separate until the final loading of the reagent cartridge.
	4. Mix 5μL of 4nM library with 5μL of NaOH, vortex, and spin down. Incubate at RT for 5 minutes.
	5. Add 990μL HT1 and vortex. This library is now at 20pM and is good for three weeks if stored at -20C.
4. Adjust and denature PhiX.
	5. Mix 2μL 10nM PhiX (aliquot) and 3μL of Tris-Tween (10mM Tris-Cl pH8.5 with 0.1% Tween 20).
	6. Vortex and spin down.
	7. Mix 5μL of 4nM PhiX with 5μL of 0.1N NaOH, vortex, and spin down. Incubate at RT for 5 minutes.
	8. Add 990μL HT1 and vortex. The PhiX is now diluted to 20pM and is good for ~3 weeks if stored at -20C.
5. Adjust amplicon library to 6pM by combining 300μL of the 20pM amplicon library with 700μL of HT1. Adjust the genome library to 8pM by combining 400μL of the 20pM genome library with 600μL of HT1. Adjust PhiX to 8pM by combining 400μL of 20pM PhiX with 600μL of HT1.
6. In a strictly 16S sequencing run, we use 30% PhiX per run. Add 300μL of PhiX to a tube containing 700μL of 16S library, vortex, and chill on ice until ready to load into reagent cartridge. This proportion of PhiX changes with diversity of samples or the inclusion of genomes. A minimum of 1% PhiX shod always be run during sequencing. A full genome run is up to 12 genomes. Final sequencing library shod be in desired ratio to a total volume of 1mL.
7. When the reagent cartridge has thawed, dry bottom with a paper towel. Carefly invert the cartridge repeatedly to check each well is thawed, making sure to create as little bubbles as possible. This also serves to mix the reagents. Place in fridge until ready to load.
8. Using a clean 1000μL pipette tip in each, pierce the foil covering wells 12, 13, 14, and 17 of the reagent cartridge, leaving the tip in place.
9. Transfer 3.4μL of Read 1 Sequencing Primer to the bottom of well 12 and pipette to mix. Repeat this process spiking the Index Primer into well 13 and the Read 2 Sequencing Primer into well 14.
10. Pipette 600μL of final library (containing PhiX) into well 17. Place cartridge in fridge until ready to load into MiSeq.
11. Unbox flowcell and PR2 bottle.
12. Thoroughly rinse the flow cell with DI water. Carefully dry by blotting with Kim wipes. Give special attention to the edges and points of intersection between the glass and plastic.
13. Using an alcohol wipe, clean the glass on both sides avoiding the rubber intake ports. Completely dry the flowcell with lens paper.
14. Visually inspect the flow cell to ensure there are no blemishes, particles, or fibers on the glass.
15. Transfer reagent cartridge, flow cell, PR2 bottle to MiSeq. Once the reagent cartridge is read, select the correct Sample Sheet from *Z:/MarsData/SeqSampleSheet*. Empty and replace the waste bottle.
16. Ensure the machine recognizes the correct sample sheet and the run parameters are correct (specifically the read number).
17. Wait for the MiSeq to perform its pre-run checks and press start. The pre-run checks can take anywhere from 5 minutes to 15 minutes, so make sure you press start before walking away from the MiSeq.


----------

### **1.10.) Run Monitoring**

1. The run shod be monitored periodically using Illumina Sequence Analysis Viewer.
2. Ideal parameters for a 70% 16S run:
	3. Cluster density 700-800k/mm2 for v2 kits, however acceptable rests can be had with above 600k/mm2 cluster density.
	4. Above 80% clusters passing filter
	5. 30% aligned (or percent of total run of PhiX)
	6. Final >Q30 score of above 80%


----------


### **1.11.) Washes and Data Transfer**

1. Perform a post run was on the MiSeq.
2. Dispose of liquid waste in appropriate hazardous jug and reagent cartridge in hazardous bucket. Leave flow cell in place until next sequencing run.
3. When MiSeq Reporter finishes, copy the files from the output folder on **insert computer name and folder here** to *Z:/MarsData/SequenceResults*
	4. To calculate the number of reads per sample, open up the Demultiplexing file that was copied over to *SequenceResults*.
	5. Insert a row below the sample names (Row 2).
	6. Take the average of the values below the sample name. These are the decimal values that are in the same rows as "s_1_1101" to "s_1_2114".
	7. Multiply this average with PF Reads (found under Run Details $\to$ Indexing QC) and then divide this by 100.
	8. This will give you the total number of reads for each sample.
	9. Ex. For the first sample (found in cell C2), $ Total \ Reads \ (into \ cell \ C3) = \frac {AVERAGE(C4:C31)* PF \ Reads}  {100} $
	10. Copy and paste the values back into the cells after the calculation is complete. 
	11. Download the Sequence Results csv from the LIMS. Copy both the Sample Names and Values from the Demultiplexing calculation and transpose them into the csv you just downloaded. 
	12. Fill in the Sequencing Run ID into the first column of the Sequence Results csv and upload that file to the LIMS.
4. Demtiplex the run by opening MiSeq Reporter in the web browser (in bookmarks). Find the desired file and start process.
5. **Is this still accurate? On the iMac, copy the Undetermine R1, I, and R2 files from Shared/All/Workgrou/miseq_analyis/MiSeq/(run-specific-folder)/Data/intensities/basecalls to DataRaid/Demtiplexing Sandbox. **
6. Perform maintenance or standby wash if required.
7. Continue into desired Qiime or Mother analysis pipeline as desired.

> Copy all sequenced blanks to their appropriate projects (RIDBlanks should go in every project folder that was on that PCR, EIDBlanks should go in every project folder that was on that extraction, etc).
> Share BaseSpace projects with the requester using the how-to template email.
> Generate Sample History report to email requestors.

----------
##**Appendices**

###**Appendix A: Primer Design**
Generic V4 Amplicon:

>AATGATACGGCGACCACCGAGATCTACAC < i5 >< pad >< link >< 16Sf > 

>CAAGCAGAAGACGGCATACGAGAT < i7 >< pad >< link >< 16Sr > 

>Generic read 1 primer design
< pad >< link >< 16Sf > VX.read1

>Generic read 2 primer design
< pad >< link >< 16Sr > VX.read2

>Generic index read primer design
Reverse complement of (< pad >< link >< 16Sr >) VX.p7_index

>The listed sequences in the generic design, above, are the adapter sequences to allow annealing of the amplicons to the flow cell. 
	The < i5 > and < i7 > sequences are the 8-nt index sequences.  
	The < pad > is a 10-nt sequence to boost the sequencing primer melting temperatures and is coordinated with each index.  
	The < link > is a 2-nt sequence that is anti-complementary to the known sequences.  
	The < 16Sf > and < 16Sr > are the gene specific primer sequences.  
	Primers are purchased from Invitrogen with desalted purification and in the smallest scale possible. They are brought to 100μM for storage at -20C, and aliquoted into 10μM for reactions. 

16Sf
V4: GTGCCAGCMGCCGCGGTAA

16Sr
V4: GGACTACHVGGGTWTCTAAT

Link:
V4f: GT
V4r: CC

Pad:
Forward: TATGGTAATT
Reverse: AGTCAGTCAG

####**i5 Primers**
|Primer Name|Sequence|
| ------ | ----- |
|2step_F01|TAGATCGC|
|2step_F02|CTCTCTAT|
|2step_F03|TATCCTCT|
|2step_F04|AGAGTAGA|
|2step_F05|GTAAGGAG|
|2step_F06|ACTGCATA|
|2step_F07|AAGGAGTA|
|2step_F08|CTAAGCCT|
|cil.v2.501|ATCGTACG|
|cil.v2.502|ACTATCTG|
|cil.v2.503|TAGCGAGT|
|cil.v2.504|CTGCGTGT|
|cil.v2.505|TCATCGAG|
|cil.v2.506|CGTGAGTG|
|cil.v2.507|GGATATCT|
|cil.v2.508|GACACCGT|
|cil.v2.509|CTACTATA|
|cil.v2.510|CGTTACTA|
|cil.v2.511|AGAGTCAC|
|cil.v2.512|TACGAGAC|
|cil.v3.501|ATCGTACG|
|cil.v3.502|ACTATCTG|
|cil.v3.503|TAGCGAGT|
|cil.v3.504|CTGCGTGT|
|cil.v3.505|TCATCGAG|
|cil.v3.506|CGTGAGTG|
|cil.v3.507|GGATATCT|
|cil.v3.508|GACACCGT|
|fung.its2.501|ATCGTACG|
|fung.its2.502|ACTATCTG|
|fung.its2.503|TAGCGAGT|
|fung.its2.504|CTGCGTGT|
|fung.its2.505|TCATCGAG|
|fung.its2.506|CGTGAGTG|
|fung.its2.507|GGATATCT|
|fung.its2.508|GACACCGT|
|v4.SA501|ATCGTACG|
|v4.SA502|ACTATCTG|
|v4.SA503|TAGCGAGT|
|v4.SA504|CTGCGTGT|
|v4.SA505|TCATCGAG|
|v4.SA506|CGTGAGTG|
|v4.SA507|GGATATCT|
|v4.SA508|GACACCGT|
|v4.SB501|CTACTATA|
|v4.SB502|CGTTACTA|
|v4.SB503|AGAGTCAC|
|v4.SB504|TACGAGAC|
|v4.SB505|ACGTCTCG|
|v4.SB506|TCGACGAG|
|v4.SB507|GATCGTGT|
|v4.SB508|GTCAGATA|
|v4.SC501|ACGACGTG|
|v4.SC502|ATATACAC|
|v4.SC503|CGTCGCTA|
|v4.SC504|CTAGAGCT|
|v4.SC505|GCTCTAGT|
|v4.SC506|GACACTGA|
|v4.SC507|TGCGTACG|
|v4.SC508|TAGTGTAG|
|v4.SC701|CAGTAGGT|
|v4.SC702|ATAGCGCT|
|v4.SC703|TCTAGACT|
|v4.SC704|TCCTCATG|
|v4.SC705|CGAGCTAG|
|v4.SC706|CTCTAGAG|
|v4.SC707|ATGAGCTC|
|v4.SC708|AGCATACC|
|v4.SC709|CGTCATAC|
|v4.SC710|TCAGTCTA|
|v4.SC711|CATCGTGA|
|v4.SC712|GAGCTCGA|
|v4.SD501|AAGCAGCA|
|v4.SD502|ACGCGTGA|
|v4.SD503|CGATCTAC|
|v4.SD504|TGCGTCAC|
|v4.SD505|GTCTAGTG|
|v4.SD506|CTAGTATG|
|v4.SD507|GATAGCGT|
|v4.SD508|TCTACACT|

####**i7 Primers**
(for use in the SEQMET file. When ordering, shod be reverse complement.)
|Primer Name|Sequence|
| ------ | ----- |
|2step_R01|	TGACCAAT|
|2step_R02|	CATTTTTA|
|2step_R03|	ACAGTGAT|
|2step_R04|	GTGAAATA|
|2step_R05|	GCCAATAT|
|2step_R06|	CTTGTATA|
|2step_R07|	CAGATCAT|
|2step_R08|	GTAGAGTA|
|2step_R09|	TAGCTTAT|
|2step_R10|	CTATACTA|
|2step_R11|	CTTGTAAT|
|2step_R12|	GCCAATTA|
|cil.v2.701|	CGAGAGTT|
|cil.v2.702|	GACATAGT|
|cil.v2.703|	ACGCTACT|
|cil.v2.704|	ACTCACTG|
|cil.v2.705|	TGAGTACG|
|cil.v2.706|	CTGCGTAG|
|cil.v2.707|	TAGTCTCC|
|cil.v2.708|	CGAGCGAC|
|cil.v2.709|	ACTACGAC|
|cil.v2.710|	GTCTGCTA|
|cil.v2.711|	GTCTATGA|
|cil.v2.712|	TATAGCGA|
|cil.v3.701|	CGAGAGTT|
|cil.v3.702|	GACATAGT|
|cil.v3.703|	ACGCTACT|
|cil.v3.704|	ACTCACTG|
|cil.v3.705|	TGAGTACG|
|cil.v3.706|	CTGCGTAG|
|cil.v3.707|	TAGTCTCC|
|cil.v3.708|	CGAGCGAC|
|cil.v3.709|	ACTACGAC|
|cil.v3.710|	GTCTGCTA|
|cil.v3.711|	GTCTATGA|
|cil.v3.712|	TATAGCGA|
|fung.its2.701|	CGAGAGTT|
|fung.its2.702|	GACATAGT|
|fung.its2.703|	ACGCTACT|
|fung.its2.704|	ACTCACTG|
|fung.its2.705|	TGAGTACG|
|fung.its2.706|	CTGCGTAG|
|fung.its2.707|	TAGTCTCC|
|fung.its2.708|	CGAGCGAC|
|fung.its2.709|	ACTACGAC|
|fung.its2.710|	GTCTGCTA|
|fung.its2.711|	GTCTATGA|
|fung.its2.712|	TATAGCGA|
|v4.SB701|	CTCGACTT|
|v4.SB702|	CGAAGTAT|
|v4.SB703|	TAGCAGCT|
|v4.SB704|	TCTCTATG|
|v4.SB705|	GATCTACG|
|v4.SB706|	GTAACGAG|
|v4.SB707|	ACGTGCGC|
|v4.SB708|	ATAGTACC|
|v4.SB709|	GCGTATAC|
|v4.SB710|	TGCTCGTA|
|v4.SB711|	AACGCTGA|
|v4.SB712|	CGTAGCGA|
|v4.SC701|	CAGTAGGT|
|v4.SC702|	ATAGCGCT|
|v4.SC703|	TCTAGACT|
|v4.SC704|	TCCTCATG|
|v4.SC705|	CGAGCTAG|
|v4.SC706|	CTCTAGAG|
|v4.SC707|	ATGAGCTC|
|v4.SC708|	AGCATACC|
|v4.SC709|	CGTCATAC|
|v4.SC710|	TCAGTCTA|
|v4.SC711|	CATCGTGA|
|v4.SC712|	GAGCTCGA|
|v4.SD501|	AAGCAGCA|
|v4.SD502|	ACGCGTGA|
|v4.SD503|	CGATCTAC|
|v4.SD504|	TGCGTCAC|
|v4.SD505|	GTCTAGTG|
|v4.SD506|	CTAGTATG|
|v4.SD507|	GATAGCGT|
|v4.SD508|	TCTACACT|
|v4.SD701|	TACTAGGT|
|v4.SD702|	ACGTACGT|
|v4.SD703|	CGCGATAT|
|v4.SD704|	CTATCGTG|
|v4.SD705|	GCGATACG|
|v4.SD706|	AGTCGCAG|
|v4.SD707|	GTTACAGC|
|v4.SD708|	TAACGTCC|
|v4.SD709|	CTACGACC|
|v4.SD710|	GAGACTTA|
|v4.SD711|	ACTGTGTA|
|v4.SD712|	TGCGTCAA|

|Primer Name|Sequence|
| ------ | ----- |
|806rcbc0| ACAAGGGA|
|806rcbc1 |AGTCTCGT|
|806rcbc3| CTGGTCGAT|
|806rcbc5| TGTGCGAT|	
|806rcbc8| CAAAGGAT|
|806rcbc9| GCGCTGTA|
|806rcbc15| TGGTATTC|
|806rcbc21 |ATGAGCTG|
|806rcbc30 |GTCAATCT|
|806rcbc33 |GGGAGTTG|
|806rcbc34 |TAACGCAA|
|806rcbc40 |AAGTGTTC|
|806rcbc43 |AGCGCCTT|
|806rcbc44 |CCGTATTA|
|806rcbc53| CTCATCAT|
|806rcbc56| GAGGGATG|
|806rcbc57| GCGGTATA|
|806rcbc64| GGTAGAGA|
|806rcbc66| TAGGTGAG|
|806rcbc69| TGTCGATA|
|806rcbc71| CAATTACG|
|806rcbc72| TAGTCACC|
|806rcbc76| GGCAGAAT|
|806rcbc78| TATCGTAC|
|806rcbc81| TCAGCGCA|
|806rcbc85| TAGAACGC|
|806rcbc86| AGAACAAC|
|806rcbc87| GGAAGTCC|
|806rcbc89| AATAGCAG|
|806rcbc93| CTACTCCA|
|806rcbc102| TCCGTGAC|
|806rcbc104| CGGTAGAT|
|806rcbc106| CTCCAAGA|
|806rcbc108| AGGTGTGC|
|806rcbc110| GAGCATGA|
|806rcbc111| TGACAGCT|
|806rcbc124| TTCGCAGG|
|806rcbc125| CGAGAGAA|
|806rcbc127| AGCTTAAC|
|806rcbc129| ACAATGTC|
|806rcbc130| TTGTTGGC|
|806rcbc132| CTCGAGGA|
|806rcbc133| GCTTGGGT|
|806rcbc137| CATTTCTG|
|806rcbc140| AAATAACC|
|806rcbc142| TGCTATGC|
|806rcbc145| AGGGTTCA|
|806rcbc148| CAGCATCG|


----------


###**Appendix B: epMotion 5075 Labware**

|Labware file name|Labware| Labware catalog number|
| :------: | :-----: | :---: |
| tip50f | 50ul epMotion filter tips| 0030014430|
| tip300f | 300ul epMotion filter tips| 0030014472|
| tip1000f | 1000ul epMotion filter tips| 0030014510|
| Rack_noTC_1_5ml | 1.5mL Tube Rack| 5075751275|
| Th_Adap_96 | Thermorack for 96-well PCR plates| 5075787008|
| ALP_MagFLX_96_1 | Magnum FLX magnet for full-skirted 96 well plates| A000400|
| ALP_MagFLX_96_dwp_krm | Magnum FLX magnet for MoBio 2mL Deep Well Plates| A000400|
| MoBio_PowerMag_ep | 100mL Reservoir + 30mL Reservoir for Extraction| N/A|
| EP_Reserv_400_ep | 400mL Reservoir| 5075751364|
| EP_TT_PCR_150_h2 | Eppendorf full-skirted 96-well plates| E951020401|
| EP_TT_PCR_40 | Eppendorf 384-well plates| 30132742|
| BioRad_360_2 |BioRad Semi-Skirted 96 well plates| HSS9601|
| EP_MTP_384F |384-well flat-bottom plates for Synergy| 12-566-615|
| MoBio_DWP_ep | MoBio 2mL Deep Well Plates| 27100-4-EP-DWP|


----------


##**References**

>ASMsociety: Microbial Diversity Research Priorities- A Working Document for Mti-Agency Consideration. c2015. American Society of Microbiology. [Accessed: Aug 2015]. http://www.asm.org/index.php/public-affairs-report/114-unknown/unknown/5046-microbial-diversity-research-priorities-a-working-document-for-mti-agency-consideration

>Bentley R, Balasubramanian S, Swedlow HP, Smith GP, Milton J, Brown CG, Hall KP, Evers DJ, Barnes CL, Bignall HR, et al. 2008. Accurate whole human genome sequencing using reversible terminator chemistty. Nature 456(7218):53-59. Doi: 10.1038/nature07517 

>Capaoraso JG, Lauber CL, Walters, WA, Berg-Lyons D, Lozupone CA, Turnbaugh PJ, Fierer N, Knight R. 2011. Global patters of 16S rRNA diversity at a depth of millions of sequences per sample. Proc. Natl. Acad. Sci. USA 108(suppl.1):4516-4522. Doi: 10.1073/pnas.1000080107.

>Kozich JJ, Westcott SL, Baxter NT, Highlander SK, Schloss PD. 2013. Development of a dual –index sequencing strategy and curation pipline for analyzing amplicon sequence data on the MiSeq Illumina sequencing platform. Appl Envrion Microbiol. 79(17)5112-20. Doi: 10.1128/AEM.01043-13 

>Loman NJ, Misra RV, Dallman TJ, Constantinidou C, Gharbia SE, Wain J, pallen MJ. 2012. Performance comparison of benchtop high-throughput sequencing platforms. Nature Biotechnology. 30(5):434-439. Doi: 10.1038/nbt.2198

>Salipante SJ, Kawashima T, Rosenthal C, Hoogestraat DR, Cummings LA, Sengupta DJ, Harkins TT, Cookson BT, Hoffman NG. 2014. Appli. Environ. Microbiol. 80(24):7583. Doi: 10.1128/AEM.02206-14