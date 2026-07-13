---
UID: NF:windowsx.ListBox_FindItemData
title: ListBox_FindItemData macro (windowsx.h)
description: Finds the first item in a list box that has the specified item data. You can use this macro or send the LB_FINDSTRING message explicitly.
helpviewer_keywords: ["ListBox_FindItemData","ListBox_FindItemData macro [Windows Controls]","_win32_ListBox_FindItemData","_win32_ListBox_FindItemData_cpp","controls.ListBox_FindItemData","controls._win32_ListBox_FindItemData","windowsx/ListBox_FindItemData"]
old-location: controls\ListBox_FindItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_finditemdata.htm
ms.date: 10/21/2024
ms.keywords: ListBox_FindItemData, ListBox_FindItemData macro [Windows Controls], _win32_ListBox_FindItemData, _win32_ListBox_FindItemData_cpp, controls.ListBox_FindItemData, controls._win32_ListBox_FindItemData, windowsx/ListBox_FindItemData
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
 - ListBox_FindItemData
 - windowsx/ListBox_FindItemData
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
 - ListBox_FindItemData
---

# ListBox_FindItemData macro

## -syntax

```cpp
int ListBox_FindItemData(
   HWND   hwndCtl,
   int    indexStart,
   LPARAM data
);
```

## -returns

Type: **int**

The index of the matching item, or LB_ERR if the search was unsuccessful.


## -description

Finds the first item in a list box that has the specified item data. You can use this macro or send the <a href="/windows/desktop/Controls/lb-findstring">LB_FINDSTRING</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list box is searched from the beginning.

### -param data

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The data to find.

## -remarks

For more information, see <a href="/windows/desktop/Controls/lb-findstring">LB_FINDSTRING</a>.
