---
UID: NF:windowsx.ComboBox_SetCurSel
title: ComboBox_SetCurSel macro (windowsx.h)
description: Sets the currently selected item in a combo box. You can use this macro or send the CB_SETCURSEL message explicitly.
helpviewer_keywords: ["ComboBox_SetCurSel","ComboBox_SetCurSel macro [Windows Controls]","_win32_ComboBox_SetCurSel","_win32_ComboBox_SetCurSel_cpp","controls.ComboBox_SetCurSel","controls._win32_ComboBox_SetCurSel","windowsx/ComboBox_SetCurSel"]
old-location: controls\ComboBox_SetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setcursel.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_SetCurSel, ComboBox_SetCurSel macro [Windows Controls], _win32_ComboBox_SetCurSel, _win32_ComboBox_SetCurSel_cpp, controls.ComboBox_SetCurSel, controls._win32_ComboBox_SetCurSel, windowsx/ComboBox_SetCurSel
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
 - ComboBox_SetCurSel
 - windowsx/ComboBox_SetCurSel
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
 - ComboBox_SetCurSel
---

# ComboBox_SetCurSel macro

## -syntax

```cpp
int ComboBox_SetCurSel(
   HWND hwndCtl,
   int  index
);
```

## -returns

Type: **int**

If an error occurs, the return value is CB_ERR. If the <i>index</i> parameter is &#8211;1, the return value is CB_ERR even though no error occurred.


## -description

Sets the currently selected item in a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-setcursel">CB_SETCURSEL</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item to select, or –1 to clear the selection.
