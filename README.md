
# 'Rubrik' Opspack '1.0.0' [![Build Status](https://travis-ci.org/rubrikinc/rubrik-opspack-for-opsview.svg?branch=master)](https://travis-ci.org/rubrikinc/rubrik-opspack-for-opsview)

Rubrik is a single platform that manages all data in the cloud, at the edge, or on-prem for backup, disaster recovery, archival, compliance, analytics, and copy data management. Rubrik powers on your data instantly (for recovery to test/dev) and unleashes hard savings from a converged architecture.

## What You Can Monitor

This opspack provides checks to monitor the following:

* Node Status - Count of Nodes up/down in the cluster
* Runway Remaining - Days remaining before protection is unavailable
* Cluster Storage - Remaining Storage Available across the cluster

## Service Checks

| Service Check | Description |
|:------------- |:----------- |
| Rubrik - Check Node Status | Count of Nodes up/down in the cluster |
| Rubrik - Check Runway | Days remaining before protection is unavailable |
| Rubrik - Cluster Storage | Remaining Storage Available across the cluster |

## Prerequisites

The scripts require the following Python modules to operate:

* rubrik_cdm
* nagiosplugin
* urllib3

To install these python dependancies, you can do the following:

### Install PIP

*Debian/Ubunutu*

`sudo apt-get install python-pip`

*CentOS/RHEL*

`sudo yum install python-pip`

### PIP Packages

```
sudo pip install rubrik_cdm
sudo pip install nagiosplugin
sudo pip install urllib3
```

## Setup 'Host' for Monitoring

It is recommended that you use a Rubrik ReadOnly account to read the information from the Rubrik cluster. 
  
## Setup and Configuration

To configure and utilize this Opspack, you simply need to add the 'Rubrik' Opspack to your Opsview Monitor system.

#### Step 1: Add the host template

Add the `Applicaiton - Rubrik` Host Template to the Rubrik Host

![Add host template](/docs/img/add_opspack_host.png?raw=true)

#### Step 2: Add and configure variables required for this host

RUBRIK_CREDS - Credentials Variable storing Username/Password for the Account that will authenticate and interact with the Rubrik API.

![Add variables](/docs/img/add_opspack_variables.png?raw=true)

#### Step 3: Reload and the system will now be monitored

![View Service Checks](/docs/img/view_opspack_service_checks.png?raw=true)
