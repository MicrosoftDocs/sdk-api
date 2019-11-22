---
UID: NN:gpmgmt.IGPMRSOP
title: IGPMRSOP (gpmgmt.h)

description: The IGPMRSOP interface provides methods that support making Resultant Set of Policy (RSoP) queries in both logging and planning mode.
old-location: gpmc\igpmrsop.htm
tech.root: gpmc
ms.assetid: 86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3

ms.date: 12/05/2018
ms.keywords: GPMRSOP, IGPMRSOP, IGPMRSOP interface [GPMC], IGPMRSOP interface [GPMC],described, _win32_igpmrsop, gpmc.igpmrsop, gpmgmt/IGPMRSOP
ms.topic: interface
f1_keywords: 
 - "gpmgmt/IGPMRSOP"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMRSOP interface


## -description


The 
<b>IGPMRSOP</b> interface provides methods that support making Resultant Set of Policy (RSoP) queries in both logging and planning mode. The typical use of this interface is to set various properties required for a particular RSoP query and then to call the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-createqueryresults">CreateQueryResults</a> method. RSoP planning mode requires Windows Server on the domain controller used to perform the query. RSoP logging mode requires that the computer being targeted be running Windows Server.
To create a  <b>GPMRSOP</b> object, call the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getrsop">IGPM::GetRSOP</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMRSOP</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGPMRSOP</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-createqueryresults">CreateQueryResults</a>
</td>
<td align="left" width="63%">
Executes a Resultant Set of Policy (RSoP) query that supports both logging mode and planning mode queries.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-generatereport">GenerateReport</a>
</td>
<td align="left" width="63%">
Generates an RSoP report based on the query specified in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-generatereport">GenerateReport</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-generatereporttofile">GenerateReportToFile</a>
</td>
<td align="left" width="63%">
Generates an RSoP report based on the query specified in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-generatereporttofile">GenerateReportToFile</a> and saves it to a file at a specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-loggingenumerateusers">LoggingEnumerateUsers</a>
</td>
<td align="left" width="63%">
Enumerates all users who have logging mode data on a specific computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-releasequeryresults">ReleaseQueryResults</a>
</td>
<td align="left" width="63%">
Releases the WMI namespace allocated by a call to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmrsop-createqueryresults">IGPMRSOP::CreateQueryResults</a> method.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">LoggingComputer</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">LoggingFlags</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">LoggingUser</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">Mode</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">Namespace</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningComputer</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningComputerSecurityGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Security groups to associate with the computer during planning mode simulation. This property is an array of variants that contain 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a> interface pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningComputerSOM</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningComputerWMIFilters</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
WMI filter to associate with the computer during planning mode simulation. This property is an array of variants that contain 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a> interface pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningDomainController</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningFlags</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningSiteName</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningUser</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningUserSecurityGroups</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Security groups to associate with the user during planning mode simulation. This property is an array of 
variants that contain <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a> interface pointers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningUserSOM</a>


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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmrsop-property-methods">PlanningUserWMIFilters</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
WMI filters to associate with the user during planning mode simulation. This property is an array of 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a> interface pointers.

</td>
</tr>
</table> 


## -remarks



For more information about security groups, see 
<a href="https://docs.microsoft.com/windows/desktop/AD/how-security-groups-are-used-in-access-control">How Security Groups are Used in Access Control</a> in the Active Directory Programmer's Guide.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmtrustee">IGPMTrustee</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>
 

 

