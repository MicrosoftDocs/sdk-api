---
UID: NN:mmc.IResultOwnerData
title: IResultOwnerData
author: windows-sdk-content
description: The IResultOwnerData interface supports the use of virtual lists, which are list-view controls that have the LVS_OWNERDATA style set.
old-location: mmc\iresultownerdata.htm
old-project: MMC
ms.assetid: 184f3783-9000-45aa-867b-580800b560b3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IResultOwnerData, IResultOwnerData interface [MMC], IResultOwnerData interface [MMC],described, _slate_iresultownerdata, mmc.iresultownerdata, mmc/IResultOwnerData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IResultOwnerData
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IResultOwnerData interface


## -description


The 
<b>IResultOwnerData</b> interface supports the use of virtual lists, which are list-view controls that have the LVS_OWNERDATA style set. The methods of this interface are applicable only to virtual lists. This is an optional interface and snap-ins can implement it for enhanced virtual list performance and functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultOwnerData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResultOwnerData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResultOwnerData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d63e5d7-f342-409a-abea-0305129ba060">CacheHint</a>
</td>
<td align="left" width="63%">
Allows the snap-in to collect the display information for a range of items ahead of time in cases where an optimization can be made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/839e6038-3f47-4192-b717-d81e4d9f202d">FindItem</a>
</td>
<td align="left" width="63%">
Finds result items matching the specified string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5326e935-cb6c-4f76-8c9b-87d910dbbb0d">SortItems</a>
</td>
<td align="left" width="63%">
Sorts the items in a virtual list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8143d11c-3740-4ffc-88f0-6df779c50521">IComponent::GetDisplayInfo</a>



<a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">IComponent::GetResultViewType</a>



<a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">IComponent::QueryDataObject</a>



<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/d2105b19-3c91-4a5f-9dfa-c330d4733c67">IResultData::SetItemCount</a>



<a href="https://msdn.microsoft.com/f02a4045-977a-4e52-93bd-7defa4fd1d89">Owner Data/Virtual Lists</a>



<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a>
 

 

