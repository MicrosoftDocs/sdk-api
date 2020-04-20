---
UID: NF:windowsx.ListBox_SetCurSel
title: ListBox_SetCurSel macro (windowsx.h)
description: Sets the currently selected item in a single-selection list box. You can use this macro or send the LB_SETCURSEL message explicitly.helpviewer_keywords: ["ListBox_SetCurSel","ListBox_SetCurSel macro [Windows Controls]","_win32_ListBox_SetCurSel","_win32_ListBox_SetCurSel_cpp","controls.ListBox_SetCurSel","controls._win32_ListBox_SetCurSel","windowsx/ListBox_SetCurSel"]
old-location: controls\ListBox_SetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setcursel.htm
ms.date: 12/05/2018
ms.keywords: ListBox_SetCurSel, ListBox_SetCurSel macro [Windows Controls], _win32_ListBox_SetCurSel, _win32_ListBox_SetCurSel_cpp, controls.ListBox_SetCurSel, controls._win32_ListBox_SetCurSel, windowsx/ListBox_SetCurSel
f1_keywords:
- windowsx/ListBox_SetCurSel
dev_langs:
- c++
req.header: windowsx.h
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
- Windowsx.h
api_name:
- ListBox_SetCurSel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_SetCurSel macro


## -description


Sets the currently selected item in a single-selection list box. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-setcursel">LB_SETCURSEL</a> message explicitly.




## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item to select, or –1 to clear the selection.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-setcursel">LB_SETCURSEL</a>.



