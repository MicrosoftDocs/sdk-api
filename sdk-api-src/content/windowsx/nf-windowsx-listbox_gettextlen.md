---
UID: NF:windowsx.ListBox_GetTextLen
title: ListBox_GetTextLen macro (windowsx.h)
description: Gets the length of a string in a list box. You can use this macro or send the LB_GETTEXTLEN message explicitly.
helpviewer_keywords: ["ListBox_GetTextLen","ListBox_GetTextLen macro [Windows Controls]","_win32_ListBox_GetTextLen","_win32_ListBox_GetTextLen_cpp","controls.ListBox_GetTextLen","controls._win32_ListBox_GetTextLen","windowsx/ListBox_GetTextLen"]
old-location: controls\ListBox_GetTextLen.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_gettextlen.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetTextLen, ListBox_GetTextLen macro [Windows Controls], _win32_ListBox_GetTextLen, _win32_ListBox_GetTextLen_cpp, controls.ListBox_GetTextLen, controls._win32_ListBox_GetTextLen, windowsx/ListBox_GetTextLen
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
 - ListBox_GetTextLen
 - windowsx/ListBox_GetTextLen
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
 - ListBox_GetTextLen
---

# ListBox_GetTextLen macro

## -syntax

```cpp
int ListBox_GetTextLen(
   HWND hwndCtl,
   int  index
);
```

## -returns

Type: **int**

The count of characters in the string.


## -description

Gets the length of a string in a list box.  You can use this macro or send the <a href="/windows/desktop/Controls/lb-gettextlen">LB_GETTEXTLEN</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-gettextlen">LB_GETTEXTLEN</a>.
