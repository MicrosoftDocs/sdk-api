---
UID: NN:msclus.ISClusResGroupResources
title: ISClusResGroupResources
author: windows-driver-content
description: Provides access to the resources that are current members of a group and allows a resource to be added to or deleted from the group.
old-location: mscs\clusresgroupresources_collection.htm
old-project: MsCS
ms.assetid: 9ea90beb-86ae-4026-94bb-175e593da8fa
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: ClusResGroupResources, ClusResGroupResources collection [Failover Cluster], ClusResGroupResources collection [Failover Cluster],described, ISClusResGroupResources, _wolf_clusresgroupresources_collection, msclus/ClusResGroupResources, mscs.clusresgroupresources_collection
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
-	ClusResGroupResources
-	ISClusResGroupResources
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResGroupResources interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResGroupResources</b> collection is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Provides access to the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> that are 
    current members of a <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">group</a> and allows a resource to be added to or 
    deleted from the group.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResGroupResources</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResGroupResources</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/609e3016-b14d-4a64-b86b-15796444a9d9">CreateItem</a>
</td>
<td align="left" width="63%">
Creates a new cluster resource and adds it to the group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfd908a3-b968-4729-8ca4-feb687108249">DeleteItem</a>
</td>
<td align="left" width="63%">
Removes a resource from the group and deletes it from the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/033cfe27-d4f4-427f-9e55-ace18d8b318c">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResGroupResources</b> collection has these properties.
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
Returns a single resource from the collection.

</td>
</tr>
</table> 


## -remarks



A <b>ClusResGroupResources</b> collection:

<ul>
<li>Contains <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> objects.</li>
<li>Is obtained from 
      <a href="https://msdn.microsoft.com/891a2126-774d-43c6-bd27-6a0e9d943383">ClusResGroup.Resources</a>.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/415eecde-4057-4efe-aeae-2066e4b6c46a">Group Management Objects</a>
 

 

