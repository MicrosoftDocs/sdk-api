---
UID: NF:windowsx.Button_SetState
title: Button_SetState macro (windowsx.h)
description: Sets the highlight state of a button. The highlight state indicates whether the button is highlighted as if the user had pushed it. You can use this macro or send the BM_SETSTATE message explicitly.
helpviewer_keywords: ["Button_SetState","Button_SetState macro [Windows Controls]","_win32_Button_SetState","_win32_Button_SetState_cpp","controls.Button_SetState","controls._win32_Button_SetState","windowsx/Button_SetState"]
old-location: controls\Button_SetState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setstate.htm
ms.date: 12/05/2018
ms.keywords: Button_SetState, Button_SetState macro [Windows Controls], _win32_Button_SetState, _win32_Button_SetState_cpp, controls.Button_SetState, controls._win32_Button_SetState, windowsx/Button_SetState
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
 - Button_SetState
 - windowsx/Button_SetState
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
 - Button_SetState
---

# Button_SetState macro


## -description

Sets the highlight state of a button. The highlight state indicates whether the button is highlighted as if the user had pushed it. You can use this macro or send the <a href="/windows/desktop/Controls/bm-setstate">BM_SETSTATE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param state

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to highlight the button; otherwise <b>FALSE</b>.

## -remarks

Highlighting  affects only the appearance of a button. It has no effect on the check state of a radio button or check box. 

A button is automatically highlighted when the user positions the cursor over it and presses and holds the left mouse button. The highlighting is removed when the user releases the mouse button.