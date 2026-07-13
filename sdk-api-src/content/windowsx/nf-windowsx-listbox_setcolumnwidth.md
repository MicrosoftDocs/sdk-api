---
UID: NF:windowsx.ListBox_SetColumnWidth
title: ListBox_SetColumnWidth macro (windowsx.h)
description: Sets the width of all columns in a multiple-column list box. You can use this macro or send the LB_SETCOLUMNWIDTH message explicitly.
helpviewer_keywords: ["ListBox_SetColumnWidth","ListBox_SetColumnWidth macro [Windows Controls]","_win32_ListBox_SetColumnWidth","_win32_ListBox_SetColumnWidth_cpp","controls.ListBox_SetColumnWidth","controls._win32_ListBox_SetColumnWidth","windowsx/ListBox_SetColumnWidth"]
old-location: controls\ListBox_SetColumnWidth.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setcolumnwidth.htm
ms.date: 10/21/2024
ms.keywords: ListBox_SetColumnWidth, ListBox_SetColumnWidth macro [Windows Controls], _win32_ListBox_SetColumnWidth, _win32_ListBox_SetColumnWidth_cpp, controls.ListBox_SetColumnWidth, controls._win32_ListBox_SetColumnWidth, windowsx/ListBox_SetColumnWidth
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ListBox_SetColumnWidth
 - windowsx/ListBox_SetColumnWidth
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ListBox_SetColumnWidth
---

# ListBox_SetColumnWidth macro

## -syntax

```cpp
void ListBox_SetColumnWidth(
   HWND hwndCtl,
   int  cxColumn
);
```


## -description

Sets the width of all columns in a multiple-column list box. You can use this macro or send the <a href="/windows/desktop/Controls/lb-setcolumnwidth">LB_SETCOLUMNWIDTH</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param cxColumn

Type: <b>int</b>

The width, in pixels, of all columns.
