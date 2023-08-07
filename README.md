# CHEP23-xrootd-NRP-data
Supplemental material for the CHEP23 poster "IceCube experience using XRootD-based Origins with GPU workflows in PNRP"

## Data

* `runtimes.csv` - A CSV file with job data:
  * GPU type name
  * Job end date/time in unix time
  * Wallclock time of the job
  * Number of CPU cores used by the job

* `filesizes.csv` - A CSV file with output file metadata:
  * Storage site
  * Job index (unique to storage site)
  * Job type (GPU, CPU1, CPU2)
  * Last modified date in unix time
  * File size in bytes

## Workflow Description

There are three storage sites, with job sets specifically targetted at each
site. Within a job set, there are many independent dags which run physics
workflows. Specifically, there is a GPU job that runs first, then two CPU
jobs.

## Notes

Not all jobs have successfully completed, due to various errors (some
in computing, some in physics code).  This data only encompasses completed
jobs.
