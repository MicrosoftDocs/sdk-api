---
UID: NF:windowsx.ListBox_SetItemHeight
title: ListBox_SetItemHeight macro (windowsx.h)
description: Sets the height of items in a list box.
helpviewer_keywords: ["ListBox_SetItemHeight","ListBox_SetItemHeight macro [Windows Controls]","_win32_ListBox_SetItemHeight","_win32_ListBox_SetItemHeight_cpp","controls.ListBox_SetItemHeight","controls._win32_ListBox_SetItemHeight","windowsx/ListBox_SetItemHeight"]
old-location: controls\ListBox_SetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setitemheight.htm
ms.date: 10/21/2024
ms.keywords: ListBox_SetItemHeight, ListBox_SetItemHeight macro [Windows Controls], _win32_ListBox_SetItemHeight, _win32_ListBox_SetItemHeight_cpp, controls.ListBox_SetItemHeight, controls._win32_ListBox_SetItemHeight, windowsx/ListBox_SetItemHeight
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
 - ListBox_SetItemHeight
 - windowsx/ListBox_SetItemHeight
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
 - ListBox_SetItemHeight
---

# ListBox_SetItemHeight macro

## -syntax

```cpp
int ListBox_SetItemHeight(
   HWND   hwndCtl,
   int    index,
   LPARAM cy
);
```

## -returns

Type: **int**

If the index or height is invalid, the return value is LB_ERR.


## -description

Sets the height of items in a list box. If the list box has the <a href="/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWVARIABLE</a> style, this macro sets the height of the specified item; otherwise, it sets the height of all items. You can use this macro or send the <a href="/windows/desktop/Controls/lb-setitemheight">LB_SETITEMHEIGHT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item. If the list box does not have the <a href="/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWVARIABLE</a> style, set this parameter to zero.

### -param cy

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The height of the item or items, in pixels.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-setitemheight">LB_SETITEMHEIGHT</a>.
