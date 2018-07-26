---
UID: NF:mmc.IResultData.SetItem
title: IResultData::SetItem
author: windows-sdk-content
description: The IResultData::SetItem method enables the snap-in to set a single item in the result pane.
old-location: mmc\iresultdata_setitem.htm
old-project: MMC
ms.assetid: d24ab645-aae2-4c0f-8fc5-05d028a724d4
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IResultData interface [MMC],SetItem method, IResultData.SetItem, IResultData2 interface [MMC],SetItem method, IResultData2::SetItem, IResultData::SetItem, SetItem, SetItem method [MMC], SetItem method [MMC],IResultData interface, SetItem method [MMC],IResultData2 interface, _slate_iresultdata_setitem, mmc.iresultdata_setitem, mmc/IResultData2::SetItem, mmc/IResultData::SetItem
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
 - IResultData.SetItem
 - IResultData2.SetItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IResultData::SetItem


## -description


The <b>IResultData::SetItem</b> method enables the snap-in to set a single item in the result pane.


## -parameters




### -param item [in]

A pointer to a 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> structure that contains information about the item to be changed.


## -returns



This method can return one of these values.




## -remarks



The itemID member of the structure pointed to by the item parameter should be set to refer to the item or subitem to be changed in the list. The mask and all appropriate associated fields in the 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> structure should be filled out with the preferred changes. The nCol member should be set to 0 (zero) because it is the only column in which anything can be set or obtained. The str member of 
<b>RESULTDATAITEM</b> should always be set to MMC_CALLBACK.

This method does not support virtual lists.




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>



<a href="https://msdn.microsoft.com/18c345b0-7d3c-4c80-8d1e-b8d5791bc550">IResultData::GetItem</a>
 

 

