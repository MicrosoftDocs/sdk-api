---
UID: NF:mmc.IColumnData.SetColumnSortData
title: IColumnData::SetColumnSortData (mmc.h)
author: windows-sdk-content
description: The IColumnData::SetColumnSortData method enables a snap-in to set the sorted column and sorting direction for columns in a column set.
old-location: mmc\icolumndata_setcolumnsortdata.htm
tech.root: mmc
ms.assetid: ece69cce-6861-4795-b1cb-da22d2bdc67a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IColumnData interface [MMC],SetColumnSortData method, IColumnData.SetColumnSortData, IColumnData::SetColumnSortData, SetColumnSortData, SetColumnSortData method [MMC], SetColumnSortData method [MMC],IColumnData interface, _slate_icolumndata_setcolumnsortdata, mmc.icolumndata_setcolumnsortdata, mmc/IColumnData::SetColumnSortData
ms.topic: method
f1_keywords:
- mmc/IColumnData.SetColumnSortData
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmcndmgr.dll
api_name:
- IColumnData.SetColumnSortData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IColumnData::SetColumnSortData


## -description


The <b>IColumnData::SetColumnSortData</b> method enables a snap-in to set the sorted column and sorting direction for columns in a column set.


## -parameters




### -param pColID [in]

A pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-scolumnsetid">SColumnSetID</a> structure that contains the column set ID of the column set whose sort data is to be set.


### -param pColSortData [in]

A pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-mmc_sort_set_data">MMC_SORT_SET_DATA</a> structure that contains the column sort data of the column set.


## -returns



This method can return one of these values.




## -remarks



If the user selects a scope item, and the snap-in then calls <b>IColumnData::SetColumnSortData</b> to modify the sort data of the list view of the selected item. MMC will apply the changes to the list view only after the user has deselected and then reselected the item. Be aware that MMC also applies the changes to all column sets with the same ID, so if the user selects a different item with the same column set ID, MMC will also apply the persisted data to it.

MMC 1.2 supports only single-column sorting, which is why 
SetColumnSortData returns <b>E_FAIL</b> when the number of sort columns is greater than 1.

All data set and retrieved by the methods of the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icolumndata">IColumnData</a> interface is persisted by MMC in memory, and not in a stream or storage medium. This data is persisted to an .msc console file only when the user chooses the 
<b>Save</b> menu command.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icolumndata">IColumnData</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/using-icolumndata">Using IColumnData</a>
 

 

