---
UID: NF:mmc.IColumnData.GetColumnConfigData
title: IColumnData::GetColumnConfigData
author: windows-sdk-content
description: The IColumnData::GetColumnConfigData method enables a snap-in to retrieve the current width, order, and hidden status of each column in a column set that is stored in memory by MMC.
old-location: mmc\icolumndata_getcolumnconfigdata.htm
old-project: mmc
ms.assetid: 197804a2-63e5-4f0c-9d6d-4abc751a8a82
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetColumnConfigData, GetColumnConfigData method [MMC], GetColumnConfigData method [MMC],IColumnData interface, IColumnData interface [MMC],GetColumnConfigData method, IColumnData.GetColumnConfigData, IColumnData::GetColumnConfigData, _slate_icolumndata_getcolumnconfigdata, mmc.icolumndata_getcolumnconfigdata, mmc/IColumnData::GetColumnConfigData
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IColumnData.GetColumnConfigData
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IColumnData::GetColumnConfigData


## -description


The <b>IColumnData::GetColumnConfigData</b> method enables a snap-in to retrieve the current width, order, and hidden status of each column in a column set that is stored in memory by MMC.


## -parameters




### -param pColID [in]

A pointer to an 
<a href="https://msdn.microsoft.com/eb08f699-74bc-445d-96b7-678abbd366b3">SColumnSetID</a> structure that holds the ID of the column set whose data is to be retrieved.


### -param ppColSetData [out]

A pointer to a pointer to an 
<a href="https://msdn.microsoft.com/15088a2f-3dfc-4af4-bcae-e7e9e456df8b">MMC_COLUMN_SET_DATA</a> structure that will hold the retrieved column data.


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




<a href="https://msdn.microsoft.com/fb2b8863-c476-4997-915d-329cf66fd945">IColumnData</a>



<a href="https://msdn.microsoft.com/4da79fd1-f887-447c-89fd-d5044bd5751c">Using IColumnData</a>
 

 

