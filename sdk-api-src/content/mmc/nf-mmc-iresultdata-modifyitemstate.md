---
UID: NF:mmc.IResultData.ModifyItemState
title: IResultData::ModifyItemState
author: windows-sdk-content
description: Enables the snap-in to modify the state of an item.
old-location: mmc\iresultdata_modifyitemstate.htm
tech.root: MMC
ms.assetid: f7eb7a23-27e6-40f3-a2f3-139ad1d3cde0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IResultData interface [MMC],ModifyItemState method, IResultData.ModifyItemState, IResultData2 interface [MMC],ModifyItemState method, IResultData2::ModifyItemState, IResultData::ModifyItemState, LVIS_CUT, LVIS_DROPHILITED, LVIS_FOCUSED, LVIS_SELECTED, ModifyItemState, ModifyItemState method [MMC], ModifyItemState method [MMC],IResultData interface, ModifyItemState method [MMC],IResultData2 interface, _slate_iresultdata_modifyitemstate, mmc.iresultdata_modifyitemstate, mmc/IResultData2::ModifyItemState, mmc/IResultData::ModifyItemState
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
 - IResultData.ModifyItemState
 - IResultData2.ModifyItemState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IResultData::ModifyItemState


## -description


The <b>IResultData::ModifyItemState</b> method enables the snap-in to modify the state of an item.


## -parameters




### -param nIndex [in]

A value that specifies the index of the item whose state is to be modified. This parameter is used only when the itemID parameter is zero. When applied to virtual lists, you must use nIndex and set itemID to zero.


### -param itemID [in]

Unique identifier of the item whose state is to be modified. When applied to virtual lists, set itemID = 0.


### -param uAdd [in]

A value that specifies which Windows list-view state flags can be set. When applied to virtual lists, only focus and select states can be modified. This value can be any valid combination of the following:



#### LVIS_CUT

The item is marked for a cut-and-paste operation.



#### LVIS_DROPHILITED

The item is highlighted as a drag-and-drop target.



#### LVIS_FOCUSED

The item has the focus, so it is surrounded by a standard focus rectangle. Although more than one item can be selected, only one item can have the focus.



#### LVIS_SELECTED

The item is selected. The appearance of a selected item depends on whether it has the focus and on the system colors used for selection.


### -param uRemove [in]

A value that specifies the list-view item state flags that can be removed. This value can be any valid combination of the preceding Win32 LVIS_* flags shown for the uAdd parameter.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>
 

 

