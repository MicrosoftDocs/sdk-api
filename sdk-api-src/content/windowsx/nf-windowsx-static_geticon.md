---
UID: NF:windowsx.Static_GetIcon
title: Static_GetIcon macro (windowsx.h)
description: Retrieves a handle to the icon associated with a static control that has the SS_ICON style. You can use this macro or send the STM_GETICON message explicitly.
helpviewer_keywords: ["Static_GetIcon","Static_GetIcon macro [Windows Controls]","_win32_Static_GetIcon","_win32_Static_GetIcon_cpp","controls.Static_GetIcon","controls._win32_Static_GetIcon","windowsx/Static_GetIcon"]
old-location: controls\Static_GetIcon.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_geticon.htm
ms.date: 10/21/2024
ms.keywords: Static_GetIcon, Static_GetIcon macro [Windows Controls], _win32_Static_GetIcon, _win32_Static_GetIcon_cpp, controls.Static_GetIcon, controls._win32_Static_GetIcon, windowsx/Static_GetIcon
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
 - Static_GetIcon
 - windowsx/Static_GetIcon
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
 - Static_GetIcon
---

# Static_GetIcon macro

## -syntax

```cpp
HICON Static_GetIcon(
   HWND  hwndCtl
   HICON hIcon
);
```

## -returns

Type: **[HICON](/windows/desktop/winprog/windows-data-types)**

A handle to the icon, or <b>NULL</b> if the static control has no associated icon or if an error occurred.


## -description

Retrieves a handle to the icon associated with a static control that has the SS_ICON style. You can use this macro or send the <a href="/windows/desktop/Controls/stm-geticon">STM_GETICON</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param hIcon

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HICON</a></b>

A handle to the icon.
