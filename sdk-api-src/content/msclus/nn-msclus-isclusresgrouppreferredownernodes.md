---
UID: NN:msclus.ISClusResGroupPreferredOwnerNodes
title: ISClusResGroupPreferredOwnerNodes
author: windows-driver-content
description: Provides access to the nodes that belong to the preferred owner list for a group.
old-location: mscs\clusresgrouppreferredownernodes_collection.htm
old-project: MsCS
ms.assetid: 3425825e-890c-4d3d-919e-a66963e1fc55
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ClusResGroupPreferredOwnerNodes, ClusResGroupPreferredOwnerNodes collection [Failover Cluster], ClusResGroupPreferredOwnerNodes collection [Failover Cluster],described, ISClusResGroupPreferredOwnerNodes, _wolf_clusresgrouppreferredownernodes_collection, msclus/ClusResGroupPreferredOwnerNodes, mscs.clusresgrouppreferredownernodes_collection
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
-	ClusResGroupPreferredOwnerNodes
-	ISClusResGroupPreferredOwnerNodes
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroupPreferredOwnerNodes interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResGroupPreferredOwnerNodes</b> 
    collection is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Provides access to the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> that belong to the 
    <a href="p_gly.htm">preferred owner</a> list for a 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResGroupPreferredOwnerNodes</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResGroupPreferredOwnerNodes</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/001e2766-d489-4406-b11e-c19c6426dfd4">AddItem</a>
</td>
<td align="left" width="63%">
Adds a node to the preferred owners list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae234397-a592-41a3-a30d-cb4b6450e332">InsertItem</a>
</td>
<td align="left" width="63%">
Adds a node to the preferred owners list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05085f9c-776c-4dc9-8c48-8157eeec6280">Refresh</a>
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
Removes a node from preferred owners list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a345174f-be29-41bf-bb0a-398d9719f55f">SaveChanges</a>
</td>
<td align="left" width="63%">
Saves the list of preferred owner nodes to the 
     <a href="https://msdn.microsoft.com/d2c1a9c0-7e87-4a3c-9a1a-7f1756f97804">cluster database</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResGroupPreferredOwnerNodes</b> collection has these properties.
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
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/05a5f903-ea0d-4058-9806-3d9a9ef38e15">Modified</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Reports whether any of the nodes in the collection have changed.

</td>
</tr>
</table> 


## -remarks



A 
    <b>ClusResGroupPreferredOwnerNodes</b> 
    collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/5e2872a4-72db-4cd8-9fce-34c1bd701706">ClusResGroup.PreferredOwnerNodes</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/415eecde-4057-4efe-aeae-2066e4b6c46a">Group Management Objects</a>
 

 

