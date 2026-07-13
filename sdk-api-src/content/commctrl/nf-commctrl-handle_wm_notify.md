---
UID: NF:commctrl.HANDLE_WM_NOTIFY
title: HANDLE_WM_NOTIFY macro (commctrl.h)
description: Calls a function that processes the WM_NOTIFY message.
helpviewer_keywords: ["HANDLE_WM_NOTIFY","HANDLE_WM_NOTIFY macro [Windows Controls]","_win32_HANDLE_WM_NOTIFY","_win32_HANDLE_WM_NOTIFY_cpp","commctrl/HANDLE_WM_NOTIFY","controls.HANDLE_WM_NOTIFY","controls._win32_HANDLE_WM_NOTIFY"]
old-location: controls\HANDLE_WM_NOTIFY.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\handle_wm_notify.htm
ms.date: 10/21/2024
ms.keywords: HANDLE_WM_NOTIFY, HANDLE_WM_NOTIFY macro [Windows Controls], _win32_HANDLE_WM_NOTIFY, _win32_HANDLE_WM_NOTIFY_cpp, commctrl/HANDLE_WM_NOTIFY, controls.HANDLE_WM_NOTIFY, controls._win32_HANDLE_WM_NOTIFY
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
 - HANDLE_WM_NOTIFY
 - commctrl/HANDLE_WM_NOTIFY
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
 - HANDLE_WM_NOTIFY
---

# HANDLE_WM_NOTIFY macro

## -syntax

```cpp
void HANDLE_WM_NOTIFY(
   HWND     hwnd,
   WPARAM   wParam,
   LPARAM   lParam,
   function fn
);
```

## -description

Calls a function that processes the <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a> message.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that received <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>.

### -param wParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WPARAM</a></b>

The first parameter of <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>.

### -param lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The second parameter of <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>.

### -param fn

Type: <b>function</b>

The function that is to process <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>.

## -remarks

The <b>HANDLE_WM_NOTIFY</b> macro is defined as follows. 


``` syntax
#define HANDLE_WM_NOTIFY(hwnd, wParam, lParam, fn) \ 

    (fn)((hwnd), (int)(wParam), (NMHDR*)(lParam))
```

The macro can be used inside a dialog window procedure to simplify the calling of an application-defined function that requires an <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> parameter.
