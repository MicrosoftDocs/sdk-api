---
UID: NF:mmc.IHeaderCtrl.SetColumnWidth
title: IHeaderCtrl::SetColumnWidth
author: windows-sdk-content
description: Sets the width, in pixels, of a specific column.
old-location: mmc\iheaderctrl_setcolumnwidth.htm
old-project: mmc
ms.assetid: E704FF35-3859-4313-B42D-77A114AA6E78
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IHeaderCtrl interface [MMC],SetColumnWidth method, IHeaderCtrl.SetColumnWidth, IHeaderCtrl::SetColumnWidth, MMCLV_AUTO, SetColumnWidth, SetColumnWidth method [MMC], SetColumnWidth method [MMC],IHeaderCtrl interface, mmc.iheaderctrl_setcolumnwidth, mmc/IHeaderCtrl::SetColumnWidth
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
req.idl: Mmc.idl
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
 - IHeaderCtrl.SetColumnWidth
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IHeaderCtrl::SetColumnWidth


## -description


Sets the width, in pixels, of a specific column.


## -parameters




### -param nCol [in]

A zero-based index that specifies the location of the column relative to other columns in the result pane.


### -param nWidth [in]

A value that specifies the width of the column. This value must be in pixels, or it can be the following value:



#### MMCLV_AUTO

MMC automatically determines the width of the column based on the width of the text in the column title.


## -returns



This method can return one of these values.




## -remarks



MMC does not persist in memory any changes made to a column set due to the action of <b>IHeaderCtrl::SetColumnWidth</b>, so snap-ins must update persisted column configuration data after modifying the width of columns in a column set. For more information, see 
<a href="https://msdn.microsoft.com/acec421f-edd4-49b6-a244-7099c524fe75">IHeaderCtrl2 and Column Persistence</a>.

The HIDE_COLUMN flag for the nWidth parameter is not supported for 
SetColumnWidth. If the snap-in must hide the column, it must call <a href="https://msdn.microsoft.com/library/Mt300850(v=VS.85).aspx">IConsole::SelectScopeItem</a> to reselect the scope item and then in the resulting call to the snap-in's <a href="https://msdn.microsoft.com/cc2a9da4-1351-4930-8fb4-577cdcc14e10">MMCN_SHOW</a> notification handler, it must use nWidth=HIDE_COLUMN when inserting the column (in the call to <a href="https://msdn.microsoft.com/F5499550-9460-4BF9-AF99-F4BDC7F32EBC">IHeaderCtrl::InsertColumn</a>).




## -see-also




<a href="https://msdn.microsoft.com/library/Mt300857(v=VS.85).aspx">IHeaderCtrl</a>



<a href="https://msdn.microsoft.com/acec421f-edd4-49b6-a244-7099c524fe75">IHeaderCtrl2 and Column Persistence</a>
 

 

