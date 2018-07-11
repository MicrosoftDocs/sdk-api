---
UID: NN:msclus.ISClusResTypePossibleOwnerNodes
title: ISClusResTypePossibleOwnerNodes
author: windows-sdk-content
description: Provides access to the possible owner nodes of a resource type.
old-location: mscs\clusrestypepossibleownernodes_collection.htm
old-project: mscs
ms.assetid: be22d5b1-8c61-40a5-883c-f49651ba623d
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: ClusResTypePossibleOwnerNodes, ClusResTypePossibleOwnerNodes collection [Failover Cluster], ClusResTypePossibleOwnerNodes collection [Failover Cluster],described, ISClusResTypePossibleOwnerNodes, _wolf_clusrestypepossibleownernodes_collection, msclus/ClusResTypePossibleOwnerNodes, mscs.clusrestypepossibleownernodes_collection
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
 - ClusResTypePossibleOwnerNodes
 - ISClusResTypePossibleOwnerNodes
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResTypePossibleOwnerNodes interface


## -description


<p class="CCE_Message">[The 
    <b>ClusResTypePossibleOwnerNodes</b> 
    collection is available for 
    use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent 
    versions.]

Provides access to the <a href="https://msdn.microsoft.com/library/ms682858(v=VS.85).aspx">possible owner</a>
<a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> of a 
    <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource type</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResTypePossibleOwnerNodes</b> collection has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusResTypePossibleOwnerNodes</b> collection has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7e8f244-8265-4000-8c83-1ce4f6c0998f">Refresh</a>
</td>
<td align="left" width="63%">
Refreshes the data in the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusResTypePossibleOwnerNodes</b> collection has these properties.
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
Returns the number of objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Returns a single node from the collection.

</td>
</tr>
</table> 


## -remarks



A <a href="https://msdn.microsoft.com/a3269288-f32f-45d5-8fd4-4e6fb257c1be">ClusResPossibleOwnerNodes</a> 
    collection contains <a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a> objects. It is obtained 
    from 
    <a href="https://msdn.microsoft.com/9437a940-bb61-4de1-9d4b-54876161e02c">ClusResType.PossibleOwnerNodes</a>.




## -see-also




<a href="https://msdn.microsoft.com/91aece2b-c47c-4e62-9aac-d546977d4848">Resource Type Management Objects</a>
 

 

