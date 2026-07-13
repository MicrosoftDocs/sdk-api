---
UID: NF:windowsx.ComboBox_AddString
title: ComboBox_AddString macro (windowsx.h)
description: Adds a string to a list in a combo box.
helpviewer_keywords: ["ComboBox_AddString","ComboBox_AddString macro [Windows Controls]","_win32_ComboBox_AddString","_win32_ComboBox_AddString_cpp","controls.ComboBox_AddString","controls._win32_ComboBox_AddString","windowsx/ComboBox_AddString"]
old-location: controls\ComboBox_AddString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_addstring.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_AddString, ComboBox_AddString macro [Windows Controls], _win32_ComboBox_AddString, _win32_ComboBox_AddString_cpp, controls.ComboBox_AddString, controls._win32_ComboBox_AddString, windowsx/ComboBox_AddString
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
 - ComboBox_AddString
 - windowsx/ComboBox_AddString
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
 - ComboBox_AddString
---

# ComboBox_AddString macro

## -syntax

```cpp
int ComboBox_AddString(
   HWND    hwndCtl,
   LPCTSTR lpsz
);
```

## -returns

Type: **int**

The return value is the zero-based index of the string in the list. If an error occurs, the return value is CB_ERR. If there is insufficient space to store the new string, the return value is CB_ERRSPACE.


## -description

Adds a string to a list in a combo box. If the combo box does not have the <a href="/windows/desktop/Controls/combo-box-styles">CBS_SORT</a> style, the string is added to the end of the list. Otherwise, the string is inserted into the list and the list is sorted. You can use this macro or send the <a href="/windows/desktop/Controls/cb-addstring">CB_ADDSTRING</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lpsz

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The string to add.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-addstring">CB_ADDSTRING</a>.
