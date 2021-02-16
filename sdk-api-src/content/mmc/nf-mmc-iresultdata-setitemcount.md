---
UID: NF:mmc.IResultData.SetItemCount
title: IResultData::SetItemCount (mmc.h)
description: Sets the number of items in a virtual list.
helpviewer_keywords: ["IResultData interface [MMC]","SetItemCount method","IResultData.SetItemCount","IResultData2 interface [MMC]","SetItemCount method","IResultData2::SetItemCount","IResultData::SetItemCount","MMCLV_UPDATE_NOINVALIDATEALL","MMCLV_UPDATE_NOSCROLL","SetItemCount","SetItemCount method [MMC]","SetItemCount method [MMC]","IResultData interface","SetItemCount method [MMC]","IResultData2 interface","_slate_iresultdata_setitemcount","mmc.iresultdata_setitemcount","mmc/IResultData2::SetItemCount","mmc/IResultData::SetItemCount"]
old-location: mmc\iresultdata_setitemcount.htm
tech.root: mmc
ms.assetid: d2105b19-3c91-4a5f-9dfa-c330d4733c67
ms.date: 12/05/2018
ms.keywords: IResultData interface [MMC],SetItemCount method, IResultData.SetItemCount, IResultData2 interface [MMC],SetItemCount method, IResultData2::SetItemCount, IResultData::SetItemCount, MMCLV_UPDATE_NOINVALIDATEALL, MMCLV_UPDATE_NOSCROLL, SetItemCount, SetItemCount method [MMC], SetItemCount method [MMC],IResultData interface, SetItemCount method [MMC],IResultData2 interface, _slate_iresultdata_setitemcount, mmc.iresultdata_setitemcount, mmc/IResultData2::SetItemCount, mmc/IResultData::SetItemCount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IResultData::SetItemCount
 - mmc/IResultData::SetItemCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IResultData.SetItemCount
 - IResultData2.SetItemCount
---

# IResultData::SetItemCount


## -description

The <b>IResultData::SetItemCount</b> method sets the number of items in a virtual list.

## -parameters

### -param nItemCount [in]

The number of items that the control will contain.

### -param dwOptions [in]

Combination of the following flags:



#### MMCLV_UPDATE_NOINVALIDATEALL

Only repaint items added or removed at the bottom of the result pane. Set this flag only if items are removed or added at the bottom of the list.



#### MMCLV_UPDATE_NOSCROLL

Do not adjust the scroll bar on changed item count.

## -returns

This method can return one of these values.

## -remarks

The primary purpose of the 
SetItemCount method is to populate virtual lists. Because items are not actually added to a virtual list, this is the way to notify the list how many virtual items exist.

<div class="alert"><b>Note</b>  Do not set the MMCLV_UPDATE_NOINVALIDATEALL flag when items are added or removed from the middle of the list; that is, when reindexing of the existing items is required. If you add or remove items in the middle of the list, setting the flag produces an incorrect update of the list.</div>
<div> </div>
The MMCLV_UPDATE_NOINVALIDATEALL flag should be used in cases where you are only adding and deleting from the end of the virtual list and you want to reduce the amount of redrawing. If you set this flag, MMC only calls <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo">IComponent::GetDisplayInfo</a> on new items added to the result pane. Setting the flag tells MMC that none of the items are being renumbered. MMC redraws only the visible items that were added or deleted.

SetItemCount can be called for nonvirtual lists as well, but for a different purpose. When called for a nonvirtual list, 
SetItemCount preallocates memory for the specified number of items. When adding a large number of items, this improves performance by reducing the number of memory allocation calls the list must do.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultownerdata">IResultOwnerData</a>