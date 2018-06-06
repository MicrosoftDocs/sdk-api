---
UID: NN:msclus.ISClusResDependencies
title: ISClusResDependencies
author: windows-sdk-content
description: Provides access to the dependencies of a resource.
old-location: mscs\clusresdependencies_collection.htm
old-project: MsCS
ms.assetid: 10695840-38ec-4614-8bbd-5772a53dea4b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusResDependencies, ClusResDependencies collection [Failover Cluster], ClusResDependencies collection [Failover Cluster],described, ISClusResDependencies, _wolf_clusresdependencies_collection, msclus/ClusResDependencies, mscs.clusresdependencies_collection
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
 - ClusResDependencies
 - ISClusResDependencies
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResDependencies interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResDependencies</b> collection is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Provides access to the <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> of a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. Resources added to a 
    <b>ClusResDependencies</b> collection become 
    dependencies of the resource from which the collection was obtained.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResDependencies</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResDependencies</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8462df8-dece-423f-a585-5774411401c8">AddItem</a>
</td>
<td align="left" width="63%">
Adds an existing <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> resource to the dependency 
     collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/609e3016-b14d-4a64-b86b-15796444a9d9">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new resource in the cluster and adds it to the dependency collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfd908a3-b968-4729-8ca4-feb687108249">DeleteItem</a>
</td>
<td align="left" width="63%">
Removes a resource from the dependency collection and deletes the resource from the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96a958b4-99f6-4739-ac7b-01c147c8e4d8">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/904556e2-7d0b-4c03-8cf5-795342263045">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes a dependency from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResDependencies</b> collection has these properties.
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
Returns the number of dependencies in the collection.

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
Returns a single dependency from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResDependencies</b> 
    collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/33539a29-1533-44fa-853d-9d4f1b3f1cca">ClusResource.Dependencies</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/fa3a5042-8bb5-4ece-825c-40d7df584b35">Resource Management Objects</a>
 

 

