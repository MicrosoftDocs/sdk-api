---
UID: NF:windowsx.ListBox_SetItemData
title: ListBox_SetItemData macro (windowsx.h)
description: Sets the application-defined value associated with the specified list box item. You can use this macro or send the LB_SETITEMDATA message explicitly.
helpviewer_keywords: ["ListBox_SetItemData","ListBox_SetItemData macro [Windows Controls]","_win32_ListBox_SetItemData","_win32_ListBox_SetItemData_cpp","controls.ListBox_SetItemData","controls._win32_ListBox_SetItemData","windowsx/ListBox_SetItemData"]
old-location: controls\ListBox_SetItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setitemdata.htm
ms.date: 10/21/2024
ms.keywords: ListBox_SetItemData, ListBox_SetItemData macro [Windows Controls], _win32_ListBox_SetItemData, _win32_ListBox_SetItemData_cpp, controls.ListBox_SetItemData, controls._win32_ListBox_SetItemData, windowsx/ListBox_SetItemData
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
 - ListBox_SetItemData
 - windowsx/ListBox_SetItemData
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
 - ListBox_SetItemData
---

# ListBox_SetItemData macro

## -syntax

```cpp
int ListBox_SetItemData(
   HWND   hwndCtl,
   int    index,
   LPARAM data
);
```

## -returns

Type: **int**

If an error occurs, the return value is LB_ERR.


## -description

Sets the application-defined value associated with the specified list box item. You can use this macro or send the <a href="/windows/desktop/Controls/lb-setitemdata">LB_SETITEMDATA</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item.

### -param data

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The item data to set.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-setitemdata">LB_SETITEMDATA</a>.
