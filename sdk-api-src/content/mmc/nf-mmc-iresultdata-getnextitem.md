---
UID: NF:mmc.IResultData.GetNextItem
title: IResultData::GetNextItem
author: windows-sdk-content
description: The IResultData::GetNextItem method gets the next item in the result view with the specified state flags set.
old-location: mmc\iresultdata_getnextitem.htm
tech.root: mmc
ms.assetid: 1123fa48-969c-4208-83f2-e8ef4f72f0bb
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetNextItem, GetNextItem method [MMC], GetNextItem method [MMC],IResultData interface, GetNextItem method [MMC],IResultData2 interface, IResultData interface [MMC],GetNextItem method, IResultData.GetNextItem, IResultData2 interface [MMC],GetNextItem method, IResultData2::GetNextItem, IResultData::GetNextItem, _slate_iresultdata_getnextitem, mmc.iresultdata_getnextitem, mmc/IResultData2::GetNextItem, mmc/IResultData::GetNextItem
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
 - IResultData.GetNextItem
 - IResultData2.GetNextItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultData::GetNextItem


## -description


The <b>IResultData::GetNextItem</b> method gets the next item in the result view with the specified state flags set.


## -parameters




### -param item [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> structure that contains information about the item to be obtained. The <b>nIndex</b> member should be set to the index at which to start the search, or to –1 to start at the first item. The specified index is excluded from the search. The <b>nState</b> member should specify which state flags must be set on the returned item.

The <b>nIndex</b> member will be updated to the index of the found item (or –1, if none is found). The <b>bScopeItem</b> and <b>lParam</b> members will be set according to the found item.


## -returns



This method can return one of these values.




## -remarks



When applied to virtual lists, only the <b>LVIS_FOCUSED</b> and <b>LVIS_SELECTED</b> state flags can specified. The <b>lParam</b> member is always set to 0 (zero).




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>
 

 

