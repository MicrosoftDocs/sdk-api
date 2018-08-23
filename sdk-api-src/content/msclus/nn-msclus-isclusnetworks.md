---
UID: NN:msclus.ISClusNetworks
title: ISClusNetworks
author: windows-sdk-content
description: Provides access to the networks in a cluster.
old-location: mscs\clusnetworks_collection.htm
old-project: mscs
ms.assetid: 7dba0985-16bc-4bda-9f37-275032c07811
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusNetworks, ClusNetworks collection [Failover Cluster], ClusNetworks collection [Failover Cluster],described, ISClusNetworks, _wolf_clusnetworks_collection, msclus/ClusNetworks, mscs.clusnetworks_collection
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
 - ClusNetworks
 - ISClusNetworks
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNetworks interface


## -description


<p class="CCE_Message">[The <b>ClusNetworks</b> collection 
    is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Provides access to the <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">networks</a> in a 
    <a href="c_gly.htm">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNetworks</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusNetworks</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ccd6e02-28b5-4490-9d7f-bfa3809d23db">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNetworks</b> collection has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c67ae910-a528-40e8-80a6-94c2d0574bbe">Count</a>


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

<a href="https://msdn.microsoft.com/da8248ab-70a2-4ca9-abf0-8aa3afe87298">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Returns a single network from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusNetworks</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/d51e9872-eb86-4b0e-b417-1a2e5ac6ee9c">ClusNetwork</a> objects.</li>
<li>Is obtained from <a href="https://msdn.microsoft.com/352f186d-bf42-480a-9554-c764345dafe6">Cluster.Networks</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8d4397e1-f24f-47b0-9037-e5a045337049">Cluster Management Objects</a>
 

 

