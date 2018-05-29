---
UID: NN:msclus.ISClusNetInterfaces
title: ISClusNetInterfaces
author: windows-sdk-content
description: Provides access to the network interfaces in a cluster.
old-location: mscs\clusnetinterfaces_collection.htm
old-project: MsCS
ms.assetid: 7d0dc4fd-733c-4a2a-9136-7dc0089b213d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusNetInterfaces, ClusNetInterfaces collection [Failover Cluster], ClusNetInterfaces collection [Failover Cluster],described, ISClusNetInterfaces, _wolf_clusnetinterfaces_collection, msclus/ClusNetInterfaces, mscs.clusnetinterfaces_collection
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
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	ClusNetInterfaces
-	ISClusNetInterfaces
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNetInterfaces interface


## -description


<p class="CCE_Message">[The 
    <b>ClusNetInterfaces</b> collection is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable 
    in subsequent versions.]

Provides access to the <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> in a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNetInterfaces</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusNetInterfaces</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8164c708-3889-4368-8112-62e8213e7fb7">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNetInterfaces</b> collection has these properties.
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
Returns a single network interface from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusNetInterfaces</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/21aaf37d-5b60-4005-9e7f-f0435de590b2">ClusNetInterface</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/f4fbac67-f196-4fd8-a678-8f7877e70f6a">Cluster.NetInterfaces</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8d4397e1-f24f-47b0-9037-e5a045337049">Cluster Management Objects</a>
 

 

