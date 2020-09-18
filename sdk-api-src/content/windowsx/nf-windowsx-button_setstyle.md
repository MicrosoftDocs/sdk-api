---
UID: NF:windowsx.Button_SetStyle
title: Button_SetStyle macro (windowsx.h)
description: Sets the style of a button. You can use this macro or send the BM_SETSTYLE message explicitly.
helpviewer_keywords: ["Button_SetStyle","Button_SetStyle macro [Windows Controls]","_win32_Button_SetStyle","_win32_Button_SetStyle_cpp","controls.Button_SetStyle","controls._win32_Button_SetStyle","windowsx/Button_SetStyle"]
old-location: controls\Button_SetStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_setstyle.htm
ms.date: 12/05/2018
ms.keywords: Button_SetStyle, Button_SetStyle macro [Windows Controls], _win32_Button_SetStyle, _win32_Button_SetStyle_cpp, controls.Button_SetStyle, controls._win32_Button_SetStyle, windowsx/Button_SetStyle
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
 - Button_SetStyle
 - windowsx/Button_SetStyle
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
 - Button_SetStyle
---

# Button_SetStyle macro


## -description

Sets the style of a button. You can use this macro or send the <a href="/windows/desktop/Controls/bm-setstyle">BM_SETSTYLE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param style

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The button style. This parameter can be a combination of button styles. For a table of button styles, see <a href="/windows/desktop/Controls/button-styles">Button Styles</a>.

### -param fRedraw

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to redraw the button; otherwise <b>FALSE</b>.