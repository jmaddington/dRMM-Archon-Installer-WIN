# Overview #
This repo is a Datto RMM Component to install the Zorus Archon agent.

# Usage #
Download aem-component.cpt from this repository and import it into your dRMM environment.

Download the version of Zorus you want to deploy, name it ZorusInstaller and upload it to the imported component.

You will need to set the site deployment token at EITHER the script level OR the site level (recommended). If setting
at the site level, name it site_archon_deployment_token in the RMM. Leaving the runtime token at 0 will tell the script to default to the site variable.

If BOTH are specified the component will attempt installation with the token provided at runtime (at the script level).

##Output

The component will error out if a deployment key isn't set or the installer is not present. Past that it should exit successfully, even if installation is NOT successful because MSI exit codes.

# Building #

Download or fork, run repackage.bat and upload aem-component.cpt to dRMM. You can also download the aem-component.cpt straight from this repository and install in your dRMM instance.