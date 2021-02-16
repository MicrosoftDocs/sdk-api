---
UID: NF:mmc.IResultData.SetItem
title: IResultData::SetItem (mmc.h)
description: The IResultData::SetItem method enables the snap-in to set a single item in the result pane.
helpviewer_keywords: ["IResultData interface [MMC]","SetItem method","IResultData.SetItem","IResultData2 interface [MMC]","SetItem method","IResultData2::SetItem","IResultData::SetItem","SetItem","SetItem method [MMC]","SetItem method [MMC]","IResultData interface","SetItem method [MMC]","IResultData2 interface","_slate_iresultdata_setitem","mmc.iresultdata_setitem","mmc/IResultData2::SetItem","mmc/IResultData::SetItem"]
old-location: mmc\iresultdata_setitem.htm
tech.root: mmc
ms.assetid: d24ab645-aae2-4c0f-8fc5-05d028a724d4
ms.date: 12/05/2018
ms.keywords: IResultData interface [MMC],SetItem method, IResultData.SetItem, IResultData2 interface [MMC],SetItem method, IResultData2::SetItem, IResultData::SetItem, SetItem, SetItem method [MMC], SetItem method [MMC],IResultData interface, SetItem method [MMC],IResultData2 interface, _slate_iresultdata_setitem, mmc.iresultdata_setitem, mmc/IResultData2::SetItem, mmc/IResultData::SetItem
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
 - IResultData::SetItem
 - mmc/IResultData::SetItem
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
 - IResultData.SetItem
 - IResultData2.SetItem
---

# IResultData::SetItem


## -description

The <b>IResultData::SetItem</b> method enables the snap-in to set a single item in the result pane.

## -parameters

### -param item [in]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> structure that contains information about the item to be changed.

## -returns

This method can return one of these values.

## -remarks

The itemID member of the structure pointed to by the item parameter should be set to refer to the item or subitem to be changed in the list. The mask and all appropriate associated fields in the 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> structure should be filled out with the preferred changes. The nCol member should be set to 0 (zero) because it is the only column in which anything can be set or obtained. The str member of 
<b>RESULTDATAITEM</b> should always be set to MMC_CALLBACK.

This method does not support virtual lists.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-getitem">IResultData::GetItem</a>