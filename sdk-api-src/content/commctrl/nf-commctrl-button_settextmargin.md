---
UID: NF:commctrl.Button_SetTextMargin
title: Button_SetTextMargin macro (commctrl.h)
description: Sets the margins for drawing text in a button control. You can use this macro or send the BCM_SETTEXTMARGIN message explicitly.
helpviewer_keywords: ["Button_SetTextMargin","Button_SetTextMargin macro [Windows Controls]","_win32_Button_SetTextMargin","_win32_Button_SetTextMargin_cpp","commctrl/Button_SetTextMargin","controls.Button_SetTextMargin","controls._win32_Button_SetTextMargin"]
old-location: controls\Button_SetTextMargin.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_settextmargin.htm
ms.date: 10/21/2024
ms.keywords: Button_SetTextMargin, Button_SetTextMargin macro [Windows Controls], _win32_Button_SetTextMargin, _win32_Button_SetTextMargin_cpp, commctrl/Button_SetTextMargin, controls.Button_SetTextMargin, controls._win32_Button_SetTextMargin
req.header: commctrl.h
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
 - Button_SetTextMargin
 - commctrl/Button_SetTextMargin
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
 - Button_SetTextMargin
---

# Button_SetTextMargin macro

## -syntax

```cpp
BOOL Button_SetTextMargin(
   HWND hwnd,
   RECT *pmargin
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the macro succeeds, it returns <b>TRUE</b>. Otherwise it returns <b>FALSE</b>.


## -description

Sets the margins for drawing text in a button control. You can use this macro or send the <a href="/windows/desktop/Controls/bcm-settextmargin">BCM_SETTEXTMARGIN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param pmargin

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the margins to set for drawing text in a button control.

## -remarks

To use this macro, you must provide a manifest specifying Comctl32.dll version 6.0. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
