---
UID: NF:windowsx.ComboBox_GetExtendedUI
title: ComboBox_GetExtendedUI macro (windowsx.h)
description: Ascertains whether a combo box is using the default user interface (UI) or the extended UI. You can use this macro or send the CB_GETEXTENDEDUI message explicitly.
helpviewer_keywords: ["ComboBox_GetExtendedUI","ComboBox_GetExtendedUI macro [Windows Controls]","_win32_ComboBox_GetExtendedUI","_win32_ComboBox_GetExtendedUI_cpp","controls.ComboBox_GetExtendedUI","controls._win32_ComboBox_GetExtendedUI","windowsx/ComboBox_GetExtendedUI"]
old-location: controls\ComboBox_GetExtendedUI.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getextendedui.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetExtendedUI, ComboBox_GetExtendedUI macro [Windows Controls], _win32_ComboBox_GetExtendedUI, _win32_ComboBox_GetExtendedUI_cpp, controls.ComboBox_GetExtendedUI, controls._win32_ComboBox_GetExtendedUI, windowsx/ComboBox_GetExtendedUI
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
 - ComboBox_GetExtendedUI
 - windowsx/ComboBox_GetExtendedUI
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
 - ComboBox_GetExtendedUI
---

# ComboBox_GetExtendedUI macro

## -syntax

```cpp
UINT ComboBox_GetExtendedUI(
   HWND hwndCtl
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Zero if the control is using the default UI, or nonzero if it is using the extended UI.


## -description

Ascertains whether a combo box is using the default user interface (UI) or the extended UI. You can use this macro or send the <a href="/windows/desktop/Controls/cb-getextendedui">CB_GETEXTENDEDUI</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-getextendedui">CB_GETEXTENDEDUI</a>.
