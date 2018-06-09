---
UID: NN:msclus.ISClusNetworkNetInterfaces
title: ISClusNetworkNetInterfaces
author: windows-sdk-content
description: Provides access to the network interfaces available to a network.
old-location: mscs\clusnetworknetinterfaces_collection.htm
old-project: MsCS
ms.assetid: 8b99f752-8aee-4c43-b49a-8ebaf20220f2
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusNetworkNetInterfaces, ClusNetworkNetInterfaces collection [Failover Cluster], ClusNetworkNetInterfaces collection [Failover Cluster],described, ISClusNetworkNetInterfaces, _wolf_clusnetworknetinterfaces_collection, msclus/ClusNetworkNetInterfaces, mscs.clusnetworknetinterfaces_collection
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
 - ClusNetworkNetInterfaces
 - ISClusNetworkNetInterfaces
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNetworkNetInterfaces interface


## -description


<p class="CCE_Message">[The 
    <b>ClusNetworkNetInterfaces</b> 
    collection is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Provides access to the 
    <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> available to a 
    <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">network</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNetworkNetInterfaces</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusNetworkNetInterfaces</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76c9915c-c419-492c-a843-740b6252c2d6">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNetworkNetInterfaces</b> collection has these properties.
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



A <b>ClusNetworkNetInterfaces</b> 
    collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/21aaf37d-5b60-4005-9e7f-f0435de590b2">ClusNetInterface</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/dbb51326-42a1-4b93-b7ab-a9b645c1ef8f">ClusNetwork.NetInterfaces</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/15f2813a-8abc-4d29-a17f-d80ddfd10032">Network Management Objects</a>
 

 

