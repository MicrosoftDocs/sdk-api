---
UID: NF:mmc.IResultData.InsertItem
title: IResultData::InsertItem
author: windows-sdk-content
description: The IResultData::InsertItem method enables the snap-in to add a single new item to the result pane view.
old-location: mmc\iresultdata_insertitem.htm
old-project: mmc
ms.assetid: c354e718-ea9a-4d50-8a77-776500b86d25
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: IResultData interface [MMC],InsertItem method, IResultData.InsertItem, IResultData2 interface [MMC],InsertItem method, IResultData2::InsertItem, IResultData::InsertItem, InsertItem, InsertItem method [MMC], InsertItem method [MMC],IResultData interface, InsertItem method [MMC],IResultData2 interface, _slate_iresultdata_insertitem, mmc.iresultdata_insertitem, mmc/IResultData2::InsertItem, mmc/IResultData::InsertItem
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
 - IResultData.InsertItem
 - IResultData2.InsertItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IResultData::InsertItem


## -description


The <b>IResultData::InsertItem</b> method enables the snap-in to add a single new item to the result pane view.


## -parameters




### -param item [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> structure that contains information about the item to be added.

After the item is inserted, a unique identifier (an item ID) is assigned to it by MMC and returned through the <b>itemID</b> member of the structure pointed to by the item parameter. Be aware that the <b>itemID</b> value is the <b>HRESULTITEM</b> handle of the inserted item. The snap-in should store this value in order to later manipulate the inserted item by calling methods such as <a href="https://msdn.microsoft.com/18c345b0-7d3c-4c80-8d1e-b8d5791bc550">IResultData::GetItem</a>.

If this identifier is not stored, it can be looked up using 
<a href="https://msdn.microsoft.com/f26be5d5-9b7d-4cbd-b70c-431799c68e5e">IResultData::FindItemByLParam</a>.


## -returns



This method can return one of these values.




## -remarks



The mask and all appropriate associated fields in the 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> structure should be filled out. Subitems cannot be inserted but can be set. The <b>nCol</b> member of the item structure must therefore be zero.

The str member of 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> must be set to <b>MMC_CALLBACK</b>.

After the item is inserted, a unique identifier (an item ID) is assigned to it by MMC and returned through the <b>itemID</b> member of the structure pointed to by the item parameter. Be aware that the <b>itemID</b> value is the <b>HRESULTITEM</b> handle of the inserted item. The snap-in should store this value in order to later manipulate the inserted item by calling methods such as <a href="https://msdn.microsoft.com/18c345b0-7d3c-4c80-8d1e-b8d5791bc550">IResultData::GetItem</a>.

If this identifier is not stored, it can be identified using 
<a href="https://msdn.microsoft.com/f26be5d5-9b7d-4cbd-b70c-431799c68e5e">IResultData::FindItemByLParam</a>.

This method does not support virtual lists.




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>
 

 

