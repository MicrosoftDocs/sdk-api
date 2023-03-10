---
UID: NF:mmc.IResultData.Sort
title: IResultData::Sort (mmc.h)
description: Sorts all items in the result pane.
helpviewer_keywords: ["IResultData interface [MMC]","Sort method","IResultData.Sort","IResultData2 interface [MMC]","Sort method","IResultData2::Sort","IResultData::Sort","RSI_DESCENDING = 0x0001","RSI_NOSORTICON = 0x0002","Sort","Sort method [MMC]","Sort method [MMC]","IResultData interface","Sort method [MMC]","IResultData2 interface","_slate_iresultdata_sort","mmc.iresultdata_sort","mmc/IResultData2::Sort","mmc/IResultData::Sort"]
old-location: mmc\iresultdata_sort.htm
tech.root: mmc
ms.assetid: 457eccaf-3727-4b29-a38b-9f009749673e
ms.date: 12/05/2018
ms.keywords: IResultData interface [MMC],Sort method, IResultData.Sort, IResultData2 interface [MMC],Sort method, IResultData2::Sort, IResultData::Sort, RSI_DESCENDING = 0x0001, RSI_NOSORTICON = 0x0002, Sort, Sort method [MMC], Sort method [MMC],IResultData interface, Sort method [MMC],IResultData2 interface, _slate_iresultdata_sort, mmc.iresultdata_sort, mmc/IResultData2::Sort, mmc/IResultData::Sort
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
 - IResultData::Sort
 - mmc/IResultData::Sort
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
 - IResultData.Sort
 - IResultData2.Sort
---

# IResultData::Sort


## -description

The <b>IResultData::Sort</b> method sorts all items in the result pane.

## -parameters

### -param nColumn [in]

An index of the column header clicked.

### -param dwSortOptions [in]

The sort options to be used during the sort operation. This value can be a combination of the following:



#### RSI_DESCENDING = 0x0001

The sort should be in descending order. The default is to sort in ascending order.



#### RSI_NOSORTICON = 0x0002

Instructs MMC to remove the sort arrow icon. This option is useful when the snap-in performs a custom sort operation.

### -param lUserParam [in]

A value that specifies information determined by the user. This parameter can contain a variety of entries such as including sort order or context information.

## -returns

This method can return one of these values.

## -remarks

If your snap-in implements the 
<a href="/windows/desktop/api/mmc/nn-mmc-iresultdatacompare">IResultDataCompare</a> or the 
<a href="/windows/desktop/api/mmc/nn-mmc-iresultdatacompareex">IResultDataCompareEx</a> interface, MMC calls the interface's 
Compare method to allow the snap-in to compare list items. Otherwise, MMC uses a default string-compare function.

There is no sorting function for a virtual list. To allow virtual list sorting the snap-in must implement the 
<a href="/windows/desktop/api/mmc/nn-mmc-iresultownerdata">IResultOwnerData</a> interface. When <b>IResultData::Sort</b> is called, MMC forwards the call to 
<a href="/windows/desktop/api/mmc/nf-mmc-iresultownerdata-sortitems">IResultOwnerData::SortItems</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata">IResultData</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iresultdata2">IResultData2</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iresultdatacompare-compare">IResultDataCompare::Compare</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iresultownerdata-sortitems">IResultOwnerData::SortItems</a>