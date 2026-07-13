---
UID: NF:windowsx.Static_Enable
title: Static_Enable macro (windowsx.h)
description: Enables or disables a static control.
helpviewer_keywords: ["Static_Enable","Static_Enable macro [Windows Controls]","_win32_Static_Enable","_win32_Static_Enable_cpp","controls.Static_Enable","controls._win32_Static_Enable","windowsx/Static_Enable"]
old-location: controls\Static_Enable.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_enable.htm
ms.date: 10/21/2024
ms.keywords: Static_Enable, Static_Enable macro [Windows Controls], _win32_Static_Enable, _win32_Static_Enable_cpp, controls.Static_Enable, controls._win32_Static_Enable, windowsx/Static_Enable
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
 - Static_Enable
 - windowsx/Static_Enable
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
 - Static_Enable
---

# Static_Enable macro

## -syntax

```cpp
BOOL Static_Enable(
   HWND hwndCtl,
   BOOL fEnable
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Zero if the window was previously disabled; otherwise nonzero.


## -description

Enables or disables a static control.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to enable the static control, or <b>FALSE</b> to disable it.
