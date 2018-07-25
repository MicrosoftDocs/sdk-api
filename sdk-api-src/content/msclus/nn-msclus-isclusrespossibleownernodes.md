---
UID: NN:msclus.ISClusResPossibleOwnerNodes
title: ISClusResPossibleOwnerNodes
author: windows-sdk-content
description: Provides access to a resource's list of possible owner &#32; nodes.
old-location: mscs\clusrespossibleownernodes_collection.htm
old-project: mscs
ms.assetid: a3269288-f32f-45d5-8fd4-4e6fb257c1be
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusResPossibleOwnerNodes, ClusResPossibleOwnerNodes collection [Failover Cluster], ClusResPossibleOwnerNodes collection [Failover Cluster],described, ISClusResPossibleOwnerNodes, _wolf_clusrespossibleownernodes_collection, msclus/ClusResPossibleOwnerNodes, mscs.clusrespossibleownernodes_collection
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
 - ClusResPossibleOwnerNodes
 - ISClusResPossibleOwnerNodes
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResPossibleOwnerNodes interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResPossibleOwnerNodes</b> 
    collection is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Provides access to a resource's list of 
    <a href="https://msdn.microsoft.com/library/ms682858(v=VS.85).aspx">possible owner</a>
<a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResPossibleOwnerNodes</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResPossibleOwnerNodes</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35d5eda5-09b6-4379-847a-dbb35f59f565">AddItem</a>
</td>
<td align="left" width="63%">
Adds a node to the list of possible owners of a 
     <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99ca2887-1e8b-4fe7-92fa-1d498d38a421">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9126b3ae-4dd3-402a-bda9-ce2d3ded8b36">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes a node from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResPossibleOwnerNodes</b> collection has these properties.
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
Returns the number of nodes in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Returns a single node from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/05a5f903-ea0d-4058-9806-3d9a9ef38e15">Modified</a>


</td>
<td align="left" width="63%">
Reports whether the collection has been modified since instantiation.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResPossibleOwnerNodes</b> 
    collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/591b0508-f963-4c62-afb8-1c9224299cc0">ClusResource.PossibleOwnerNodes</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/fa3a5042-8bb5-4ece-825c-40d7df584b35">Resource Management Objects</a>
 

 

