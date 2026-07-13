---
UID: NF:windowsx.ComboBox_Enable
title: ComboBox_Enable macro (windowsx.h)
description: Enables or disables a combo box control.
helpviewer_keywords: ["ComboBox_Enable","ComboBox_Enable macro [Windows Controls]","_win32_ComboBox_Enable","_win32_ComboBox_Enable_cpp","controls.ComboBox_Enable","controls._win32_ComboBox_Enable","windowsx/ComboBox_Enable"]
old-location: controls\ComboBox_Enable.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_enable.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_Enable, ComboBox_Enable macro [Windows Controls], _win32_ComboBox_Enable, _win32_ComboBox_Enable_cpp, controls.ComboBox_Enable, controls._win32_ComboBox_Enable, windowsx/ComboBox_Enable
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
 - ComboBox_Enable
 - windowsx/ComboBox_Enable
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
 - ComboBox_Enable
---

# ComboBox_Enable macro

## -syntax

```cpp
BOOL ComboBox_Enable(
   HWND hwndCtl,
   BOOL fEnable
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if the window was previously disabled, or <b>FALSE</b> if it was previously enabled.


## -description

Enables or disables a combo box control.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to enable the control, or <b>FALSE</b> to disable it.
