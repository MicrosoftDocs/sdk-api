---
UID: NF:windowsx.ComboBox_SetExtendedUI
title: ComboBox_SetExtendedUI macro (windowsx.h)
description: Selects either the default user interface (UI) or the extended UI for a combo box that has the CBS_DROPDOWN or CBS_DROPDOWNLIST style. You can use this macro or send the CB_SETEXTENDEDUI message explicitly.
helpviewer_keywords: ["ComboBox_SetExtendedUI","ComboBox_SetExtendedUI macro [Windows Controls]","_win32_ComboBox_SetExtendedUI","_win32_ComboBox_SetExtendedUI_cpp","controls.ComboBox_SetExtendedUI","controls._win32_ComboBox_SetExtendedUI","windowsx/ComboBox_SetExtendedUI"]
old-location: controls\ComboBox_SetExtendedUI.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setextendedui.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_SetExtendedUI, ComboBox_SetExtendedUI macro [Windows Controls], _win32_ComboBox_SetExtendedUI, _win32_ComboBox_SetExtendedUI_cpp, controls.ComboBox_SetExtendedUI, controls._win32_ComboBox_SetExtendedUI, windowsx/ComboBox_SetExtendedUI
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
 - ComboBox_SetExtendedUI
 - windowsx/ComboBox_SetExtendedUI
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
 - ComboBox_SetExtendedUI
---

# ComboBox_SetExtendedUI macro

## -syntax

```cpp
int ComboBox_SetExtendedUI(
   HWND hwndCtl,
   UINT flags
);
```

## -returns

Type: **int**

If an error occurs, the return value is CB_ERR.


## -description

Selects either the default user interface (UI) or the extended UI for a combo box that has the <a href="/windows/desktop/Controls/combo-box-styles">CBS_DROPDOWN</a> or <a href="/windows/desktop/Controls/combo-box-styles">CBS_DROPDOWNLIST</a> style. You can use this macro or send the <a href="/windows/desktop/Controls/cb-setextendedui">CB_SETEXTENDEDUI</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero to use the default UI, or nonzero to use the extended UI.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-setextendedui">CB_SETEXTENDEDUI</a>.
