---
UID: NF:commctrl.Button_GetTextMargin
title: Button_GetTextMargin macro (commctrl.h)
description: Gets the margins used to draw text in a button control. You can use this macro or send the BCM_GETTEXTMARGIN message explicitly.
helpviewer_keywords: ["Button_GetTextMargin","Button_GetTextMargin macro [Windows Controls]","_win32_Button_GetTextMargin","_win32_Button_GetTextMargin_cpp","commctrl/Button_GetTextMargin","controls.Button_GetTextMargin","controls._win32_Button_GetTextMargin"]
old-location: controls\Button_GetTextMargin.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_gettextmargin.htm
ms.date: 10/21/2024
ms.keywords: Button_GetTextMargin, Button_GetTextMargin macro [Windows Controls], _win32_Button_GetTextMargin, _win32_Button_GetTextMargin_cpp, commctrl/Button_GetTextMargin, controls.Button_GetTextMargin, controls._win32_Button_GetTextMargin
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
 - Button_GetTextMargin
 - commctrl/Button_GetTextMargin
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
 - Button_GetTextMargin
---

# Button_GetTextMargin macro

## -syntax

```cpp
BOOL Button_GetTextMargin(
   HWND  hwnd,
   RECT* pmargin
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the macro succeeds, it returns <b>TRUE</b>. Otherwise it returns <b>FALSE</b>.


## -description

Gets the margins used to draw text in a button control. You can use this macro or send the <a href="/windows/desktop/Controls/bcm-gettextmargin">BCM_GETTEXTMARGIN</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param pmargin

Type: <b>RECT*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the margins to use for drawing text in a button control.

## -remarks

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comctl32.dll version 6.0. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>
