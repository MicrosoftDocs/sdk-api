---
UID: NF:windowsx.ListBox_GetItemHeight
title: ListBox_GetItemHeight macro (windowsx.h)
description: Retrieves the height of items in a list box.
helpviewer_keywords: ["ListBox_GetItemHeight","ListBox_GetItemHeight macro [Windows Controls]","_win32_ListBox_GetItemHeight","_win32_ListBox_GetItemHeight_cpp","controls.ListBox_GetItemHeight","controls._win32_ListBox_GetItemHeight","windowsx/ListBox_GetItemHeight"]
old-location: controls\ListBox_GetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getitemheight.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetItemHeight, ListBox_GetItemHeight macro [Windows Controls], _win32_ListBox_GetItemHeight, _win32_ListBox_GetItemHeight_cpp, controls.ListBox_GetItemHeight, controls._win32_ListBox_GetItemHeight, windowsx/ListBox_GetItemHeight
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
 - ListBox_GetItemHeight
 - windowsx/ListBox_GetItemHeight
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
 - ListBox_GetItemHeight
---

# ListBox_GetItemHeight macro

## -syntax

```cpp
int ListBox_GetItemHeight(
   HWND hwndCtl,
   int  index
);
```

## -returns

Type: **int**

The height, in pixels, of the item or items, or LB_ERR if an error occurs.


## -description

Retrieves the height of items in a list box. If the list box has the <a href="/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWVARIABLE</a> style, this macro gets the height of the specified item; otherwise, it gets the height of all items. You can use this macro or send the <a href="/windows/desktop/Controls/lb-getitemheight">LB_GETITEMHEIGHT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item. If the list box does not have the <a href="/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWVARIABLE</a> style, set this parameter to zero.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-getitemheight">LB_GETITEMHEIGHT</a>.
