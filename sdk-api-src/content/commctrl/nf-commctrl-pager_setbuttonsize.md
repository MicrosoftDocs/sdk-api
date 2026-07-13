---
UID: NF:commctrl.Pager_SetButtonSize
title: Pager_SetButtonSize macro (commctrl.h)
description: Sets the current button size for the pager control. You can use this macro or send the PGM_SETBUTTONSIZE message explicitly.
helpviewer_keywords: ["Pager_SetButtonSize","Pager_SetButtonSize macro [Windows Controls]","_win32_Pager_SetButtonSize","_win32_Pager_SetButtonSize_cpp","commctrl/Pager_SetButtonSize","controls.Pager_SetButtonSize","controls._win32_Pager_SetButtonSize"]
old-location: controls\Pager_SetButtonSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setbuttonsize.htm
ms.date: 10/21/2024
ms.keywords: Pager_SetButtonSize, Pager_SetButtonSize macro [Windows Controls], _win32_Pager_SetButtonSize, _win32_Pager_SetButtonSize_cpp, commctrl/Pager_SetButtonSize, controls.Pager_SetButtonSize, controls._win32_Pager_SetButtonSize
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
 - Pager_SetButtonSize
 - commctrl/Pager_SetButtonSize
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
 - Pager_SetButtonSize
---

# Pager_SetButtonSize macro

## -syntax

```cpp
int Pager_SetButtonSize(
   HWND hwnd,
   int  iSize
);
```

## -returns

Type: **int**

Returns an <b>int</b> value that contains the previous button size, in pixels.


## -description

Sets the current button size for the pager control. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-setbuttonsize">PGM_SETBUTTONSIZE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.

### -param iSize

Type: <b>int</b>

Value of type <b>int</b> that contains the new button size, in pixels.

## -remarks

If the pager control has the <a href="/windows/desktop/Controls/pager-control-styles">PGS_HORZ</a> style, the button size determines the width of the pager buttons. If the pager control has the <a href="/windows/desktop/Controls/pager-control-styles">PGS_VERT</a> style, the button size determines the height of the pager buttons. By default, the pager control sets its button size to three-fourths of the width of the scroll bar.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-pager_getbuttonsize">Pager_GetButtonSize</a>
