---
UID: NF:mmc.IResultData.ModifyViewStyle
title: IResultData::ModifyViewStyle
author: windows-sdk-content
description: The IResultData::ModifyViewStyle method enables the snap-in to set the result pane's view style.
old-location: mmc\iresultdata_modifyviewstyle.htm
old-project: MMC
ms.assetid: f33a427c-6952-4877-bbfb-09ac976ea188
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IResultData interface [MMC],ModifyViewStyle method, IResultData.ModifyViewStyle, IResultData2 interface [MMC],ModifyViewStyle method, IResultData2::ModifyViewStyle, IResultData::ModifyViewStyle, MMC_NOSORTHEADER, MMC_SHOWSELALWAYS, MMC_SINGLESEL, ModifyViewStyle, ModifyViewStyle method [MMC], ModifyViewStyle method [MMC],IResultData interface, ModifyViewStyle method [MMC],IResultData2 interface, _slate_iresultdata_modifyviewstyle, mmc.iresultdata_modifyviewstyle, mmc/IResultData2::ModifyViewStyle, mmc/IResultData::ModifyViewStyle
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
 - IResultData.ModifyViewStyle
 - IResultData2.ModifyViewStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IResultData::ModifyViewStyle


## -description


The <b>IResultData::ModifyViewStyle</b> method enables the snap-in to set the result pane's view style.


## -parameters




### -param add [in]

A value that specifies the view style (or styles) to be set in the result view pane. This value can be a valid combination of the following:



#### MMC_SINGLESEL

Allows only one item at a time to be selected. Without this view style, multiple items can be selected.



#### MMC_SHOWSELALWAYS

Always show the selection, if any, even if the control does not have the focus.



#### MMC_NOSORTHEADER

A value that specifies that column headers do not work like buttons. This style is useful if clicking on a column header in report view does not perform an operation, such as sorting.

These values are from the 
<a href="https://msdn.microsoft.com/2f1b93e2-aa1d-4478-877b-a26cdb3dc84b">MMC_RESULT_VIEW_STYLE</a> enumeration and correspond to the Win32 LVS_* flags of the same names.


### -param remove [in]

A value that specifies the view style (or styles) to be removed from the result view pane. This value can be a valid combination of the preceding flags shown for the add parameter. As described there, these values are from the 
<a href="https://msdn.microsoft.com/2f1b93e2-aa1d-4478-877b-a26cdb3dc84b">MMC_RESULT_VIEW_STYLE</a> enumeration and correspond to the Win32 LVS_* flags of the same names.


## -returns



This method can return one of these values.




## -remarks



This method provides the same functionality for both result view panes and virtual lists.




## -see-also




<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>



<a href="https://msdn.microsoft.com/cca0c2a4-7a41-48d1-bdaa-27b7aad7cc05">IResultData2</a>
 

 

