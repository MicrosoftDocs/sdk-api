---
UID: NF:mmc.IResultData.UpdateItem
title: IResultData::UpdateItem (mmc.h)
description: Causes a specified item in the result pane to be redrawn.
helpviewer_keywords: ["IResultData interface [MMC]","UpdateItem method","IResultData.UpdateItem","IResultData2 interface [MMC]","UpdateItem method","IResultData2::UpdateItem","IResultData::UpdateItem","UpdateItem","UpdateItem method [MMC]","UpdateItem method [MMC]","IResultData interface","UpdateItem method [MMC]","IResultData2 interface","_slate_iresultdata_updateitem","mmc.iresultdata_updateitem","mmc/IResultData2::UpdateItem","mmc/IResultData::UpdateItem"]
old-location: mmc\iresultdata_updateitem.htm
tech.root: mmc
ms.assetid: 6d335375-42b2-4f0a-a828-7ee636452db0
ms.date: 12/05/2018
ms.keywords: IResultData interface [MMC],UpdateItem method, IResultData.UpdateItem, IResultData2 interface [MMC],UpdateItem method, IResultData2::UpdateItem, IResultData::UpdateItem, UpdateItem, UpdateItem method [MMC], UpdateItem method [MMC],IResultData interface, UpdateItem method [MMC],IResultData2 interface, _slate_iresultdata_updateitem, mmc.iresultdata_updateitem, mmc/IResultData2::UpdateItem, mmc/IResultData::UpdateItem
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
 - IResultData::UpdateItem
 - mmc/IResultData::UpdateItem
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
 - IResultData.UpdateItem
 - IResultData2.UpdateItem
---

# IResultData::UpdateItem


## -description

The <b>IResultData::UpdateItem</b> method causes a specified item in the result pane to be redrawn.

## -parameters

### -param itemID [in]

A value that specifies the unique identifier of the item to be redrawn in the result pane. When applied to virtual lists, pass the item index instead of the itemID.

## -returns

This method can return one of these values.

## -remarks

UpdateItem would typically be used to update a displayed item after changes were made to it by the user.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>