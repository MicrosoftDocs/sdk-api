---
UID: NN:gpmgmt.IGPMRSOP
title: IGPMRSOP (gpmgmt.h)
author: windows-sdk-content
description: The IGPMRSOP interface provides methods that support making Resultant Set of Policy (RSoP) queries in both logging and planning mode.
old-location: gpmc\igpmrsop.htm
tech.root: gpmc
ms.assetid: 86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMRSOP, IGPMRSOP, IGPMRSOP interface [GPMC], IGPMRSOP interface [GPMC],described, _win32_igpmrsop, gpmc.igpmrsop, gpmgmt/IGPMRSOP
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMRSOP
 - GPMRSOP
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMRSOP interface


## -description


The 
<b>IGPMRSOP</b> interface provides methods that support making Resultant Set of Policy (RSoP) queries in both logging and planning mode. The typical use of this interface is to set various properties required for a particular RSoP query and then to call the 
<a href="https://msdn.microsoft.com/2259a014-3ecb-480d-ab65-9d27c0acf26c">CreateQueryResults</a> method. RSoP planning mode requires Windows Server on the domain controller used to perform the query. RSoP logging mode requires that the computer being targeted be running Windows Server.
To create a  <b>GPMRSOP</b> object, call the 
<a href="https://msdn.microsoft.com/61a1be3e-d959-47e2-ad6c-ca00accd0afe">IGPM::GetRSOP</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMRSOP</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGPMRSOP</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMRSOP</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2259a014-3ecb-480d-ab65-9d27c0acf26c">CreateQueryResults</a>
</td>
<td align="left" width="63%">
Executes a Resultant Set of Policy (RSoP) query that supports both logging mode and planning mode queries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86766a08-4f3a-4758-8abc-83db3408f0fd">GenerateReport</a>
</td>
<td align="left" width="63%">
Generates an RSoP report based on the query specified in <a href="https://msdn.microsoft.com/86766a08-4f3a-4758-8abc-83db3408f0fd">GenerateReport</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92a199d6-244f-44e5-8158-d77b8488fde0">GenerateReportToFile</a>
</td>
<td align="left" width="63%">
Generates an RSoP report based on the query specified in <a href="https://msdn.microsoft.com/92a199d6-244f-44e5-8158-d77b8488fde0">GenerateReportToFile</a> and saves it to a file at a specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cc794e6-1a8d-4e31-9bea-4ebc4cf51602">LoggingEnumerateUsers</a>
</td>
<td align="left" width="63%">
Enumerates all users who have logging mode data on a specific computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2bf9050-4db0-4bf0-a063-0076ba191ff6">ReleaseQueryResults</a>
</td>
<td align="left" width="63%">
Releases the WMI namespace allocated by a call to the 
<a href="https://msdn.microsoft.com/2259a014-3ecb-480d-ab65-9d27c0acf26c">IGPMRSOP::CreateQueryResults</a> method.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMRSOP</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">LoggingComputer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the computer being logged.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">LoggingFlags</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Logging mode flags. This property can be one of the following:

<ul>
<li><b>RSOP_NO_COMPUTER</b></li>
<li><b>RSOP_NO_USER</b></li>
</ul>
<b>RSOP_NO_COMPUTER</b> and <b>RSOP_NO_USER</b> must not be specified together.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">LoggingUser</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the user targeted in logging mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">Mode</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
RSOP mode. This property can be one of the following: <b>rsopUnknown</b>, <b>rsopPlanning</b>, or <b>rsopLogging</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">Namespace</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
RSOP WMI namespace generated as output from an RSoP simulation. The format is typically "\\computername\root\rsop\namespace".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningComputer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the computer to use during planning mode simulation. This is the SAM account name of the Computer object; for example, example\computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningComputerSecurityGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Security groups to associate with the computer during planning mode simulation. This property is an array of variants that contain 
<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a> interface pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningComputerSOM</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Scope of management (SOM) to use for the computer during planning mode simulation. This is the distinguished name of the Active Directory container in which the computer object  resides, for purposes of the RSoP simulation. It is not necessary that this property be the true location where the object currently resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningComputerWMIFilters</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
WMI filter to associate with the computer during planning mode simulation. This property is an array of variants that contain 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a> interface pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningDomainController</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the DC to use in planning mode. This can be a DNS name or a NetBIOS name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningFlags</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Planning mode flags. The value of this property can be one or more of the following constants combined with OR operators.

<ul>
<li><b>RSOP_NO_COMPUTER</b></li>
<li><b>RSOP_NO_USER</b></li>
<li><b>RSOP_PLANNING_ASSUME_SLOW_LINK</b></li>
<li><b>RSOP_PLANNING_ASSUME_LOOPBACK_MERGE</b></li>
<li><b>RSOP_PLANNING_ASSUME_LOOPBACK_REPLACE</b></li>
<li><b>RSOP_PLANNING_ASSUME_USER_WQLFILTER_TRUE</b></li>
<li><b>RSOP_PLANNING_ASSUME_COMP_WQLFILTER_TRUE</b></li>
</ul>
<b>RSOP_NO_COMPUTER</b> and <b>RSOP_NO_USER</b> must not be specified together.

<b>RSOP_PLANNING_ASSUME_LOOPBACK_MERGE</b> and
<b>RSOP_PLANNING_ASSUME_LOOPBACK_REPLACE</b> must not be specified together.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningSiteName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the site to use during planning mode simulation; for example, Default-first-site-name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningUser</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the user for planning mode simulation. This is the Security Accounts Manager (SAM) account name of the User object; for example, example\user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningUserSecurityGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Security groups to associate with the user during planning mode simulation. This property is an array of 
variants that contain <a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a> interface pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningUserSOM</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the user scope of management (SOM) to use during planning mode simulation. This is the distinguished name of the Active Directory container in which the user object  resides, for purposes of the RSoP simulation. It is not necessary that this property be the true location where the object currently resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">PlanningUserWMIFilters</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
WMI filters to associate with the user during planning mode simulation. This property is an array of 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a> interface pointers.

</td>
</tr>
</table> 


## -remarks



For more information about security groups, see 
<a href="https://msdn.microsoft.com/3236c51f-21c1-4c07-9b76-2668ae72a42f">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.




## -see-also




<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/f9c24fe6-58c7-4e82-9ac0-1157ed8fffeb">IGPMTrustee</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>
 

 

