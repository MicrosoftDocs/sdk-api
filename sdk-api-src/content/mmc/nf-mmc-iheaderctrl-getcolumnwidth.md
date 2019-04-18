---
UID: NF:mmc.IHeaderCtrl.GetColumnWidth
title: IHeaderCtrl::GetColumnWidth (mmc.h)
author: windows-sdk-content
description: Retrieves the width, in pixels, of the column.
old-location: mmc\iheaderctrl_getcolumnwidth.htm
tech.root: mmc
ms.assetid: 2F0C08F2-C7AF-4E91-A7AD-34BC19D65DC2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetColumnWidth, GetColumnWidth method [MMC], GetColumnWidth method [MMC],IHeaderCtrl interface, IHeaderCtrl interface [MMC],GetColumnWidth method, IHeaderCtrl.GetColumnWidth, IHeaderCtrl::GetColumnWidth, mmc.iheaderctrl_getcolumnwidth, mmc/IHeaderCtrl::GetColumnWidth
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
req.idl: Mmc.idl
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
 - IHeaderCtrl.GetColumnWidth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IHeaderCtrl::GetColumnWidth


## -description


Retrieves the width, in pixels, of the column.


## -parameters




### -param nCol [in]

A zero-based index of the column from which the width is to be retrieved.


### -param pWidth [out]

A pointer to width, in pixels, of the column. This parameter must not be <b>NULL</b>.


## -returns



This method can return one of these values.




## -remarks



This method can be called successfully even if items are already in the list.

If the column is currently hidden, 
GetColumnWidth returns 0 (zero) as the column width. However, because a column can have a (0) zero width without being hidden, a return value of (0) zero does not mean that the column is hidden. Therefore, the snap-in should call 
<a href="https://msdn.microsoft.com/197804a2-63e5-4f0c-9d6d-4abc751a8a82">IColumnData::GetColumnConfigData</a> to identify which columns are hidden.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt300857(v=VS.85).aspx">IHeaderCtrl</a>
 

 

