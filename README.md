# PASTOR

## ABOUT
The Pain Assessment Screening Tool and Outcomes Registry (PASTOR) is a 20-30 minute screening assessment for individuals with chronic pain. PASTOR was developed in response to the National Defense Authorization Act (NDAA) 2010 recommendation for “performance measures used to determine the effectiveness of the policy in improving pain care for beneficiaries enrolled in the military health care system.” As a result of the NDAA recommendation the Army Pain Management Task Force was convened to conceive and design an outcomes registry to facilitate pain research and provide clinical outcomes data to improve evidence based decision making by providers.

For more information about PASTOR please visit the [Defense and Veterans Center for Integrative Pain Management](http://www.dvcipm.org/clinical-resources/pain-assessment-screening-tool-and-outcomes-registry-pastor)

## This Project
This GitHub project is specifically aimed at:
  1. Tracking the current status of the cue sheet (list of variables and questions)
  2. Tracking the current status of the data dictonary for use in REDCap
  3. Tracking the current status of the reporting scripts for generating the PDF report. 
  
## Installation 

Note: This assumes that our forked branch of the [SUSOM REDCap-extra hooks](https://github.com/susom/redcap-extras) have already been installed into your instance of REDCap.  If not, please find our forked version which enables single and double clicked images here [https://github.com/jpsuen/redcap-extras](https://github.com/jpsuen/redcap-extras)

### To get started with a new REDCap project.
  1. Create a new Project in REDCap
  2. Copy the pidXXX folder using the new PID of your REDCap project
  3. Utilize the data dictonary or the XML - CDISC ODM formatted document available within the data_dictonary folder of this project.  
  4. Adjust the timepoints and branching logic to meet the needs of your implementation.
  
### To generate the PDF Report.
  1. Install wkhtmltopdf in your local environment
  2. Install Mike Haertl's PHP wrapper for wkhtmltopdf available here: [https://github.com/mikehaertl/phpwkhtmltopdf](https://github.com/mikehaertl/phpwkhtmltopdf)
  3. Install the the files located in the report.php section into you /plugins folder on your REDCap instance.
  4. Update any variable names that may have been added/removed/changed when you set-up the project.
  5. On the final instrument administered on REDCap update the 'Survey Termination Options' to 'Redirect to a URL' and point to the location of the plugin installed in step 3 using piping for the project id number. 

## FAQ
  1. How can I use PASTOR?
    - Currently PASTOR has been developed into the Research Electronic Data Capture (REDCap) system which was developed by Vanderbilt University.  It is freely available to not for-profit organizations at [https://projectredcap.org/](https://projectredcap.org/)
    
  2. What if I want to use a system other than REDCap?
    - PASTOR is a collection of validated instruments and a structured format for displaying and reporting data.  Integration into third party systems such as an EHR like Epic or Cerner can be completed as needed by your organization.  REDCap was only utilized as a way to lower the barriers to entry for a large majority of researchers and clinicians. 
  
  3. What does the assessment look like in REDCap?
    - A sample assessment can be taken via a link on the [DVCIPM website](http://www.dvcipm.org/clinical-resources/pain-assessment-screening-tool-and-outcomes-registry-pastor).
  
  4. How do I use REDCap?
    - Unfortunately we are unable to provide direct support for obtaining, installing, or utilziing the REDCap software.  That said, the [REDCap consortium](https://projectredcap.org/resources/community/) is a great place to look for answers.  
    
  5. Is PASTOR HIPAA compliant?
    - If your organization is a 'Covered Entity' under HIPAA, it is the responsibility of your Security and Privacy Officer 
