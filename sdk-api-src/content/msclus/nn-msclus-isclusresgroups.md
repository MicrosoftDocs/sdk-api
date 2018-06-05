---
UID: NN:msclus.ISClusResGroups
title: ISClusResGroups
author: windows-sdk-content
description: Provides access to all cluster groups belonging either to a cluster or to a particular node in a cluster.
old-location: mscs\clusresgroups_collection.htm
old-project: MsCS
ms.assetid: 7411d5f9-15c0-4c03-9128-c6b636979a50
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ClusResGroups, ClusResGroups collection [Failover Cluster], ClusResGroups collection [Failover Cluster],described, ISClusResGroups, _wolf_clusresgroups_collection, msclus/ClusResGroups, mscs.clusresgroups_collection
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	ClusResGroups
-	ISClusResGroups
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroups interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResGroups</b> collection is available for 
    use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Provides access to all cluster <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> belonging either to 
    a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> or to a particular 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> in a cluster.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResGroups</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResGroups</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b43a7d4-db08-402d-9910-464ba3ea8d18">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new group and adds it to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/907364e7-cf9d-49f6-9c98-d16f6058ce5f">DeleteItem</a>
</td>
<td align="left" width="63%">
Deletes a group from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09945337-86b7-495f-9f34-90efb238629a">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResGroups</b> collection has these properties.
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
Returns a single group from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResGroups</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/cd0e8510-4eb0-45fe-819e-f40fe4bfa4e7">ClusResGroup</a> objects.</li>
<li>Is obtained from <a href="https://msdn.microsoft.com/449e4432-571c-403c-81c7-da50f455224c">Cluster.ResourceGroups</a> 
      or <a href="https://msdn.microsoft.com/45eae46b-54d2-4945-aab1-8b471df64881">ClusNode.ResourceGroups</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8d4397e1-f24f-47b0-9037-e5a045337049">Cluster Management Objects</a>
 

 

