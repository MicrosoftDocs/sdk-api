---
UID: NF:mmc.IResultData.GetNextItem
title: IResultData::GetNextItem (mmc.h)
description: The IResultData::GetNextItem method gets the next item in the result view with the specified state flags set.
helpviewer_keywords: ["GetNextItem","GetNextItem method [MMC]","GetNextItem method [MMC]","IResultData interface","GetNextItem method [MMC]","IResultData2 interface","IResultData interface [MMC]","GetNextItem method","IResultData.GetNextItem","IResultData2 interface [MMC]","GetNextItem method","IResultData2::GetNextItem","IResultData::GetNextItem","_slate_iresultdata_getnextitem","mmc.iresultdata_getnextitem","mmc/IResultData2::GetNextItem","mmc/IResultData::GetNextItem"]
old-location: mmc\iresultdata_getnextitem.htm
tech.root: mmc
ms.assetid: 1123fa48-969c-4208-83f2-e8ef4f72f0bb
ms.date: 12/05/2018
ms.keywords: GetNextItem, GetNextItem method [MMC], GetNextItem method [MMC],IResultData interface, GetNextItem method [MMC],IResultData2 interface, IResultData interface [MMC],GetNextItem method, IResultData.GetNextItem, IResultData2 interface [MMC],GetNextItem method, IResultData2::GetNextItem, IResultData::GetNextItem, _slate_iresultdata_getnextitem, mmc.iresultdata_getnextitem, mmc/IResultData2::GetNextItem, mmc/IResultData::GetNextItem
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
 - IResultData::GetNextItem
 - mmc/IResultData::GetNextItem
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
 - IResultData.GetNextItem
 - IResultData2.GetNextItem
---

# IResultData::GetNextItem


## -description

The <b>IResultData::GetNextItem</b> method gets the next item in the result view with the specified state flags set.

## -parameters

### -param item [in, out]

A pointer to a 
<a href="/windows/desktop/api/mmc/ns-mmc-resultdataitem">RESULTDATAITEM</a> structure that contains information about the item to be obtained. The <b>nIndex</b> member should be set to the index at which to start the search, or to –1 to start at the first item. The specified index is excluded from the search. The <b>nState</b> member should specify which state flags must be set on the returned item.

The <b>nIndex</b> member will be updated to the index of the found item (or –1, if none is found). The <b>bScopeItem</b> and <b>lParam</b> members will be set according to the found item.

## -returns

This method can return one of these values.

## -remarks

When applied to virtual lists, only the <b>LVIS_FOCUSED</b> and <b>LVIS_SELECTED</b> state flags can specified. The <b>lParam</b> member is always set to 0 (zero).

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>