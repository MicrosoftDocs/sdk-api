---
UID: NF:mmc.IColumnData.GetColumnSortData
title: IColumnData::GetColumnSortData
author: windows-sdk-content
description: The IColumnData::GetColumnSortData method enables a snap-in to retrieve from memory the sorted column and sorting direction for columns in a column set.
old-location: mmc\icolumndata_getcolumnsortdata.htm
tech.root: mmc
ms.assetid: cbcc5e61-994e-46e2-b227-398b79cbc557
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: GetColumnSortData, GetColumnSortData method [MMC], GetColumnSortData method [MMC],IColumnData interface, IColumnData interface [MMC],GetColumnSortData method, IColumnData.GetColumnSortData, IColumnData::GetColumnSortData, _slate_icolumndata_getcolumnsortdata, mmc.icolumndata_getcolumnsortdata, mmc/IColumnData::GetColumnSortData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IColumnData.GetColumnSortData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IColumnData::GetColumnSortData


## -description


The <b>IColumnData::GetColumnSortData</b> method enables a snap-in to retrieve from memory the sorted column and sorting direction for columns in a column set.


## -parameters




### -param pColID [in]

A pointer to an 
<a href="https://msdn.microsoft.com/eb08f699-74bc-445d-96b7-678abbd366b3">SColumnSetID</a> structure that contains the ID of the column set whose sort data is to be retrieved.


### -param ppColSortData [out]

A pointer to a pointer to an 
<a href="https://msdn.microsoft.com/bb16061d-a6bb-4816-b52d-c63097638f58">MMC_SORT_SET_DATA</a> structure that will contain the column sort data of the column set.


## -returns



This method can return one of these values.




## -remarks



If the user selects a scope item and then modifies the sort data of the list view of the selected item. If the snap-in calls <b>IColumnData::GetColumnSortData</b> to retrieve the same sort data, the method will return the new data, regardless of whether the user has deselected the item or not.

The 
<a href="https://msdn.microsoft.com/bb16061d-a6bb-4816-b52d-c63097638f58">MMC_SORT_SET_DATA</a> structure and its array of 
<a href="https://msdn.microsoft.com/26500d98-4355-4e0c-a636-2c6898955ef0">MMC_SORT_DATA</a> structures are allocated as one contiguous memory block by MMC during calls to 
GetColumnSortData. The snap-in must call CoTaskMemFree with the given pointer to 
<b>MMC_SORT_SET_DATA</b>. This frees the entire memory block.

All data set and retrieved by the methods of the 
<a href="https://msdn.microsoft.com/fb2b8863-c476-4997-915d-329cf66fd945">IColumnData</a> interface is persisted by MMC in memory, and not in a stream or storage medium. This data is persisted to an .msc console file only when the user chooses the 
<b>Save</b> menu command.




## -see-also




<a href="https://msdn.microsoft.com/fb2b8863-c476-4997-915d-329cf66fd945">IColumnData</a>



<a href="https://msdn.microsoft.com/4da79fd1-f887-447c-89fd-d5044bd5751c">Using IColumnData</a>
 

 

