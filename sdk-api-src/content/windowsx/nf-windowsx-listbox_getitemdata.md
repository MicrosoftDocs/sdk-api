---
UID: NF:windowsx.ListBox_GetItemData
title: ListBox_GetItemData macro (windowsx.h)
description: Gets the application-defined value associated with the specified list box item. You can use this macro or send the LB_GETITEMDATA message explicitly.
helpviewer_keywords: ["ListBox_GetItemData","ListBox_GetItemData macro [Windows Controls]","_win32_ListBox_GetItemData","_win32_ListBox_GetItemData_cpp","controls.ListBox_GetItemData","controls._win32_ListBox_GetItemData","windowsx/ListBox_GetItemData"]
old-location: controls\ListBox_GetItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getitemdata.htm
ms.date: 10/21/2024
ms.keywords: ListBox_GetItemData, ListBox_GetItemData macro [Windows Controls], _win32_ListBox_GetItemData, _win32_ListBox_GetItemData_cpp, controls.ListBox_GetItemData, controls._win32_ListBox_GetItemData, windowsx/ListBox_GetItemData
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
 - ListBox_GetItemData
 - windowsx/ListBox_GetItemData
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
 - ListBox_GetItemData
---

# ListBox_GetItemData macro

## -syntax

```cpp
LRESULT ListBox_GetItemData(
   HWND hwndCtl,
   int  index
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

The item data. For more information, see <b>LB_GETITEMDATA</b>.


## -description

Gets the application-defined value associated with the specified list box item. You can use this macro or send the <a href="/windows/desktop/Controls/lb-getitemdata">LB_GETITEMDATA</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item.
