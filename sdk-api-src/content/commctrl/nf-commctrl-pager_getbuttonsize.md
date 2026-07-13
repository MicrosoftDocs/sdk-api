---
UID: NF:commctrl.Pager_GetButtonSize
title: Pager_GetButtonSize macro (commctrl.h)
description: Retrieves the current button size for the pager control. You can use this macro or send the PGM_GETBUTTONSIZE message explicitly.
helpviewer_keywords: ["Pager_GetButtonSize","Pager_GetButtonSize macro [Windows Controls]","_win32_Pager_GetButtonSize","_win32_Pager_GetButtonSize_cpp","commctrl/Pager_GetButtonSize","controls.Pager_GetButtonSize","controls._win32_Pager_GetButtonSize"]
old-location: controls\Pager_GetButtonSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getbuttonsize.htm
ms.date: 10/21/2024
ms.keywords: Pager_GetButtonSize, Pager_GetButtonSize macro [Windows Controls], _win32_Pager_GetButtonSize, _win32_Pager_GetButtonSize_cpp, commctrl/Pager_GetButtonSize, controls.Pager_GetButtonSize, controls._win32_Pager_GetButtonSize
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
 - Pager_GetButtonSize
 - commctrl/Pager_GetButtonSize
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
 - Pager_GetButtonSize
---

# Pager_GetButtonSize macro

## -syntax

```cpp
int Pager_GetButtonSize(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns an <b>int</b> value that contains the current button size, in pixels.


## -description

Retrieves the current button size for the pager control. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-getbuttonsize">PGM_GETBUTTONSIZE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-pager_setbuttonsize">Pager_SetButtonSize</a>
