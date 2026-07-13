---
UID: NF:windowsx.ComboBox_InsertItemData
title: ComboBox_InsertItemData macro (windowsx.h)
description: Inserts item data in a list in a combo box at the specified location. You can use this macro or send the CB_INSERTSTRING message explicitly.
helpviewer_keywords: ["ComboBox_InsertItemData","ComboBox_InsertItemData macro [Windows Controls]","_win32_ComboBox_InsertItemData","_win32_ComboBox_InsertItemData_cpp","controls.ComboBox_InsertItemData","controls._win32_ComboBox_InsertItemData","windowsx/ComboBox_InsertItemData"]
old-location: controls\ComboBox_InsertItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_insertitemdata.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_InsertItemData, ComboBox_InsertItemData macro [Windows Controls], _win32_ComboBox_InsertItemData, _win32_ComboBox_InsertItemData_cpp, controls.ComboBox_InsertItemData, controls._win32_ComboBox_InsertItemData, windowsx/ComboBox_InsertItemData
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
 - ComboBox_InsertItemData
 - windowsx/ComboBox_InsertItemData
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
 - ComboBox_InsertItemData
---

# ComboBox_InsertItemData macro

## -syntax

```cpp
int ComboBox_InsertItemData(
   HWND   hwndCtl,
   int    index,
   LPARAM data
);
```

## -returns

Type: **int**

The return value is the zero-based index of the item in the list. If an error occurs, the return value is CB_ERR. If there is insufficient space to store the new string, the return value is CB_ERRSPACE.


## -description

Inserts item data in a list in a combo box at the specified location. You can use this macro or send the <a href="/windows/desktop/Controls/cb-insertstring">CB_INSERTSTRING</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index in the list at which to insert the item data, or –1 to add it to the end of the list.

### -param data

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The item data to insert.

## -remarks

Use this macro for a list in a combo box with an owner-drawn style but without the <a href="/windows/desktop/Controls/combo-box-styles">CBS_HASSTRINGS</a> style. For more information, see <a href="/windows/desktop/Controls/cb-insertstring">CB_INSERTSTRING</a>.
