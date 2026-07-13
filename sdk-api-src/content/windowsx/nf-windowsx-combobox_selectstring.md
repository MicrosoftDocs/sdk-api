---
UID: NF:windowsx.ComboBox_SelectString
title: ComboBox_SelectString macro (windowsx.h)
description: Searches a list in a combo box for an item that begins with the characters in a specified string. If a matching item is found, the item is selected. You can use this macro or send the CB_SELECTSTRING message explicitly.
helpviewer_keywords: ["ComboBox_SelectString","ComboBox_SelectString macro [Windows Controls]","_win32_ComboBox_SelectString","_win32_ComboBox_SelectString_cpp","controls.ComboBox_SelectString","controls._win32_ComboBox_SelectString","windowsx/ComboBox_SelectString"]
old-location: controls\ComboBox_SelectString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_selectstring.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_SelectString, ComboBox_SelectString macro [Windows Controls], _win32_ComboBox_SelectString, _win32_ComboBox_SelectString_cpp, controls.ComboBox_SelectString, controls._win32_ComboBox_SelectString, windowsx/ComboBox_SelectString
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
 - ComboBox_SelectString
 - windowsx/ComboBox_SelectString
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
 - ComboBox_SelectString
---

# ComboBox_SelectString macro

## -syntax

```cpp
int ComboBox_SelectString(
   HWND    hwndCtl,
   int     indexStart,
   LPCTSTR lpszSelect
);
```

## -returns

Type: **int**

If the search is successful, the return value is the index of the selected item. If the search is unsuccessful, the return value is CB_ERR and the current selection is not changed.


## -description

Searches a list in a combo box for an item that begins with the characters in a specified string. If a matching item is found, the item is selected. You can use this macro or send the <a href="/windows/desktop/Controls/cb-selectstring">CB_SELECTSTRING</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list, it continues searching from the top of the list back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list is searched from the beginning.

### -param lpszSelect

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The string to find.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-selectstring">CB_SELECTSTRING</a>.
