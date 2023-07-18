# Monthly Process
This is a slow and arduous process when done manually. It took approximately 1 and half weeks of an FTE every month to complete. It is now down to less than an hour with some elbow grease and liberal use of Python.
Error rate went from 6% to 0%, as it no longer relies on direct manual input and has been routinely overseen for edge cases. 

## Impact
![flow chart of process, and the time impact of optimization](https://github.com/david-c-brown/clinic_kpi_monthly/blob/main/process_impact.gv.png)

## Approach
cpt_analysis was the first file in this tree to be finalized and the most impactful overall. Many of the tools, tricks, and processes used in it are seen in some way across this process. A monthly cadence of a 40-hour project is not sustainable, especially as we looked to open more and more clinics (depending on # of providers, each clinic took 90-120 minutes assuming no errors)

load is the product of an internal CRM being laborious to modify, and no accessible API for metric updates. Everything needed to be through the UI. This raised some interesting issues, as the descriptors on the site are inconsistent from location to location. A lot of trial and error, a few other projects that had to get done, and some assistance grabbing selectors from ChatGPT led to this streamlined, automated data entry program.

## Further optimizations
Updating rev_analysis to inject numbers directly into the master spreadsheet would be ideal, but the usage of dropbox for file management makes the saved files more likely to corrupt due to version control.
