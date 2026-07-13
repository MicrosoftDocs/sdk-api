---
UID: NF:windowsx.ComboBox_FindItemData
title: ComboBox_FindItemData macro (windowsx.h)
description: Finds the first item in a combo box list that has the specified item data. You can use this macro or send the CB_FINDSTRING message explicitly.
helpviewer_keywords: ["ComboBox_FindItemData","ComboBox_FindItemData macro [Windows Controls]","_win32_ComboBox_FindItemData","_win32_ComboBox_FindItemData_cpp","controls.ComboBox_FindItemData","controls._win32_ComboBox_FindItemData","windowsx/ComboBox_FindItemData"]
old-location: controls\ComboBox_FindItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_finditemdata.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_FindItemData, ComboBox_FindItemData macro [Windows Controls], _win32_ComboBox_FindItemData, _win32_ComboBox_FindItemData_cpp, controls.ComboBox_FindItemData, controls._win32_ComboBox_FindItemData, windowsx/ComboBox_FindItemData
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
 - ComboBox_FindItemData
 - windowsx/ComboBox_FindItemData
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
 - ComboBox_FindItemData
---

# ComboBox_FindItemData macro

## -syntax

```cpp
int ComboBox_FindItemData(
   HWND   hwndCtl,
   int    indexStart,
   LPARAM data
);
```

## -returns

Type: **int**

The index of the matching item, or CB_ERR if the search was unsuccessful.


## -description

Finds the first item in a combo box list that has the specified item data. You can use this macro or send the <a href="/windows/desktop/Controls/cb-findstring">CB_FINDSTRING</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list, it continues searching from the top of the list back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i> is –1, the entire list is searched from the beginning.

### -param data

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The data to find.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-findstring">CB_FINDSTRING</a>.
