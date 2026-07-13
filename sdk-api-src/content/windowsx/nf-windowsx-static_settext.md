---
UID: NF:windowsx.Static_SetText
title: Static_SetText macro (windowsx.h)
description: Sets the text of a static control.
helpviewer_keywords: ["Static_SetText","Static_SetText macro [Windows Controls]","_win32_Static_SetText","_win32_Static_SetText_cpp","controls.Static_SetText","controls._win32_Static_SetText","windowsx/Static_SetText"]
old-location: controls\Static_SetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_settext.htm
ms.date: 10/21/2024
ms.keywords: Static_SetText, Static_SetText macro [Windows Controls], _win32_Static_SetText, _win32_Static_SetText_cpp, controls.Static_SetText, controls._win32_Static_SetText, windowsx/Static_SetText
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
 - Static_SetText
 - windowsx/Static_SetText
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
 - Static_SetText
---

# Static_SetText macro

## -syntax

```cpp
int Static_SetText(
   HWND   hwndCtl,
   LPTSTR lpsz
);
```

## -returns

Type: **int**

If the function succeeds, the return value is nonzero. If it fails, the return value is zero.


## -description

Sets the text of a static control.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lpsz

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a null-terminated string to be used as the static control text.

## -remarks

The macro expands to a call to <a href="/windows/desktop/api/winuser/nf-winuser-setwindowtexta">SetWindowText</a>.
