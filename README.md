# About

This personal project is a continuation of education in the field of information security and a hands-on practical approach. Its aim is to assess the current situation, improve security (both IT and physical) and increase awareness of individuals affected by this project.  
The activities described here were carried out in real systems (not in a lab environment) and with the consent (and cooperation) of the individuals to whom these systems belong.
By no means is this a how-to guide. All operations here were conducted by unexpirienced individual not employed in the information security. 

# Index

- [Project Goals](#project-goals)
- [Project Requirements](#project-requirements)
- [TLDR](#tldr)
- [Client Profile](#client-profile)
- [Risk Assessment](#risk-assessment)
    - [1.  Assesment Scope](#1-assessment-scope)
    - [2.  Identifying Assets](#2-identifying-assets)
    	- [2.1 Location A](#21-location-a)
			- [2.1.1 Physical](#211-physical-assets)
			- [2.1.2 Information Technology](#212-it-assets)
			- [2.1.3 Data Flow](#213-data-flow)
			- [2.1.4 Vulnerability Scanning](#214-vulnerability-scanning)
    	- [2.2 Location B](#22-location-b)
			- [2.2.1 Physical](#221-physical-assets)
			- [2.2.2 Information Technology](#222-it-assets)
			- [2.2.3 Data Flow](#223-data-flow)
			- [2.2.4 Vulnerability Scanning](#224-vulnerability-scanning)
	- [3. CIS RAM Risk Analysis|](#3-cis-ram-risk-analysis)
	- [4. Risk Treatment](#4-risk-treatment)
		-  [4.1 Governance](#41-governance)
		-  [4.2 Implementations](#42-implementations)
		-  [4.3 Configuration](#43-configuration)
		-  [4.4 Training and individial configurations](#44-training-and-individial-configurations)
		-  [4.5 Maintenance and Monitoring](#45-maintenance-and-monitoring)

- What's been accomplished
- Summary

&nbsp;

# Project Goals

- assesment of
- hardening systems
- implementing continous monitoring
- implementing Intrusion Prevention solutions
- preparing incident recovery solutions
- configuring remote communication for systems configuration and management
- increasing awareness of physical and IT security

&nbsp;

# Project Requirements

- dopasowanie rozwiązań do potencjalnych zagrożeń i analizy ryzyka
- możliwie niski koszt wdrożenia poprzez zastosowanie rozwiązań open source
- jeśli to możliwe, praca z użyciem istniejących urządzeń sieciowych
- we use every possible known way to harden systems without getting paranoid on threats that has no chance to appear

&nbsp;

# TLDR!

If you're in hurry and would rather like to take time reading new vulnerabilities....

&nbsp;

# Client Profile

This projects targets are systems in two separate locations and location themselves. In each of these locations operates two companies. In summary there are four small one-person businesses.  
Location A runs an office that accepts clients for Business 1. Business 2 at location A occupies the same office but does not meet with it's clients.  
Location B ic closed for any visitors.  
All businesses are low profile and operate in services industry.

For future reference:

- Location A
    - Business 1
    - Business 2
- Location B
    - Business 3
    - Business 4

All four businesses has marginal knowledge about information security.

&nbsp;

# Risk Assessment

This Risk Assessment is not "Enterprise grade". It's shape is tailored to address very small businesses
This is only qualitative analysis with no scope on finances.

## 1. Assessment Scope

Until the beginning of this project all four businesses did not evaluate any risk analysis so the scope of this project is to assess general security posture. This assesment will take into consideration physical and IT components.  
This project does not cover mission, obligations and policies issues because they are usually the responsibility of management which, due to the scale of these businesses, is simply missing.

## 2. Identifying Assets

### 2.1 Location A

#### 2.1.1 Physical assets

#### 2.1.2 IT assets

#### 2.1.3 Data Flow

#### 2.1.4 Vulnerability Scanning 

==obrazek z wynikami skanowania==
==link do raportu ze skanowania==

### 2.2 Location B
&nbsp;
#### 2.2.1 Physical assets
==zweryfikować safeguard 1.1==
||inventory <br>identifier|asset|
|-|-|-|
|1.|L2-P1|Premises gate with lock|
|2.|L2-P2|Lock on the entry door|

&nbsp;
#### 2.2.2 IT assets

![location-mod.jpg](:/3e845ad86a484adfa3abe3a997c45200)

||inventory <br> identifier|type|model|firmware version|
|-|-|-|-|-|
|1.|L2-IT1|Modem LTE|Huawei B525s-23a|11.230.03.01.55|
|2.|L2-IT2|All-In-One Router|TP-Link Archer C80|1.13.2|
|3.|L2-IT3|Linux Workstation|Arch Linux|Kernel 6.8.1|
|4.|L2-IT4|Linux Workstation|Arch Linux|Kernel 6.8.1|
|5.|L2-IT5|Laptop|Arch Linux|Kernel 6.8.1|
|6.|L2-IT6|Laptop|Windows 11||
|7.|L2-IT7|Multifunction Device|Brother MFC J5910DW|F|
|8.|L2-IT8|Smart TV| Samsung .... |....|
|9.|L2-IT9|Smartphone|Blackview BV9900 Pro|Android 10|
|10.|L2-IT10|Smartphone|Samsung.....|.....|
|11.|L2-IT11|NAS|TrueNas ......... | ..... |

&nbsp;
#### 2.2.3 Data Flow
&nbsp;

![data-flow-L2-B1.jpg](:/496ca11b93584c068e17175707cbedd3)
![data-flow-L2-B2.jpg](:/c2d5906e4f13423a8618388ef4b87c98)

#### 2.2.4 Vulnerability Scanning

**Nessus - Basic Network Scan**
![Location B - 1.png](:/7f00a4e41a6440c3aa725f8a3fe3a004)

**Nessus - Basic Network Scan with credentials provided**
![Location B - credentials - 1.png](:/bd6f297fb541427a8ede2c6331f0efe6)

**Nessus - Basic Network Scan with credentials report**

[Location B - credentials_rmnxdq.pdf](:/f49f48e21b3d410588fd1434234b395c)

[Back to index](#index)

## 3. CIS RAM Risk Analysis 

Due to limited cybersecurity expertise and to have a well defined starting point I've decided to use CIS Risk Assessment Method. It's a structured approach to conducting cybersecurity risk assessments. It provides a framework to identify, analyze, and prioritize cybersecurity risks based on industry-recognized standards. CIS RAM aims to help organizations improve their cybersecurity posture by providing guidance on risk management, controls, and mitigation strategies. 

For this project I've used IG1 set of safeguards as a basis and some IG2 and IG3 safeguards where it was relevant. I also removed some IG1 safeguards which did not relate to projects conditions and targeted businesses.

It is worth emphasizing that although we are dealing with 4 different businesses, for the purposes of this project we often treat them as one organization. It's best for making the whole process simpler. 

[link to CIS RAM](https://www.cisecurity.org/insights/white-papers/cis-ram-risk-assessment-method)



![CIS_RAM_v2.1_for_IG1_Workbook.22.05.jpg](:/471610d4f1ba46d5ae6eda3883780d0f)


## 4. Risk Treatment 



All actions needed to be performed in the scope of Risk Treatment has been divided into 5 groups:
- [4.1 Governance](#41-governance)
- [4.2 Implementations](#42-implementations)
- [4.3 Configuration](#43-configuration)
- [4.4 Training and individial configurations](#44-training-and-individial-configurations)
- [4.5 Maintenance and Monitoring](#45-maintenance-and-monitoring)
***
### 4.1 Governance

![1.Governance.jpg](:/215b562d28e9419b9be5f62074c80635)


### 4.2 Implementations

![2.Implementations.jpg](:/474bb6d4b2a943e1b2f335bd98805e90)


### Rebuilding Network Architecture to address segmenation

 to limited cybersecurity expertise and to have a well defined starting point I've decided to use CIS Risk Assessment Method. It's a structured approach to conducting cybersecurity risk assessments. It provides a framework to identify, analyze, and prioritize cybersecurity risks based on industry-recognized standards. CIS RAM aims to help organizations improve their cybersecurity posture by providing guidance on risk management, controls, and mitigation stra

### Deploying host-based firewall with intrusion detection and prevention solutions


### Establishing backup solutions

### Deploying Host-Based Intrusion Prevention Solutions

||||
|-|-|-|
|![location-2-mod-rebuilt.jpg](:/9388884beb314c9b9b00f8c958e59673)|||

- 

### 4.3 Configuration

![3.Config.jpg](:/eb06d3c0e1244f40b2c51ec9cdf55221)



### 4.4 Training and individial configurations

![4.Training.jpg](:/b3ad270e9c594d848552df4317c22e88)

IT assets used by individuals are not only used for work purposes but also for personal activity. This is why it's important to address both work and personal activities to limit risk of unwanted actions leading to exposing vulnerabilities. Training on social engineering methods, guidance (help) with safe software instalation and management and general IT hygiene to preserve privacy 

***

## Training on phishing smishing and vishing methods used for stealing credentials or money

Training on recognizing social engineering attacks is an important part of this project. Nowadays ==dane dot. udziału ataków social engineering w całym rynku security== So taking into count that work assets are used for social media and other personal activities it's important to bring caution to every 

&nbsp;
***
### Creating dedicated contact for security incidents and alerts


### 4.5 Maintenance and Monitoring
|Tekst||
|-|-|
|![5.Maintenance.jpg](:/f34c7b104ba1478083e37f49d65fc982)|any information|








