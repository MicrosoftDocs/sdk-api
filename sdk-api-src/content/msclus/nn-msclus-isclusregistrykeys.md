---
UID: NN:msclus.ISClusRegistryKeys
title: ISClusRegistryKeys
author: windows-sdk-content
description: Represents the list of registry keys that are checkpointed for a resource.
old-location: mscs\clusregistrykeys_collection.htm
old-project: mscs
ms.assetid: 888f70d9-6562-4add-895d-604f22d75307
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusRegistryKeys, ClusRegistryKeys collection [Failover Cluster], ClusRegistryKeys collection [Failover Cluster],described, ISClusRegistryKeys, _wolf_clusregistrykeys_collection, msclus/ClusRegistryKeys, mscs.clusregistrykeys_collection
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
 - ClusRegistryKeys
 - ISClusRegistryKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusRegistryKeys interface


## -description


<p class="CCE_Message">[The 
    <b>ClusRegistryKeys</b> collection is available 
    for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Represents the list of registry keys that are 
    <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">checkpointed</a> for a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusRegistryKeys</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusRegistryKeys</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b28b848-ab26-4422-9e0e-a47613d7aa63">AddItem</a>
</td>
<td align="left" width="63%">
Adds an object to the 
     <b>ClusRegistryKeys</b> collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21206d22-ed84-49f9-878a-7376abaad642">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32b2eef7-40b1-4bfe-9f28-43831006d4cb">RemoveItem</a>
</td>
<td align="left" width="63%">
Deletes an object from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusRegistryKeys</b> collection has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a single object from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusRegistryKeys</b> collection:

<ul>
<li>Contains registry keys as strings.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/18bb4cfb-cd96-4f43-9cf6-ab06c22d0abf">ClusResource.RegistryKeys</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/386405da-1f57-46a2-b913-b946d7574ede">Property Management Objects</a>
 

 

