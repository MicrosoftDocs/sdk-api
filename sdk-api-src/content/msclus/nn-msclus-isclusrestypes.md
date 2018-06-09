---
UID: NN:msclus.ISClusResTypes
title: ISClusResTypes
author: windows-sdk-content
description: Provides access to the resource types in a cluster.
old-location: mscs\clusrestypes_collection.htm
old-project: MsCS
ms.assetid: 614d3ed6-255f-46ed-9354-7a73a21cac87
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusResTypes, ClusResTypes collection [Failover Cluster], ClusResTypes collection [Failover Cluster],described, ISClusResTypes, _wolf_clusrestypes_collection, msclus/ClusResTypes, mscs.clusrestypes_collection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msclus.h
req.include-header: 
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
 - ClusResTypes
 - ISClusResTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResTypes interface


## -description


<p class="CCE_Message">[The <b>ClusResTypes</b> 
    collection is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Provides 
    access to the <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource types</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResTypes</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResTypes</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7fc79b1-1803-4060-bf1f-39a253bccab6">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new resource type in the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a528b4e-8d6d-434b-b005-ca732c72c7a3">DeleteItem</a>
</td>
<td align="left" width="63%">
Deletes a resource type from the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d85c3506-5da7-46c8-8458-0ee0ef47a0e7">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResTypes</b> collection has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Returns the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Returns a single resource type from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResTypes</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/e4ad6364-f318-47f9-a276-d99c91ffbbb5">ClusResType</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/73a9ca85-0da2-4978-965a-47bdee4ded6c">Cluster.ResourceTypes</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8d4397e1-f24f-47b0-9037-e5a045337049">Cluster Management Objects</a>
 

 

