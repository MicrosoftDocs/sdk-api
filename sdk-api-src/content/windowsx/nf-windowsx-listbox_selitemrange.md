---
UID: NF:windowsx.ListBox_SelItemRange
title: ListBox_SelItemRange macro (windowsx.h)
description: Selects or deselects one or more consecutive items in a multiple-selection list box. You can use this macro or send the LB_SELITEMRANGE message explicitly.
helpviewer_keywords: ["ListBox_SelItemRange","ListBox_SelItemRange macro [Windows Controls]","_win32_ListBox_SelItemRange","_win32_ListBox_SelItemRange_cpp","controls.ListBox_SelItemRange","controls._win32_ListBox_SelItemRange","windowsx/ListBox_SelItemRange"]
old-location: controls\ListBox_SelItemRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_selitemrange.htm
ms.date: 10/21/2024
ms.keywords: ListBox_SelItemRange, ListBox_SelItemRange macro [Windows Controls], _win32_ListBox_SelItemRange, _win32_ListBox_SelItemRange_cpp, controls.ListBox_SelItemRange, controls._win32_ListBox_SelItemRange, windowsx/ListBox_SelItemRange
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
 - ListBox_SelItemRange
 - windowsx/ListBox_SelItemRange
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
 - ListBox_SelItemRange
---

# ListBox_SelItemRange macro

## -syntax

```cpp
int ListBox_SelItemRange(
   HWND hwndCtl,
   BOOL fSelect,
   int  first,
   int  last
);
```

## -returns

Type: **int**

If an error occurs, the return value is LB_ERR.


## -description

Selects or deselects one or more consecutive items in a multiple-selection list box. You can use this macro or send the <a href="/windows/desktop/Controls/lb-selitemrange">LB_SELITEMRANGE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fSelect

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to select the range of items, or <b>FALSE</b> to deselect it.

### -param first

Type: <b>int</b>

The zero-based index of the first item to select.

### -param last

Type: <b>int</b>

The zero-based index of the last item to select.
