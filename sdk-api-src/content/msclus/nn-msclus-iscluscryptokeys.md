---
UID: NN:msclus.ISClusCryptoKeys
title: ISClusCryptoKeys
author: windows-sdk-content
description: Provides access to the checkpointed crypto keys of a resource.
old-location: mscs\cluscryptokeys_collection.htm
old-project: mscs
ms.assetid: 0078ba7a-24d7-4de6-af05-f1a03d9deb0a
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusCryptoKeys, ClusCryptoKeys collection [Failover Cluster], ClusCryptoKeys collection [Failover Cluster],described, ISClusCryptoKeys, _wolf_cluscryptokeys_collection, msclus/ClusCryptoKeys, mscs.cluscryptokeys_collection
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
 - ClusCryptoKeys
 - ISClusCryptoKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusCryptoKeys interface


## -description


<p class="CCE_Message">[The 
    <b>ClusCryptoKeys</b> collection is available for 
    use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Provides access to the <a href="https://msdn.microsoft.com/6031fe2b-d5cb-477e-9d0f-c8c4a14ce02b">checkpointed</a> crypto keys of 
    a resource. Crypto keys are created using the Crypto API. Checkpointed keys are moved to the resource's 
    new host <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> during 
    <a href="https://msdn.microsoft.com/6722d075-02e0-4817-abc3-dce8951c17da">failover</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusCryptoKeys</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusCryptoKeys</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f830e93-fa0a-4dbe-9544-9065cb2b4e8d">AddItem</a>
</td>
<td align="left" width="63%">
Adds an object to the <b>ClusCryptoKeys</b> 
     collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5b0dcd1-c2c4-4867-b532-93f6337804e6">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffaf36c7-86d2-4368-8c8f-f0b58a38fceb">RemoveItem</a>
</td>
<td align="left" width="63%">
Deletes an object from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusCryptoKeys</b> collection has these properties.
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



A <b>ClusCryptoKeys</b> collection:

<ul>
<li>Contains crypto keys (registry keys) as strings.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/14f75dc0-6d6e-4b70-9481-d00132f2b87b">ClusResource.CryptoKeys</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/386405da-1f57-46a2-b913-b946d7574ede">Property Management Objects</a>
 

 

