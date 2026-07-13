---
UID: NF:windowsx.ListBox_DeleteString
title: ListBox_DeleteString macro (windowsx.h)
description: Deletes the item at the specified location in a list box. You can use this macro or send the LB_DELETESTRING message explicitly.
helpviewer_keywords: ["ListBox_DeleteString","ListBox_DeleteString macro [Windows Controls]","_win32_ListBox_DeleteString","_win32_ListBox_DeleteString_cpp","controls.ListBox_DeleteString","controls._win32_ListBox_DeleteString","windowsx/ListBox_DeleteString"]
old-location: controls\ListBox_DeleteString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_deletestring.htm
ms.date: 10/21/2024
ms.keywords: ListBox_DeleteString, ListBox_DeleteString macro [Windows Controls], _win32_ListBox_DeleteString, _win32_ListBox_DeleteString_cpp, controls.ListBox_DeleteString, controls._win32_ListBox_DeleteString, windowsx/ListBox_DeleteString
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
 - ListBox_DeleteString
 - windowsx/ListBox_DeleteString
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
 - ListBox_DeleteString
---

# ListBox_DeleteString macro

## -syntax

```cpp
int ListBox_DeleteString(
   HWND hwndCtl,
   int  index
);
```

## -returns

Type: **int**

The return value is a count of the strings remaining in the list. The return value is LB_ERR if the <i>index</i> parameter specifies an index greater than the number of items in the list.


## -description

Deletes the item at the specified location in a list box. You can use this macro or send the <a href="/windows/desktop/Controls/lb-deletestring">LB_DELETESTRING</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item to delete.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-deletestring">LB_DELETESTRING</a>
