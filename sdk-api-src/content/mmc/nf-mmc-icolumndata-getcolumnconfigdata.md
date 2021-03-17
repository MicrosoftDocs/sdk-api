---
UID: NF:mmc.IColumnData.GetColumnConfigData
title: IColumnData::GetColumnConfigData (mmc.h)
description: The IColumnData::GetColumnConfigData method enables a snap-in to retrieve the current width, order, and hidden status of each column in a column set that is stored in memory by MMC.
helpviewer_keywords: ["GetColumnConfigData","GetColumnConfigData method [MMC]","GetColumnConfigData method [MMC]","IColumnData interface","IColumnData interface [MMC]","GetColumnConfigData method","IColumnData.GetColumnConfigData","IColumnData::GetColumnConfigData","_slate_icolumndata_getcolumnconfigdata","mmc.icolumndata_getcolumnconfigdata","mmc/IColumnData::GetColumnConfigData"]
old-location: mmc\icolumndata_getcolumnconfigdata.htm
tech.root: mmc
ms.assetid: 197804a2-63e5-4f0c-9d6d-4abc751a8a82
ms.date: 12/05/2018
ms.keywords: GetColumnConfigData, GetColumnConfigData method [MMC], GetColumnConfigData method [MMC],IColumnData interface, IColumnData interface [MMC],GetColumnConfigData method, IColumnData.GetColumnConfigData, IColumnData::GetColumnConfigData, _slate_icolumndata_getcolumnconfigdata, mmc.icolumndata_getcolumnconfigdata, mmc/IColumnData::GetColumnConfigData
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
 - IColumnData::GetColumnConfigData
 - mmc/IColumnData::GetColumnConfigData
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
 - IColumnData.GetColumnConfigData
---

# IColumnData::GetColumnConfigData


## -description

The <b>IColumnData::GetColumnConfigData</b> method enables a snap-in to retrieve the current width, order, and hidden status of each column in a column set that is stored in memory by MMC.

## -parameters

### -param pColID [in]

A pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-scolumnsetid">SColumnSetID</a> structure that holds the ID of the column set whose data is to be retrieved.

### -param ppColSetData [out]

A pointer to a pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_column_set_data">MMC_COLUMN_SET_DATA</a> structure that will hold the retrieved column data.

## -returns

This method can return one of these values.

## -remarks

Suppose the user selects a scope item and then modifies the column configuration data of the list view of the selected item. If the snap-in calls <b>IColumnData::GetColumnConfigData</b> to retrieve that list view's column configuration data, the method will return the new data, regardless of whether or not the user has deselected the item.

The 
<b>MMC_COLUMN_SET_DATA</b> structure and its array of 
<b>MMC_COLUMN_DATA</b> structures are allocated as one contiguous memory block by MMC during calls to 
<b>GetColumnConfigData</b>. The snap-in must call <b>CoTaskMemFree</b> with the given pointer to 
<b>MMC_COLUMN_SET_DATA</b>. This frees the entire memory block.

All data set and retrieved by the methods of the 
<b>IColumnData</b> interface is persisted by MMC in memory, and not in a stream or storage medium. This data is saved to an .MSC console file only when the user clicks the 
<b>Save</b> menu command.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-icolumndata">IColumnData</a>



<a href="/previous-versions/windows/desktop/mmc/using-icolumndata">Using IColumnData</a>