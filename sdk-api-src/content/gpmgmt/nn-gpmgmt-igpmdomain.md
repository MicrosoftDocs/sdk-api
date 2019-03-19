---
UID: NN:gpmgmt.IGPMDomain
title: IGPMDomain (gpmgmt.h)
author: windows-sdk-content
description: Represents a given domain and supports methods that allow you to query scope of management (SOM) objects, create, restore and query GPOs, and create and query WMI filters when you are using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmdomain.htm
tech.root: gpmc
ms.assetid: c3639f07-7c8c-4440-ade4-b58abd2586d6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GPMDomain, IGPMDomain, IGPMDomain interface [GPMC], IGPMDomain interface [GPMC],described, _win32_igpmdomain, gpmc.igpmdomain, gpmgmt/IGPMDomain
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
 - IGPMDomain
 - GPMDomain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/32aee72f-96fa-4ebd-9ff7-643972b82cf6">IGPM::GetDomain</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMDomain</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMDomain</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/00e83637-820b-488e-abf4-4210ac3b98b6">CreateGPO</a>
</td>
<td align="left" width="63%">
Creates and retrieves a 
<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac413241-3649-4f22-9a67-94e4da8672e7">GetGPO</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> object that has a specified GPO ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbacd900-26ea-4554-97d8-8f33d2f5dd2b">GetSOM</a>
</td>
<td align="left" width="63%">
Retrieves the 
<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">GPMSOM</a> object that has the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/093fba1a-69b3-4045-891a-de9c6a78e166">GetWMIFilter</a>
</td>
<td align="left" width="63%">
Retrieves a 
<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> object that has the specified path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e202ea1-ca5c-4757-950b-ea1802699b68">RestoreGPO</a>
</td>
<td align="left" width="63%">
Restores a GPO from a 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19a8efae-0b85-49ba-bf7e-08ed700874c3">SearchGPOs</a>
</td>
<td align="left" width="63%">
Executes a search for <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">GPMGPO</a> objects in the domain, and returns a 
<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">GPMGPOCollection</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ca3b0ef-b0d5-408a-8d75-647546087155">SearchSOMs</a>
</td>
<td align="left" width="63%">
Executes a search for <a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">GPMSOM</a> objects (domains and organizational  units [OUs]) in the domain, and returns a 
<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">GPMSOMCollection</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e0abc25-bdcb-4277-90bb-542e922fc71c">SearchWMIFilters</a>
</td>
<td align="left" width="63%">
Executes a search for <a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">GPMWMIFilter</a> objects in the domain, and returns a 
<a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">GPMWMIFilterCollection</a> object.

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

<a href="https://msdn.microsoft.com/7d252302-6250-4c84-ad21-4b2bbe229da8">Domain</a>


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

<a href="https://msdn.microsoft.com/7d252302-6250-4c84-ad21-4b2bbe229da8">DomainController</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The full DNS name of the domain controller. This is the domain controller with which the GPMC is communicating. The domain controller is specified by the user in a call to the 
<a href="https://msdn.microsoft.com/32aee72f-96fa-4ebd-9ff7-643972b82cf6">IGPM::GetDomain</a> method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a>



<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">IGPMGPOCollection</a>



<a href="https://msdn.microsoft.com/e3252dba-403d-486d-b666-9bb04ec0aa90">IGPMSOM</a>



<a href="https://msdn.microsoft.com/079f2fd9-7b1e-4bb1-b342-8ed8fb2c773d">IGPMSOMCollection</a>



<a href="https://msdn.microsoft.com/801428f1-9ce5-4348-acab-23cc9ea8cac3">IGPMWMIFilter</a>



<a href="https://msdn.microsoft.com/8f65e6f6-fca3-46b7-aa0d-804470feb5bb">IGPMWMIFilterCollection</a>
 

 

