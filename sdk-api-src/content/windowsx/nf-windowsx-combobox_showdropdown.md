---
UID: NF:windowsx.ComboBox_ShowDropdown
title: ComboBox_ShowDropdown macro (windowsx.h)
description: Shows or hides the list in a combo box. You can use this macro or send the CB_SHOWDROPDOWN message explicitly.
helpviewer_keywords: ["ComboBox_ShowDropdown","ComboBox_ShowDropdown macro [Windows Controls]","_win32_ComboBox_ShowDropdown","_win32_ComboBox_ShowDropdown_cpp","controls.ComboBox_ShowDropdown","controls._win32_ComboBox_ShowDropdown","windowsx/ComboBox_ShowDropdown"]
old-location: controls\ComboBox_ShowDropdown.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_showdropdown.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_ShowDropdown, ComboBox_ShowDropdown macro [Windows Controls], _win32_ComboBox_ShowDropdown, _win32_ComboBox_ShowDropdown_cpp, controls.ComboBox_ShowDropdown, controls._win32_ComboBox_ShowDropdown, windowsx/ComboBox_ShowDropdown
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
 - ComboBox_ShowDropdown
 - windowsx/ComboBox_ShowDropdown
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
 - ComboBox_ShowDropdown
---

# ComboBox_ShowDropdown macro

## -syntax

```cpp
BOOL ComboBox_ShowDropdown(
   HWND hwndCtl,
   BOOL fShow
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Always returns <b>TRUE</b>.


## -description

Shows or hides the list in a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-showdropdown">CB_SHOWDROPDOWN</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fShow

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to show the dropdown, or <b>FALSE</b> to hide it.

## -remarks

This macro has no effect on a combo box created with the <a href="/windows/desktop/Controls/combo-box-styles">CBS_SIMPLE</a> style.
