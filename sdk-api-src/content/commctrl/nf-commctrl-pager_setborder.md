---
UID: NF:commctrl.Pager_SetBorder
title: Pager_SetBorder macro (commctrl.h)
description: Sets the current border size for the pager control. You can use this macro or send the PGM_SETBORDER message explicitly.
helpviewer_keywords: ["Pager_SetBorder","Pager_SetBorder macro [Windows Controls]","_win32_Pager_SetBorder","_win32_Pager_SetBorder_cpp","commctrl/Pager_SetBorder","controls.Pager_SetBorder","controls._win32_Pager_SetBorder"]
old-location: controls\Pager_SetBorder.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setborder.htm
ms.date: 10/21/2024
ms.keywords: Pager_SetBorder, Pager_SetBorder macro [Windows Controls], _win32_Pager_SetBorder, _win32_Pager_SetBorder_cpp, commctrl/Pager_SetBorder, controls.Pager_SetBorder, controls._win32_Pager_SetBorder
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
 - Pager_SetBorder
 - commctrl/Pager_SetBorder
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
 - Pager_SetBorder
---

# Pager_SetBorder macro

## -syntax

```cpp
INT Pager_SetBorder(
   HWND hwnd,
   int  iBorder
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

Returns an INT value that contains the previous border size, in pixels.


## -description

Sets the current border size for the pager control. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-setborder">PGM_SETBORDER</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.

### -param iBorder

Type: <b>int</b>

New size of the border, in pixels. This value should not be larger than the pager button or less than zero. If <i>iBorder</i> is too large, the border will be drawn the same size as the button. If 
<i>iBorder</i> is negative, the border size will be set to zero.
