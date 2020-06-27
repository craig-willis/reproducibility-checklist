# Reproducibility assessment checklist

The purpose of results validation review is to:
* Ensure that the author has provided sufficient information for a third party to reproduce the computational results reported in the manuscript
* Perform a reproducibility assessment or reproduction to confirm that the results match those reported in the manuscript

## Packaging and archiving

* All data and code should be accessible through a suitable archival repository.  While open access is strongly encouraged, restricted access is permissible if justified (including proprietary, confidential or otherwise protected information). If data and code are protected, access instructions must be provided.
* Github repositories are an excellent way to collaboratively develop and release software. However, Github repositories are not considered archival.  Use the Zenodo integration to publish a release of your package to Zenodo and obtain a persistent identifier (DOI)
* If your manuscript describes a software package, consider whether it is appropriate to include manuscript information and results in the software archive or whether you may want to have a separate repository/package with scripts, data, and documentation specific to the manuscript. 

## Documentation
* Every verification package must include a top-level README that contains a brief description of all files and detailed instructions required for verification/reproduction. This includes how to install and configure a system and execute all computational steps required to verify the results reported in the manuscript. 


## Software
* Include all scripts, commands, and libraries necessary to reproduce results reported in the manuscript  (including figures, tables, and other analytical results). Include any wrapper scripts used (e.g., job submission etc). Consider providing a single master script that can be used to reproduce computational steps end-to-end.
* Include all scripts and commands required to construct datasets (e.g., simulation output, analysis datasets from source datasets, preprocessing scripts)
* Scripts should accurately reproduce results (up to rounding). Any potential differences due to randomness should be noted. Always document random seed values.
* All scripts should use relative file paths and include detailed comments explaining the steps to reproduce any results. Comments should indicate workflows/commands used for individual tables, figures or other outputs.
* If any software cannot be provided directly, include specific citations or software access protocol describing the steps required to gain access. 

## Data 
* Include all data files required to reproduce results. 
* If the original data files cannot be included for any reason, include specific citations or data access protocols. A data access protocol describes the steps required to gain access to the data. Scripts should clearly indicate how to specify any data not provided as part of the package.
* For externally referenced data, include information about source data versions and access dates.

## Results
* Include all results output in the archive. This includes figures, tables, or related output as well as data behind figures and results. 
* Capture one or more log files containing the output (i.e., informational, warning, and errors) of all scripts used when generating results used in publication. 

## Environment
* Include a specification of the environment used to execute all scripts and programs. This includes operating system and all software dependencies, including versions. 
* Optionally, include a virtual machine image, container specification or image (e.g., Dockerfile or Docker image)
* Include estimates of resources required including number of cores, memory, and approximate execution time.

## Citation and Identification
* The verification package (and associated Github repo, if present) should include references to the manuscript via citation and DOI.  It should be possible for a reader of the manuscript to easily find the archived package and for the discoverer of the archived package or Github repo to easily find the associated manuscript.
* The verification package should include any references to external data or software via citation and DOI, when possible.
* The verification package itself should be published to an archival repository with a persistent identifier (DOI) that can be referenced in the manuscript.

## License and Copyright
* Include appropriate licenses and copyright notices for code, content, and data.  Recommended include MIT for code components and CC-BY for media components.
