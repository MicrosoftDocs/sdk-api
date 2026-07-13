---
UID: NF:windowsx.ComboBox_GetCurSel
title: ComboBox_GetCurSel macro (windowsx.h)
description: Gets the index of the currently selected item in a combo box. You can use this macro or send the CB_GETCURSEL message explicitly.
helpviewer_keywords: ["ComboBox_GetCurSel","ComboBox_GetCurSel macro [Windows Controls]","_win32_ComboBox_GetCurSel","_win32_ComboBox_GetCurSel_cpp","controls.ComboBox_GetCurSel","controls._win32_ComboBox_GetCurSel","windowsx/ComboBox_GetCurSel"]
old-location: controls\ComboBox_GetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getcursel.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetCurSel, ComboBox_GetCurSel macro [Windows Controls], _win32_ComboBox_GetCurSel, _win32_ComboBox_GetCurSel_cpp, controls.ComboBox_GetCurSel, controls._win32_ComboBox_GetCurSel, windowsx/ComboBox_GetCurSel
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
 - ComboBox_GetCurSel
 - windowsx/ComboBox_GetCurSel
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
 - ComboBox_GetCurSel
---

# ComboBox_GetCurSel macro

## -syntax

```cpp
int ComboBox_GetCurSel(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The zero-based index of the selected item. If there is no selection, the return value is CB_ERR.


## -description

Gets the index of the currently selected item in a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-getcursel">CB_GETCURSEL</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.
