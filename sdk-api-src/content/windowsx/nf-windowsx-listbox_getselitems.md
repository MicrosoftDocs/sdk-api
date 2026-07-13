---
UID: NF:windowsx.ListBox_GetSelItems
title: ListBox_GetSelItems macro (windowsx.h)
description: Gets the indexes of selected items in a multiple-selection list box. You can use this macro or send the LB_GETSELITEMS message explicitly.
helpviewer_keywords: ["ListBox_GetSelItems","ListBox_GetSelItems macro [Windows Controls]","_win32_ListBox_GetSelItems","_win32_ListBox_GetSelItems_cpp","controls.ListBox_GetSelItems","controls._win32_ListBox_GetSelItems","windowsx/ListBox_GetSelItems"]
old-location: controls\ListBox_GetSelItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getselitems.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetSelItems, ListBox_GetSelItems macro [Windows Controls], _win32_ListBox_GetSelItems, _win32_ListBox_GetSelItems_cpp, controls.ListBox_GetSelItems, controls._win32_ListBox_GetSelItems, windowsx/ListBox_GetSelItems
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
 - ListBox_GetSelItems
 - windowsx/ListBox_GetSelItems
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
 - ListBox_GetSelItems
---

# ListBox_GetSelItems macro

## -syntax

```cpp
int ListBox_GetSelItems(
   HWND hwndCtl,
   int  cItems,
   int  *lpItems
);
```

## -returns

Type: **int**

The number of items placed in the buffer. If the list box is a single-selection list box, the return value is LB_ERR.


## -description

Gets the indexes of selected items in a multiple-selection list box. You can use this macro or send the <a href="/windows/desktop/Controls/lb-getselitems">LB_GETSELITEMS</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param cItems

Type: <b>int</b>

The maximum number of selected items whose item numbers are to be placed in the buffer.

### -param lpItems

Type: <b>int*</b>

A pointer to a buffer large enough for the number of integers specified by <i>cItems</i>.
