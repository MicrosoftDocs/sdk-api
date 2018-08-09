---
UID: NF:mmc.IResultData.GetItem
title: IResultData::GetItem
author: windows-sdk-content
description: Enables a user to retrieve the parameters of a single item.
old-location: mmc\iresultdata_getitem.htm
old-project: MMC
ms.assetid: 18c345b0-7d3c-4c80-8d1e-b8d5791bc550
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetItem, GetItem method [MMC], GetItem method [MMC],IResultData interface, GetItem method [MMC],IResultData2 interface, IResultData interface [MMC],GetItem method, IResultData.GetItem, IResultData2 interface [MMC],GetItem method, IResultData2::GetItem, IResultData::GetItem, _slate_iresultdata_getitem, mmc.iresultdata_getitem, mmc/IResultData2::GetItem, mmc/IResultData::GetItem
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
 - IResultData.GetItem
 - IResultData2.GetItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IResultData::GetItem


## -description


The <b>IResultData::GetItem</b> method enables a user to retrieve the parameters of a single item.


## -parameters




### -param item [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> structure that contains information about the item whose parameters are being retrieved.


## -returns



This method can return one of these values.




## -remarks



The itemID member of the 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> structure pointed to by the item parameter should be set to refer to the item or subitem for which information is being returned. The nCol member should be set to 0 (zero) because it is the only column in which anything can be obtained or set. In addition, the data members for each of the flags set in the mask member of the structure pointed to by the item parameter if this method call succeeds will be returned.

If itemID is 0 (zero), the nIndex member can be used.

When applied to virtual lists, you must use the nIndex member and set itemID to 0 (zero). For virtual lists you can only get the select and focus states of an item.




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>



<a href="https://msdn.microsoft.com/d24ab645-aae2-4c0f-8fc5-05d028a724d4">IResultData::SetItem</a>
 

 

