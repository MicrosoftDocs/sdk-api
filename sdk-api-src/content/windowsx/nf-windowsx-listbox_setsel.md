---
UID: NF:windowsx.ListBox_SetSel
title: ListBox_SetSel macro (windowsx.h)
description: Selects or deselects an item in a multiple-selection list box. You can use this macro or send the LB_SETSEL message explicitly.
helpviewer_keywords: ["ListBox_SetSel","ListBox_SetSel macro [Windows Controls]","_win32_ListBox_SetSel","_win32_ListBox_SetSel_cpp","controls.ListBox_SetSel","controls._win32_ListBox_SetSel","windowsx/ListBox_SetSel"]
old-location: controls\ListBox_SetSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setsel.htm
ms.date: 10/21/2024
ms.keywords: ListBox_SetSel, ListBox_SetSel macro [Windows Controls], _win32_ListBox_SetSel, _win32_ListBox_SetSel_cpp, controls.ListBox_SetSel, controls._win32_ListBox_SetSel, windowsx/ListBox_SetSel
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
 - ListBox_SetSel
 - windowsx/ListBox_SetSel
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
 - ListBox_SetSel
---

# ListBox_SetSel macro

## -syntax

```cpp
int ListBox_SetSel(
   HWND hwndCtl,
   BOOL fSelect,
   int  index
);
```

## -returns

Type: **int**

If an error occurs, the return value is LB_ERR.


## -description

Selects or deselects an item in a multiple-selection list box. You can use this macro or send the <a href="/windows/desktop/Controls/lb-setsel">LB_SETSEL</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fSelect

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to select the item, or <b>FALSE</b> to deselect it.

### -param index

Type: <b>int</b>

The zero-based index of the item.
