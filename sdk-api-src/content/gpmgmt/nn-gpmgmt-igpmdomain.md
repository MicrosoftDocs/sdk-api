---
UID: NN:gpmgmt.IGPMDomain
title: IGPMDomain (gpmgmt.h)
author: windows-sdk-content
description: Represents a given domain and supports methods that allow you to query scope of management (SOM) objects, create, restore and query GPOs, and create and query WMI filters when you are using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmdomain.htm
tech.root: gpmc
ms.assetid: c3639f07-7c8c-4440-ade4-b58abd2586d6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMDomain, IGPMDomain, IGPMDomain interface [GPMC], IGPMDomain interface [GPMC],described, _win32_igpmdomain, gpmc.igpmdomain, gpmgmt/IGPMDomain
ms.topic: interface
f1_keywords: 
 - "gpmgmt/IGPMDomain"
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
 - IGPMDomain
 - GPMDomain
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMDomain interface


## -description


The 
<b>IGPMDomain</b> interface represents a specific domain and supports methods that allow you to perform the following tasks when you are using the Group Policy Management Console (GPMC) interfaces:
<ul>
<li>Query scope of management (SOM) objects.</li>
<li>Create, restore and query Group Policy objects (GPOs).</li>
<li>Create and query Windows Management Instrumentation (WMI) filters.</li>
</ul>To create a <b>GPMDomain</b> object, call the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getdomain">IGPM::GetDomain</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMDomain</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMDomain</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMDomain</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-creategpo">CreateGPO</a>
</td>
<td align="left" width="63%">
Creates and retrieves a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-getgpo">GetGPO</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> object that has a specified GPO ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-getsom">GetSOM</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">GPMSOM</a> object that has the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-getwmifilter">GetWMIFilter</a>
</td>
<td align="left" width="63%">
Retrieves a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object that has the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-restoregpo">RestoreGPO</a>
</td>
<td align="left" width="63%">
Restores a GPO from a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-searchgpos">SearchGPOs</a>
</td>
<td align="left" width="63%">
Executes a search for <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">GPMGPO</a> objects in the domain, and returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMGPOCollection</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-searchsoms">SearchSOMs</a>
</td>
<td align="left" width="63%">
Executes a search for <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">GPMSOM</a> objects (domains and organizational  units [OUs]) in the domain, and returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsomcollection">GPMSOMCollection</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmdomain-searchwmifilters">SearchWMIFilters</a>
</td>
<td align="left" width="63%">
Executes a search for <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> objects in the domain, and returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">GPMWMIFilterCollection</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMDomain</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmdomain-property-methods">Domain</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The full Domain Name System (DNS) name of the domain, such as "example.microsoft.com".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmdomain-property-methods">DomainController</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The full DNS name of the domain controller. This is the domain controller with which the GPMC is communicating. The domain controller is specified by the user in a call to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getdomain">IGPM::GetDomain</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">IGPMGPOCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsom">IGPMSOM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmsomcollection">IGPMSOMCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>
 

 

