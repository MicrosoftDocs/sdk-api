---
UID: NN:gpmgmt.IGPMSitesContainer
title: IGPMSitesContainer
author: windows-sdk-content
description: The IGPMSitesContainer interface provides the methods required to access the scope of management (SOM) objects that represent sites in a forest.
old-location: gpmc\igpmsitescontainer.htm
tech.root: GPMC
ms.assetid: e3fdfd44-9e90-4206-b7e9-97d4ed6eb8af
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMSitesContainer, IGPMSitesContainer, IGPMSitesContainer interface [GPMC], IGPMSitesContainer interface [GPMC],described, _win32_igpmsitescontainer, gpmc.igpmsitescontainer, gpmgmt/IGPMSitesContainer
ms.prod: windows
ms.technology: windows-sdk
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
 - IGPMSitesContainer
 - GPMSitesContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMSitesContainer interface


## -description


The 
<b>IGPMSitesContainer</b> interface provides the methods required to access the scope of management (SOM) objects that represent sites in a forest. The <b>GPMSitesContainer</b> object represents the forest-level container that contains the actual sites in a forest. To create a <b>GPMSitesContainer</b> object, call the 
<a href="https://msdn.microsoft.com/0a1b8975-cd73-49e6-83b9-f6af296276cb">IGPM::GetSitesContainer</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSitesContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMSitesContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMSitesContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8b459d0-d0f5-48b1-8870-487a1645ae7a">GetSite</a>
</td>
<td align="left" width="63%">
Returns the scope of management (SOM) object that corresponds to the site.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcbe1d94-ae82-4b33-8831-039896816a2d">SearchSites</a>
</td>
<td align="left" width="63%">
Retrieves a collection of SOMs for the specified search criteria.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMSitesContainer</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc1cb43b-2e18-45a7-9fda-b43e5a674b62">Domain</a>


</td>
<td align="left" width="63%">
Name of the domain being used to perform site operations. This is a full DNS name, such as, example.microsoft.com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc1cb43b-2e18-45a7-9fda-b43e5a674b62">DomainController</a>


</td>
<td align="left" width="63%">
Name of the domain controller being used to perform site operations. This can be a DNS name or a NetBIOS name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cc1cb43b-2e18-45a7-9fda-b43e5a674b62">Forest</a>


</td>
<td align="left" width="63%">
Full DNS name of the forest in which the <b>GPMSitesContainer</b> object resides; this is the name of the forest root domain.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>
 

 

