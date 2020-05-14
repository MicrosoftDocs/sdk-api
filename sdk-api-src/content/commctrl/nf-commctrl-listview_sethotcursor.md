---
UID: NF:commctrl.ListView_SetHotCursor
title: ListView_SetHotCursor macro (commctrl.h)
description: Sets the HCURSOR that the list-view control uses when the pointer is over an item while hot tracking is enabled. You can use this macro or send the LVM_SETHOTCURSOR message explicitly. To check whether hot tracking is enabled, call SystemParametersInfo.helpviewer_keywords: ["ListView_SetHotCursor","ListView_SetHotCursor macro [Windows Controls]","_win32_ListView_SetHotCursor","_win32_ListView_SetHotCursor_cpp","commctrl/ListView_SetHotCursor","controls.ListView_SetHotCursor","controls._win32_ListView_SetHotCursor"]
old-location: controls\ListView_SetHotCursor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_sethotcursor.htm
ms.date: 12/05/2018
ms.keywords: ListView_SetHotCursor, ListView_SetHotCursor macro [Windows Controls], _win32_ListView_SetHotCursor, _win32_ListView_SetHotCursor_cpp, commctrl/ListView_SetHotCursor, controls.ListView_SetHotCursor, controls._win32_ListView_SetHotCursor
f1_keywords:
- commctrl/ListView_SetHotCursor
dev_langs:
- c++
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
- ListView_SetHotCursor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetHotCursor macro


## -description


Sets the HCURSOR that the list-view control uses when the pointer is over an item while hot tracking is enabled. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-sethotcursor">LVM_SETHOTCURSOR</a> message explicitly. To check whether hot tracking is enabled, call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa">SystemParametersInfo</a>. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control. 


### -param hcur

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HCURSOR</a></b>

A handle to the cursor to be set. 


## -remarks



A list-view control uses hot tracking and hover selection when the <a href="https://docs.microsoft.com/windows/desktop/Controls/extended-list-view-styles">LVS_EX_TRACKSELECT</a> style is set. 



