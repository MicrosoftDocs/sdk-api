---
UID: NN:msclus.ISClusterNames
title: ISClusterNames
author: windows-sdk-content
description: Provides access to the names of the clusters in a domain.
old-location: mscs\clusternames_collection.htm
old-project: mscs
ms.assetid: c4e29498-c4e2-4351-8eed-05bc73437485
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusterNames, ClusterNames collection [Failover Cluster], ClusterNames collection [Failover Cluster],described, ISClusterNames, _wolf_clusternames_collection, msclus/ClusterNames, mscs.clusternames_collection
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
 - ClusterNames
 - ISClusterNames
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusterNames interface


## -description


<p class="CCE_Message">[The <b>ClusterNames</b> 
    collection is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Provides access 
    to the names of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922622">clusters</a> in a domain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusterNames</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusterNames</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4f71465-3573-4525-b37a-5b8aa22a84ec">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusterNames</b> collection has these properties.
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
Returns the number of clusters in the domain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915304">DomainName</a>


</td>
<td align="left" width="63%">
Returns the name of the domain that is the source of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Returns a name of a cluster from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusterNames</b> collection:

<ul>
<li>Contains cluster names.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/5c4d64e1-d8cb-4abb-b157-3ecdf02a6219">ClusApplication.ClusterNames</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/37d11232-ef16-46c3-a914-1c0d358eca1a">Application Management Objects</a>
 

 

