---
UID: NF:commctrl.ListView_InsertColumn
title: ListView_InsertColumn macro
author: windows-sdk-content
description: Inserts a new column in a list-view control. You can use this macro or send the LVM_INSERTCOLUMN message explicitly.
old-location: controls\ListView_InsertColumn.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertcolumn.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: ListView_InsertColumn, ListView_InsertColumn macro [Windows Controls], _win32_ListView_InsertColumn, _win32_ListView_InsertColumn_cpp, commctrl/ListView_InsertColumn, controls.ListView_InsertColumn, controls._win32_ListView_InsertColumn
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_InsertColumn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_InsertColumn macro


## -description


Inserts a new column in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/1326e38e-bb45-4d0d-b5bc-ec684b3b92ef">LVM_INSERTCOLUMN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param iCol

Type: <b>int</b>

The index of the new column. 


### -param pcol

Type: <b>const LPLVCOLUMN</b>

A pointer to an <a href="https://msdn.microsoft.com/6ffa287d-0284-43c9-80ff-b9c90a83e855">LVCOLUMN</a> structure that contains the attributes of the new column. 


## -remarks



Columns are visible only in report (details) view.
	



