---
UID: NF:windowsx.Static_SetIcon
title: Static_SetIcon macro (windowsx.h)
description: Sets the icon for a static control. You can use this macro or send the STM_SETICON message explicitly.
helpviewer_keywords: ["Static_SetIcon","Static_SetIcon macro [Windows Controls]","_win32_Static_SetIcon","_win32_Static_SetIcon_cpp","controls.Static_SetIcon","controls._win32_Static_SetIcon","windowsx/Static_SetIcon"]
old-location: controls\Static_SetIcon.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_seticon.htm
ms.date: 10/21/2024
ms.keywords: Static_SetIcon, Static_SetIcon macro [Windows Controls], _win32_Static_SetIcon, _win32_Static_SetIcon_cpp, controls.Static_SetIcon, controls._win32_Static_SetIcon, windowsx/Static_SetIcon
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
 - Static_SetIcon
 - windowsx/Static_SetIcon
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
 - Static_SetIcon
---

# Static_SetIcon macro

## -syntax

```cpp
HICON Static_SetIcon(
   HWND  hwndCtl,
   HICON hIcon
);
```

## -returns

Type: **[HICON](/windows/desktop/winprog/windows-data-types)**

A handle to the icon previously associated with the icon control, or zero if an error occurs.


## -description

Sets the icon for a static control. You can use this macro or send the <a href="/windows/desktop/Controls/stm-seticon">STM_SETICON</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param hIcon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a></b>

a handle to the icon.
