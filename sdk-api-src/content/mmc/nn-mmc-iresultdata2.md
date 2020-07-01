---
UID: NN:mmc.IResultData2
title: IResultData2 (mmc.h)
description: The IResultData2 interface supersedes the IResultData interface. The IResultData2 interface contains the IResultData2::RenameResultItem method, which allows a result node to programmatically be put in rename mode.
helpviewer_keywords: ["IResultData2","IResultData2 interface [MMC]","IResultData2 interface [MMC]","described","_slate_iresultdata2","mmc.iresultdata2","mmc/IResultData2"]
old-location: mmc\iresultdata2.htm
tech.root: mmc
ms.assetid: cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05
ms.date: 12/05/2018
ms.keywords: IResultData2, IResultData2 interface [MMC], IResultData2 interface [MMC],described, _slate_iresultdata2, mmc.iresultdata2, mmc/IResultData2
f1_keywords:
- mmc/IResultData2
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
req.lib: Mmc.lib
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
- IResultData2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IResultData2 interface


## -description


The 
<b>IResultData2</b> interface supersedes the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a> interface. The 
<b>IResultData2</b> interface contains the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata2-renameresultitem">IResultData2::RenameResultItem</a> method, which allows a result node to programmatically be put in rename mode.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IResultData2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IResultData2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-deleteallrsltitems">DeleteAllRsltItems</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete all items.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-deleteitem">DeleteItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to delete a single item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-finditembylparam">FindItemByLParam</a>
</td>
<td align="left" width="63%">
Enables the snap-in to find an item or subitem based on a user-inserted value.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-getitem">GetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to retrieve a single item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-getnextitem">GetNextItem</a>
</td>
<td align="left" width="63%">
Returns the <i>lParam</i> of the first item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-getviewmode">GetViewMode</a>
</td>
<td align="left" width="63%">
Enables the snap-in to retrieve the result view mode.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-insertitem">InsertItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to insert a single item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-modifyitemstate">ModifyItemState</a>
</td>
<td align="left" width="63%">
Enables the snap-in to modify the item's state.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-modifyviewstyle">ModifyViewStyle</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the result view style.</p> (Inherited from IResultData)</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata2-renameresultitem">RenameResultItem</a>
</td>
<td align="left" width="63%">
Allows a specified result item to be placed into rename mode.

</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setdescbartext">SetDescBarText</a>
</td>
<td align="left" width="63%">
Sets result view description bar text.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setitem">SetItem</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set a single item.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setitemcount">SetItemCount</a>
</td>
<td align="left" width="63%">
Sets the number of items in a virtual list.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-setviewmode">SetViewMode</a>
</td>
<td align="left" width="63%">
Enables the snap-in to set the result view mode.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-sort">Sort</a>
</td>
<td align="left" width="63%">
Sorts all result items.</p> (Inherited from IResultData)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-updateitem">UpdateItem</a>
</td>
<td align="left" width="63%">
Redraws an item in the result pane after it has been changed.</p> (Inherited from IResultData)</td>
</tr>
</table> 

