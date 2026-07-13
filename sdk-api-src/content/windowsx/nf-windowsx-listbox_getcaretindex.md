---
UID: NF:windowsx.ListBox_GetCaretIndex
title: ListBox_GetCaretIndex macro (windowsx.h)
description: Retrieves the index of the list box item that has the focus rectangle in a multiple-selection list box. The item may or may not be selected. You can use this macro or send the LB_GETCARETINDEX message explicitly.
helpviewer_keywords: ["ListBox_GetCaretIndex","ListBox_GetCaretIndex macro [Windows Controls]","_win32_ListBox_GetCaretIndex","_win32_ListBox_GetCaretIndex_cpp","controls.ListBox_GetCaretIndex","controls._win32_ListBox_GetCaretIndex","windowsx/ListBox_GetCaretIndex"]
old-location: controls\ListBox_GetCaretIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getcaretindex.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetCaretIndex, ListBox_GetCaretIndex macro [Windows Controls], _win32_ListBox_GetCaretIndex, _win32_ListBox_GetCaretIndex_cpp, controls.ListBox_GetCaretIndex, controls._win32_ListBox_GetCaretIndex, windowsx/ListBox_GetCaretIndex
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
 - ListBox_GetCaretIndex
 - windowsx/ListBox_GetCaretIndex
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
 - ListBox_GetCaretIndex
---

# ListBox_GetCaretIndex macro

## -syntax

```cpp
int ListBox_GetCaretIndex(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The zero-based index of the focused item, or 0 if no item has the focus.


## -description

Retrieves the index of the list box item that has the focus rectangle in a multiple-selection list box. The item may or may not be selected. You can use this macro or send the <a href="/windows/desktop/controls/lb-getcaretindex">LB_GETCARETINDEX</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

The contents of the list box are scrolled till the item is fully visible.

For more information, see <a href="/windows/desktop/controls/lb-getcaretindex">LB_GETCARETINDEX</a>.
