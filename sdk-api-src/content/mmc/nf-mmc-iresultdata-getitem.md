---
UID: NF:mmc.IResultData.GetItem
title: IResultData::GetItem (mmc.h)
description: Enables a user to retrieve the parameters of a single item.
helpviewer_keywords: ["GetItem","GetItem method [MMC]","GetItem method [MMC]","IResultData interface","GetItem method [MMC]","IResultData2 interface","IResultData interface [MMC]","GetItem method","IResultData.GetItem","IResultData2 interface [MMC]","GetItem method","IResultData2::GetItem","IResultData::GetItem","_slate_iresultdata_getitem","mmc.iresultdata_getitem","mmc/IResultData2::GetItem","mmc/IResultData::GetItem"]
old-location: mmc\iresultdata_getitem.htm
tech.root: mmc
ms.assetid: 18c345b0-7d3c-4c80-8d1e-b8d5791bc550
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [MMC], GetItem method [MMC],IResultData interface, GetItem method [MMC],IResultData2 interface, IResultData interface [MMC],GetItem method, IResultData.GetItem, IResultData2 interface [MMC],GetItem method, IResultData2::GetItem, IResultData::GetItem, _slate_iresultdata_getitem, mmc.iresultdata_getitem, mmc/IResultData2::GetItem, mmc/IResultData::GetItem
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
 - IResultData::GetItem
 - mmc/IResultData::GetItem
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
 - IResultData.GetItem
 - IResultData2.GetItem
---

# IResultData::GetItem


## -description

The <b>IResultData::GetItem</b> method enables a user to retrieve the parameters of a single item.

## -parameters

### -param item [in, out]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> structure that contains information about the item whose parameters are being retrieved.

## -returns

This method can return one of these values.

## -remarks

The itemID member of the 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> structure pointed to by the item parameter should be set to refer to the item or subitem for which information is being returned. The nCol member should be set to 0 (zero) because it is the only column in which anything can be obtained or set. In addition, the data members for each of the flags set in the mask member of the structure pointed to by the item parameter if this method call succeeds will be returned.

If itemID is 0 (zero), the nIndex member can be used.

When applied to virtual lists, you must use the nIndex member and set itemID to 0 (zero). For virtual lists you can only get the select and focus states of an item.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iresultdata-setitem">IResultData::SetItem</a>