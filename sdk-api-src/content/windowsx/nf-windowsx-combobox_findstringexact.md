---
UID: NF:windowsx.ComboBox_FindStringExact
title: ComboBox_FindStringExact macro (windowsx.h)
description: Finds the first string in a combo box list that exactly matches the specified string, except that the search is not case sensitive. You can use this macro or send the CB_FINDSTRINGEXACT message explicitly.
helpviewer_keywords: ["ComboBox_FindStringExact","ComboBox_FindStringExact macro [Windows Controls]","_win32_ComboBox_FindStringExact","_win32_ComboBox_FindStringExact_cpp","controls.ComboBox_FindStringExact","controls._win32_ComboBox_FindStringExact","windowsx/ComboBox_FindStringExact"]
old-location: controls\ComboBox_FindStringExact.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_findstringexact.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_FindStringExact, ComboBox_FindStringExact macro [Windows Controls], _win32_ComboBox_FindStringExact, _win32_ComboBox_FindStringExact_cpp, controls.ComboBox_FindStringExact, controls._win32_ComboBox_FindStringExact, windowsx/ComboBox_FindStringExact
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
 - ComboBox_FindStringExact
 - windowsx/ComboBox_FindStringExact
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
 - ComboBox_FindStringExact
---

# ComboBox_FindStringExact macro

## -syntax

```cpp
int ComboBox_FindStringExact(
   HWND    hwndCtl,
   int     indexStart,
   LPCTSTR lpszFind
);
```

## -returns

Type: **int**

The index of the matching item, or CB_ERR if the search was unsuccessful.


## -description

Finds the first string in a combo box list that exactly matches the specified string, except that the search is not case sensitive. You can use this macro or send the <a href="/windows/desktop/Controls/cb-findstringexact">CB_FINDSTRINGEXACT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list, it continues searching from the top of the list back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list is searched from the beginning.

### -param lpszFind

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The string to find.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-findstringexact">CB_FINDSTRINGEXACT</a>.
