---
UID: NF:mmc.IColumnData.GetColumnSortData
title: IColumnData::GetColumnSortData (mmc.h)
description: The IColumnData::GetColumnSortData method enables a snap-in to retrieve from memory the sorted column and sorting direction for columns in a column set.
helpviewer_keywords: ["GetColumnSortData","GetColumnSortData method [MMC]","GetColumnSortData method [MMC]","IColumnData interface","IColumnData interface [MMC]","GetColumnSortData method","IColumnData.GetColumnSortData","IColumnData::GetColumnSortData","_slate_icolumndata_getcolumnsortdata","mmc.icolumndata_getcolumnsortdata","mmc/IColumnData::GetColumnSortData"]
old-location: mmc\icolumndata_getcolumnsortdata.htm
tech.root: mmc
ms.assetid: cbcc5e61-994e-46e2-b227-398b79cbc557
ms.date: 12/05/2018
ms.keywords: GetColumnSortData, GetColumnSortData method [MMC], GetColumnSortData method [MMC],IColumnData interface, IColumnData interface [MMC],GetColumnSortData method, IColumnData.GetColumnSortData, IColumnData::GetColumnSortData, _slate_icolumndata_getcolumnsortdata, mmc.icolumndata_getcolumnsortdata, mmc/IColumnData::GetColumnSortData
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
 - IColumnData::GetColumnSortData
 - mmc/IColumnData::GetColumnSortData
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
 - IColumnData.GetColumnSortData
---

# IColumnData::GetColumnSortData


## -description

The <b>IColumnData::GetColumnSortData</b> method enables a snap-in to retrieve from memory the sorted column and sorting direction for columns in a column set.

## -parameters

### -param pColID [in]

A pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-scolumnsetid">SColumnSetID</a> structure that contains the ID of the column set whose sort data is to be retrieved.

### -param ppColSortData [out]

A pointer to a pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_sort_set_data">MMC_SORT_SET_DATA</a> structure that will contain the column sort data of the column set.

## -returns

This method can return one of these values.

## -remarks

If the user selects a scope item and then modifies the sort data of the list view of the selected item. If the snap-in calls <b>IColumnData::GetColumnSortData</b> to retrieve the same sort data, the method will return the new data, regardless of whether the user has deselected the item or not.

The 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_sort_set_data">MMC_SORT_SET_DATA</a> structure and its array of 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_sort_data">MMC_SORT_DATA</a> structures are allocated as one contiguous memory block by MMC during calls to 
GetColumnSortData. The snap-in must call CoTaskMemFree with the given pointer to 
<b>MMC_SORT_SET_DATA</b>. This frees the entire memory block.

All data set and retrieved by the methods of the 
<a href="/windows/desktop/api/mmc/nn-mmc-icolumndata">IColumnData</a> interface is persisted by MMC in memory, and not in a stream or storage medium. This data is persisted to an .msc console file only when the user chooses the 
<b>Save</b> menu command.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icolumndata">IColumnData</a>



<a href="/previous-versions/windows/desktop/mmc/using-icolumndata">Using IColumnData</a>