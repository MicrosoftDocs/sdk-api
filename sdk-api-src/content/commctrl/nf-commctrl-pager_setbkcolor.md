---
UID: NF:commctrl.Pager_SetBkColor
title: Pager_SetBkColor macro (commctrl.h)
description: Sets the current background color for the pager control. You can use this macro or send the PGM_SETBKCOLOR message explicitly.
helpviewer_keywords: ["Pager_SetBkColor","Pager_SetBkColor macro [Windows Controls]","_win32_Pager_SetBkColor","_win32_Pager_SetBkColor_cpp","commctrl/Pager_SetBkColor","controls.Pager_SetBkColor","controls._win32_Pager_SetBkColor"]
old-location: controls\Pager_SetBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setbkcolor.htm
ms.date: 10/21/2024
ms.keywords: Pager_SetBkColor, Pager_SetBkColor macro [Windows Controls], _win32_Pager_SetBkColor, _win32_Pager_SetBkColor_cpp, commctrl/Pager_SetBkColor, controls.Pager_SetBkColor, controls._win32_Pager_SetBkColor
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
 - Pager_SetBkColor
 - commctrl/Pager_SetBkColor
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
 - Pager_SetBkColor
---

# Pager_SetBkColor macro

## -syntax

```cpp
COLORREF Pager_SetBkColor(
   HWND     hwnd,
   COLORREF clr
);
```

## -returns

Type: **[COLORREF](/windows/desktop/winprog/windows-data-types)**

Returns a <b>COLORREF</b> value that contains the previous background color.

## -description

Sets the current background color for the pager control. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-setbkcolor">PGM_SETBKCOLOR</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.

### -param clr

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

<b>COLORREF</b> value that contains the new background color of the pager control.

## -remarks

By default, the pager control will use the system button face color as the background color. This is the same color that can be retrieved by calling <a href="/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush">GetSysColorBrush</a> with COLOR_BTNFACE.
