---
UID: NN:mmc.IResultData2
title: IResultData2
author: windows-sdk-content
description: The IResultData2 interface supersedes the IResultData interface. The IResultData2 interface contains the IResultData2::RenameResultItem method, which allows a result node to programmatically be put in rename mode.
old-location: mmc\iresultdata2.htm
old-project: MMC
ms.assetid: cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IResultData2, IResultData2 interface [MMC], IResultData2 interface [MMC],described, _slate_iresultdata2, mmc.iresultdata2, mmc/IResultData2
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
 - IResultData2
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IResultData2 interface


## -description


The 
<b>IResultData2</b> interface supersedes the 
<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a> interface. The 
<b>IResultData2</b> interface contains the 
<a href="https://msdn.microsoft.com/a667f638-88bb-4758-8df7-478b0d6c18c4">IResultData2::RenameResultItem</a> method, which allows a result node to programmatically be put in rename mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultData2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IResultData2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IResultData2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07514672-2973-40f1-864a-066e256bd76a">DeleteAllRsltItems</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete all items.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0e6192a-2cc0-4a90-9793-e425879fcff2">DeleteItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete a single item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f26be5d5-9b7d-4cbd-b70c-431799c68e5e">FindItemByLParam</a>
</td>
<td align="left" width="63%">
Enables the snap-in to find an item or subitem based on a user-inserted value.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18c345b0-7d3c-4c80-8d1e-b8d5791bc550">GetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to retrieve a single item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1123fa48-969c-4208-83f2-e8ef4f72f0bb">GetNextItem</a>
</td>
<td align="left" width="63%">
Returns the <i>lParam</i> of the first item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6c9b3ef-3b12-42c1-9b3b-ad890b8bd05e">GetViewMode</a>
</td>
<td align="left" width="63%">
Enables the snap-in to retrieve the result view mode.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c354e718-ea9a-4d50-8a77-776500b86d25">InsertItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to insert a single item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7eb7a23-27e6-40f3-a2f3-139ad1d3cde0">ModifyItemState</a>
</td>
<td align="left" width="63%">
Enables the snap-in to modify the item's state.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f33a427c-6952-4877-bbfb-09ac976ea188">ModifyViewStyle</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the result view style.</p> (Inherited from IResultData)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a667f638-88bb-4758-8df7-478b0d6c18c4">RenameResultItem</a>
</td>
<td align="left" width="63%">
Allows a specified result item to be placed into rename mode.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5bde009-9f05-4ecb-9fbc-3ab211baa184">SetDescBarText</a>
</td>
<td align="left" width="63%">
Sets result view description bar text.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d24ab645-aae2-4c0f-8fc5-05d028a724d4">SetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set a single item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2105b19-3c91-4a5f-9dfa-c330d4733c67">SetItemCount</a>
</td>
<td align="left" width="63%">
Sets the number of items in a virtual list.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17cff5e6-9624-4873-baa8-96c05d877764">SetViewMode</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the result view mode.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">Sort</a>
</td>
<td align="left" width="63%">
Sorts all result items.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d335375-42b2-4f0a-a828-7ee636452db0">UpdateItem</a>
</td>
<td align="left" width="63%">
Redraws an item in the result pane after it has been changed.</p> (Inherited from IResultData)</td>
</tr>
</table> 

