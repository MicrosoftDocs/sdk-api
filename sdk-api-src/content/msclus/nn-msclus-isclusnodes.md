---
UID: NN:msclus.ISClusNodes
title: ISClusNodes
author: windows-driver-content
description: Provides access to the nodes in a cluster.
old-location: mscs\clusnodes_collection.htm
old-project: MsCS
ms.assetid: f35d610f-014a-48cf-aaa4-93e320bcd890
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ClusNodes, ClusNodes collection [Failover Cluster], ClusNodes collection [Failover Cluster],described, ISClusNodes, _wolf_clusnodes_collection, msclus/ClusNodes, mscs.clusnodes_collection
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	ClusNodes
-	ISClusNodes
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNodes interface


## -description


<p class="CCE_Message">[The <b>ClusNodes</b> 
    collection is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Provides 
    access to the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNodes</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusNodes</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c488584-344e-4ab4-8abe-c1da9b7ffaea">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNodes</b> collection has these properties.
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
Returns a single node from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusNodes</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> objects.</li>
<li>Is obtained from <a href="https://msdn.microsoft.com/690c9635-114f-4109-a9b9-4ebb1961c58b">Cluster.Nodes</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8d4397e1-f24f-47b0-9037-e5a045337049">Cluster Management Objects</a>
 

 

