---
UID: NF:commctrl.Button_SetDropDownState
title: Button_SetDropDownState macro (commctrl.h)
description: Sets the drop down state for a specified button with style of BS_SPLITBUTTON. Use this macro or send the BCM_SETDROPDOWNSTATE message explicitly.
helpviewer_keywords: ["Button_SetDropDownState","Button_SetDropDownState macro [Windows Controls]","_shell_Button_SetDropDownState","_shell_Button_SetDropDownState_cpp","commctrl/Button_SetDropDownState","controls.Button_SetDropDownState","controls._shell_Button_SetDropDownState"]
old-location: controls\Button_SetDropDownState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setdropdownstate.htm
ms.date: 10/21/2024
ms.keywords: Button_SetDropDownState, Button_SetDropDownState macro [Windows Controls], _shell_Button_SetDropDownState, _shell_Button_SetDropDownState_cpp, commctrl/Button_SetDropDownState, controls.Button_SetDropDownState, controls._shell_Button_SetDropDownState
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Button_SetDropDownState
 - commctrl/Button_SetDropDownState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Button_SetDropDownState
---

# Button_SetDropDownState macro

## -syntax

```cpp
BOOL Button_SetDropDownState(
  [in] HWND hwnd,
  [in] BOOL fDropDown
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets the drop down state for a specified button with style of <a href="/windows/desktop/Controls/button-styles">BS_SPLITBUTTON</a>. Use this macro or send the <a href="/windows/desktop/Controls/bcm-setdropdownstate">BCM_SETDROPDOWNSTATE</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param fDropDown [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> for state of  BST_DROPDOWNPUSHED, or <b>FALSE</b> otherwise.
