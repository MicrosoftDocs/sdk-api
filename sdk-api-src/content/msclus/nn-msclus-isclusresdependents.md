---
UID: NN:msclus.ISClusResDependents
title: ISClusResDependents
author: windows-driver-content
description: Provides access to the dependents of a resource.
old-location: mscs\clusresdependents_collection.htm
old-project: MsCS
ms.assetid: 4e1f47fa-e240-4fdb-b736-9b2e64828eb0
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ClusResDependents, ClusResDependents collection [Failover Cluster], ClusResDependents collection [Failover Cluster],described, ISClusResDependents, _wolf_clusresdependents_collection, msclus/ClusResDependents, mscs.clusresdependents_collection
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
-	ClusResDependents
-	ISClusResDependents
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResDependents interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResDependents</b> collection is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Provides access to the <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependents</a> of a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. Resources added to a 
    <b>ClusResDependents</b> collection become 
    dependents of the resource from which the collection was obtained.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResDependents</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResDependents</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f640b526-163d-4975-b135-6734569bf29a">AddItem</a>
</td>
<td align="left" width="63%">
Adds an existing <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> resource to the 
     collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/609e3016-b14d-4a64-b86b-15796444a9d9">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new resource in the cluster and adds it to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfd908a3-b968-4729-8ca4-feb687108249">DeleteItem</a>
</td>
<td align="left" width="63%">
Removes a resource from the collection and deletes the resource from the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6335e861-26f4-4fa5-89f9-650bbd6d7047">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70cee9b9-4d21-4237-8262-211e1b87923f">RemoveItem</a>
</td>
<td align="left" width="63%">
Removes a resource from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResDependents</b> collection has these properties.
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
Returns the number of dependents in the collection.

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
Returns a single resource from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResDependents</b> 
    collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/33539a29-1533-44fa-853d-9d4f1b3f1cca">ClusResource.Dependencies</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/fa3a5042-8bb5-4ece-825c-40d7df584b35">Resource Management Objects</a>
 

 

