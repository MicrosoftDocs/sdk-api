---
UID: NF:windowsx.ListBox_AddString
title: ListBox_AddString macro (windowsx.h)
description: Adds a string to a list box.
helpviewer_keywords: ["ListBox_AddString","ListBox_AddString macro [Windows Controls]","_win32_ListBox_AddString","_win32_ListBox_AddString_cpp","controls.ListBox_AddString","controls._win32_ListBox_AddString","windowsx/ListBox_AddString"]
old-location: controls\ListBox_AddString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_addstring.htm
ms.date: 10/21/2024
ms.keywords: ListBox_AddString, ListBox_AddString macro [Windows Controls], _win32_ListBox_AddString, _win32_ListBox_AddString_cpp, controls.ListBox_AddString, controls._win32_ListBox_AddString, windowsx/ListBox_AddString
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
 - ListBox_AddString
 - windowsx/ListBox_AddString
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
 - ListBox_AddString
---

# ListBox_AddString macro

## -syntax

```cpp
int ListBox_AddString(
   HWND   hwndCtl,
   LPCSTR lpsz
);
```

## -returns

Type: **int**

The return value is the zero-based index of the string in the list box. If an error occurs, the return value is LB_ERR. If there is insufficient space to store the new string, the return value is LB_ERRSPACE.


## -description

Adds a string to a list box. If the list box does not have the <a href="/windows/desktop/Controls/list-box-styles">LBS_SORT</a> style, the string is added to the end of the list. Otherwise, the string is inserted into the list and the list is sorted. You can use this macro or send the <a href="/windows/desktop/Controls/lb-addstring">LB_ADDSTRING</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lpsz

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The string to add.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-addstring">LB_ADDSTRING</a>.
