---
UID: NN:mmc.IResultOwnerData
title: IResultOwnerData (mmc.h)
description: The IResultOwnerData interface supports the use of virtual lists, which are list-view controls that have the LVS_OWNERDATA style set.
old-location: mmc\iresultownerdata.htm
tech.root: mmc
ms.assetid: 184f3783-9000-45aa-867b-580800b560b3
ms.date: 12/05/2018
ms.keywords: IResultOwnerData, IResultOwnerData interface [MMC], IResultOwnerData interface [MMC],described, _slate_iresultownerdata, mmc.iresultownerdata, mmc/IResultOwnerData
f1_keywords:
- mmc/IResultOwnerData
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmc.h
api_name:
- IResultOwnerData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IResultOwnerData interface


## -description


The 
<b>IResultOwnerData</b> interface supports the use of virtual lists, which are list-view controls that have the LVS_OWNERDATA style set. The methods of this interface are applicable only to virtual lists. This is an optional interface and snap-ins can implement it for enhanced virtual list performance and functionality.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultOwnerData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResultOwnerData</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultownerdata-cachehint">CacheHint</a>
</td>
<td align="left" width="63%">
Allows the snap-in to collect the display information for a range of items ahead of time in cases where an optimization can be made.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultownerdata-finditem">FindItem</a>
</td>
<td align="left" width="63%">
Finds result items matching the specified string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultownerdata-sortitems">SortItems</a>
</td>
<td align="left" width="63%">
Sorts the items in a virtual list.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo">IComponent::GetDisplayInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setitemcount">IResultData::SetItemCount</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/owner-data-virtual-lists">Owner Data/Virtual Lists</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a>
 

 

