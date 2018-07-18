---
UID: NN:mmc.IResultData
title: IResultData
author: windows-sdk-content
description: The IResultData interface enables a user to add, remove, find, and modify items associated with the result view pane. It also enables the manipulation of the view style of the result view pane.
old-location: mmc\iresultdata.htm
old-project: MMC
ms.assetid: 58f8bcdb-b062-4048-92fc-eb652ce62c5b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IResultData, IResultData interface [MMC], IResultData interface [MMC],described, _slate_iresultdata, mmc.iresultdata, mmc/IResultData
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
 - Mmcndmgr.dll
api_name:
 - IResultData
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultData</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResultData</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/07514672-2973-40f1-864a-066e256bd76a">DeleteAllRsltItems</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete all items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0e6192a-2cc0-4a90-9793-e425879fcff2">DeleteItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete a single item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f26be5d5-9b7d-4cbd-b70c-431799c68e5e">FindItemByLParam</a>
</td>
<td align="left" width="63%">
Enables the snap-in to find an item or subitem based on a user-inserted value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18c345b0-7d3c-4c80-8d1e-b8d5791bc550">GetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to retrieve a single item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1123fa48-969c-4208-83f2-e8ef4f72f0bb">GetNextItem</a>
</td>
<td align="left" width="63%">
Returns the <i>lParam</i> of the first item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6c9b3ef-3b12-42c1-9b3b-ad890b8bd05e">GetViewMode</a>
</td>
<td align="left" width="63%">
Enables the snap-in to retrieve the result view mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c354e718-ea9a-4d50-8a77-776500b86d25">InsertItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to insert a single item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7eb7a23-27e6-40f3-a2f3-139ad1d3cde0">ModifyItemState</a>
</td>
<td align="left" width="63%">
Enables the snap-in to modify the item's state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f33a427c-6952-4877-bbfb-09ac976ea188">ModifyViewStyle</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the result view style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5bde009-9f05-4ecb-9fbc-3ab211baa184">SetDescBarText</a>
</td>
<td align="left" width="63%">
Sets result view description bar text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d24ab645-aae2-4c0f-8fc5-05d028a724d4">SetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set a single item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2105b19-3c91-4a5f-9dfa-c330d4733c67">SetItemCount</a>
</td>
<td align="left" width="63%">
Sets the number of items in a virtual list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17cff5e6-9624-4873-baa8-96c05d877764">SetViewMode</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the result view mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">Sort</a>
</td>
<td align="left" width="63%">
Sorts all result items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d335375-42b2-4f0a-a828-7ee636452db0">UpdateItem</a>
</td>
<td align="left" width="63%">
Redraws an item in the result pane after it has been changed.

</td>
</tr>
</table> 

