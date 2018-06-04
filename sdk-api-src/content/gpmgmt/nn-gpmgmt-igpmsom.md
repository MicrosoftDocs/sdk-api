---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IGPMSOM interface


## -description


The 
<b>IGPMSOM</b> interface contains methods that allow you to create and retrieve GPO links for a scope of management (SOM), and to set and retrieve security attributes and various properties for a SOM. A SOM can be a site, domain or OU.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSOM</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMSOM</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMSOM</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f3d8234-617f-4ce4-846a-476c28251989">CreateGPOLink</a>
</td>
<td align="left" width="63%">
Links a GPO to the specified position and sets various link-specific properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cab93e8e-d91d-47b6-9b33-adcf06fb9e41">GetGPOLinks</a>
</td>
<td align="left" width="63%">
Returns a collection of GPO links for the SOM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/545ab05a-b25e-40a7-b002-6935587764a5">GetInheritedGPOLinks</a>
</td>
<td align="left" width="63%">
Returns a collection of GPO links that are applied to the SOM, including links inherited from parent containers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b120bf6-17f8-43d7-a27c-b7674535c1d3">GetSecurityInfo</a>
</td>
<td align="left" width="63%">
Returns a collection of 
<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">GPMPermission</a> objects for the SOM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/675de64c-4eef-47c8-a06c-9167559b11a9">SetSecurityInfo</a>
</td>
<td align="left" width="63%">
Sets the list of permissions for the SOM.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSOM</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/733be6ee-47bd-4599-93f3-989aeac67ed5">GPOInheritanceBlocked</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Value that specifies whether GPO inheritance is blocked for the SOM.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Name of the SOM.

If IGPMSOM points to an OU, as in "Ou=testou,dc=example,dc=Microsoft,dc=com", this property is the last part of the name, that is, testou. If IGPMSOM points to a domain, as in "dc=example,dc=Microsoft,dc=com", this property is "example.microsoft.com". If it points to a site, this property is the website name; for example, "Default-first-site-name".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915708">Path</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Distinguished name of the SOM; for example, "ou=MyOU,dc=coname,dc=com".

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Type of the SOM. The following types are defined:

<ul>
<li><b>somSite</b></li>
<li><b>somDomain</b></li>
<li><b>somOU</b></li>
</ul>
</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/7ac19065-571e-45f5-934f-35ddbf225262">IGPMPermission</a>
 

 

