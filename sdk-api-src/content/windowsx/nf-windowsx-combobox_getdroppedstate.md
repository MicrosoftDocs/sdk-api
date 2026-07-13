---
UID: NF:windowsx.ComboBox_GetDroppedState
title: ComboBox_GetDroppedState macro (windowsx.h)
description: Ascertains whether the drop list in a combo box control is visible. You can use this macro or send the CB_GETDROPPEDSTATE message explicitly.
helpviewer_keywords: ["ComboBox_GetDroppedState","ComboBox_GetDroppedState macro [Windows Controls]","_win32_ComboBox_GetDroppedState","_win32_ComboBox_GetDroppedState_cpp","controls.ComboBox_GetDroppedState","controls._win32_ComboBox_GetDroppedState","windowsx/ComboBox_GetDroppedState"]
old-location: controls\ComboBox_GetDroppedState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getdroppedstate.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetDroppedState, ComboBox_GetDroppedState macro [Windows Controls], _win32_ComboBox_GetDroppedState, _win32_ComboBox_GetDroppedState_cpp, controls.ComboBox_GetDroppedState, controls._win32_ComboBox_GetDroppedState, windowsx/ComboBox_GetDroppedState
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
 - ComboBox_GetDroppedState
 - windowsx/ComboBox_GetDroppedState
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
 - ComboBox_GetDroppedState
---

# ComboBox_GetDroppedState macro

## -syntax

```cpp
BOOL ComboBox_GetDroppedState(
   HWND hwndCtl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if the drop list is visible; otherwise <b>FALSE</b>.


## -description

Ascertains whether the drop list in a combo box control is visible. You can use this macro or send the <a href="/windows/desktop/Controls/cb-getdroppedstate">CB_GETDROPPEDSTATE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the combo box control.
