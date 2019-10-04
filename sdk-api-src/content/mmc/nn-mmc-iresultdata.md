---
UID: NN:mmc.IResultData
title: IResultData (mmc.h)
author: windows-sdk-content
description: The IResultData interface enables a user to add, remove, find, and modify items associated with the result view pane. It also enables the manipulation of the view style of the result view pane.
old-location: mmc\iresultdata.htm
tech.root: mmc
ms.assetid: 58f8bcdb-b062-4048-92fc-eb652ce62c5b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IResultData, IResultData interface [MMC], IResultData interface [MMC],described, _slate_iresultdata, mmc.iresultdata, mmc/IResultData
ms.topic: interface
f1_keywords: 
 - "mmc/IResultData"
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IResultData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IResultData interface


## -description


The 
<b>IResultData</b> interface enables a user to add, remove, find, and modify items associated with the result view pane. It also enables the manipulation of the view style of the result view pane.

The 
<b>IResultData</b> interface was designed to give the impression that the result view pane would be used by only one component, but components should be aware that the result view pane can, in fact, be shared by several components. All item manipulations are performed through the use of an item ID assigned when the item is inserted. This ID is guaranteed to be both static and unique for the life of the item. When an item is deleted, the ID is freed and can be used by other new items in the list. You should never keep an item ID around after its associated item has been deleted.

The 
<b>IResultData</b> interface handles virtual (owner data) lists as well. Because of the nature of virtual lists, not all methods apply and some methods have limited functionality. These differences are detailed in the descriptions of individual methods. The primary difference in handling virtual lists it that because the console does not maintain any storage for virtual items, it does not provide item IDs. Instead virtual list items are identified by their list position (index).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultData</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResultData</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResultData</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-deleteallrsltitems">DeleteAllRsltItems</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete all items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-deleteitem">DeleteItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete a single item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-finditembylparam">FindItemByLParam</a>
</td>
<td align="left" width="63%">
Enables the snap-in to find an item or subitem based on a user-inserted value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to retrieve a single item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-getnextitem">GetNextItem</a>
</td>
<td align="left" width="63%">
Returns the <i>lParam</i> of the first item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-getviewmode">GetViewMode</a>
</td>
<td align="left" width="63%">
Enables the snap-in to retrieve the result view mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-insertitem">InsertItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to insert a single item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-modifyitemstate">ModifyItemState</a>
</td>
<td align="left" width="63%">
Enables the snap-in to modify the item's state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-modifyviewstyle">ModifyViewStyle</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the result view style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setdescbartext">SetDescBarText</a>
</td>
<td align="left" width="63%">
Sets result view description bar text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setitem">SetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set a single item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setitemcount">SetItemCount</a>
</td>
<td align="left" width="63%">
Sets the number of items in a virtual list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setviewmode">SetViewMode</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the result view mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-sort">Sort</a>
</td>
<td align="left" width="63%">
Sorts all result items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-updateitem">UpdateItem</a>
</td>
<td align="left" width="63%">
Redraws an item in the result pane after it has been changed.

</td>
</tr>
</table> 

