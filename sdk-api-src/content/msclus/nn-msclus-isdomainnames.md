---
UID: NN:msclus.ISDomainNames
title: ISDomainNames
author: windows-sdk-content
description: Provides access to the names of the domains on a network.
old-location: mscs\domainnames_collection.htm
old-project: mscs
ms.assetid: e7f806a7-02e7-41be-b8b9-60351180e748
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DomainNames, DomainNames collection [Failover Cluster], DomainNames collection [Failover Cluster],described, ISDomainNames, _wolf_domainnames_collection, msclus/DomainNames, mscs.domainnames_collection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msclus.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - DomainNames
 - ISDomainNames
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISDomainNames interface


## -description


<p class="CCE_Message">[The <b>DomainNames</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Provides access 
    to the names of the domains on a <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DomainNames</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>DomainNames</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ba8a5ba-0cb0-461e-8a42-968600bef6f2">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">DomainNames</b> collection has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a858642-3b74-4d06-a917-c6de272fb165">Count</a>


</td>
<td align="left" width="63%">
Returns the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/b4d57afc-82d1-4cdd-8347-da9053cafdcb">Item</a>


</td>
<td align="left" width="63%">
Returns a name of a domain from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>DomainNames</b> collection:

<ul>
<li>Contains domain names.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/418274eb-a366-4df8-af84-7e4ba8eeed5f">ClusApplication.DomainNames</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/37d11232-ef16-46c3-a914-1c0d358eca1a">Application Management Objects</a>
 

 

