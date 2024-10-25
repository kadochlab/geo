# Kadoch Lab NCBI GEO Accessioning Guide

[NCBI Gene Expression Omnibus (GEO)](https://www.ncbi.nlm.nih.gov/geo/) is a public functional genomics data repository supporting MIAME-compliant data submissions. Given that RNA-seq, ATAC-seq, ChIP-seq, CUT&TAG, and CUT&RUN are all functional genomics data commonly derived by the lab, all data associated with published research papers will need to be archived with NCBI GEO upon publication. Here is an opinionated guide for conducting and documenting experiments and computational analyses that ensures that important experimental details necessary for GEO accessioning are properly captured and reported, making the accessioning process straightforward and less prone to error.

The [general submission information page](https://www.ncbi.nlm.nih.gov/geo/info/submission.html) at GEO provides a lot of useful information and I encourage everyone to read through it. GEO accepts data in the form of high throughput sequencing (HTS) datasets, such as the Illumina data that we commonly generate, and this will be the most common type of submission we perform. However, microarray data are also accessioned in GEO - we occassionally handle microarray data in the lab too. The below details are tailored to the HTS datasets but a lot of the information will apply more generally.

NCBI generally uses Excel spreadsheet templates to gather important data and experimental details, which is parsed by their systems to derive the information needed for the GEO record. [Here is the spreadsheet template for HTS data submissions.](https://www.ncbi.nlm.nih.gov/geo/info/examples/seq_template.xlsx) Instructions and examples are provided therein for completing the forms properly and I outline some important details below. Instructions are both in-line and are also included as pop-up messages on the cells with the red triangle in the top-right corner - simply hover over the cell to see the message. Please ensure you are careful with formatting the text to avoid poorly formatted records or submission issues.

In practice, the computational biologist working on the project will be responsible for accessioning data to GEO. However, they rely a lot on details from the experimentalists. Moreover, the computationalist must keep track of important data processing details. Therefore, I make the following recommendations for how you should approach your work to ensure a smooth process:

## Experimentalists

I highly recommend filling out the GEO template for each genomics experiment and submission you perform. Ideally, this is done at the same time as the experiment to ensure important details are properly captured.

In the HTS GEO submission template, you will insert experimental details under the `Metadata` tab - this is the only place you will need to provide information (the computationalist will deal with everything else). Below is a list of the fields you will need to provide information for - all are mandatory.

1. `STUDY` --> `title`: A title for your study. Usually we end up using the paper's title, so it is fine to use an informative placeholder at first, which can get modified later.
2. `STUDY` --> `summary (abstract)`: An abstract for your study. Usually we end up using the paper's abstract, but for now, you can add some important details as a placeholder.
3. `STUDY` --> `experimental design`: Details of the experimental design - see the pop-up instructions. *You should fill this out completely when conducting your experiment, as these are important details. Modifications can always be made later.*
4. `STUDY` --> `contributor`: You should list yourself, other experimentalists involved with the work, the computationalist, and Cigall as contributors (potentially others, but at least these people). As instructed, ensure you have a comma between your names/initials so the data is properly parsed.
5. `SAMPLES` --> `library name`: This is a *unique* library name for each sample that was sequenced. Generally, the `Sample Name` field we record on our sequencing spreadsheet will be what you use here. Try to standardize the formatting as much as possible and stay way from special characters - characters other than alphanumeric, "-", "_", or ".".
6. `SAMPLES` --> `title`: This is a *unique* title for each sample that was sequenced. It will probably take some of the information from the library name field, but could include additional information, and it should be written in a more human-readable format, like a sentence.
7. `SAMPLES` --> `organism`: Self explanatory - the genus and species for the organism. Homo sapiens, Mus musculus, etc.
8. `SAMPLES` --> combination of one or more of `tissue`, `cell line`, `cell type`, `genotype`, or `treatment`, depending on the context of the samples/cells used and experimental details.
9. `SAMPLES` --> `molecule`: Select the appropriate molecule type from the drop-down menu.
10. `SAMPLES` --> `single or paired-end`: Select single or paired-end from the drop-down menu.
11. `SAMPLES` --> `instrument model`: Select the instrument and model of the sequencer used in the experiment from the drop-down menu.
12. `PROTOCOLS` --> `growth protocol`: Describe the details of how organisms or cells were maintained prior to or during the experiment. *You should fill this out completely when conducting your experiment, as these are important details. Modifications can always be made later.*
13. `PROTOCOLS` --> `treatment protocol`: Describe the treatments applied in the experiment performed. *You should fill this out completely when conducting your experiment, as these are important details. Modifications can always be made later.*
14. `PROTOCOLS` --> `extract protocol`: Describe the protocols used to extract and prepare the material for sequencing. *You should fill this out completely when conducting your experiment, as these are important details. Modifications can always be made later.*
15. `PROTOCOLS` --> `library construction protocol`: Describe the details of the genomics library preparation you performed. *You should fill this out completely when conducting your experiment, as these are important details. Modifications can always be made later.*
16. `PROTOCOLS` --> `library strategy`: Identify the library strategy: RNA-seq, ATAC-seq, ChIP-seq, CUT&TAG, or CUT&RUN.
