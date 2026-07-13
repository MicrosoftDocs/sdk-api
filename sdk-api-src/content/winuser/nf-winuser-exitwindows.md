---
UID: NF:winuser.ExitWindows
title: ExitWindows macro (winuser.h)
description: Calls the ExitWindowsEx function to log off the interactive user.
helpviewer_keywords: ["ExitWindows","ExitWindows macro","_win32_exitwindows","base.exitwindows","winuser/ExitWindows"]
old-location: base\exitwindows.htm
tech.root: base
ms.assetid: 7c76caac-459d-45df-ae00-bc208a9e7b22
ms.date: 07/01/2025
ms.keywords: ExitWindows, ExitWindows macro, _win32_exitwindows, base.exitwindows, winuser/ExitWindows
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - ExitWindows
 - winuser/ExitWindows
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ExitWindows
---

# ExitWindows macro

## -syntax

```cpp
BOOL ExitWindows(
    DWORD dwReserved,
    UINT Code
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the call succeeds, the return value is nonzero. If the call fails, the return value is zero. To get extended error information, call **GetLastError**.


## -description

Calls the <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> function to log off the interactive user. Applications should call <a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> directly.

## -parameters

### -param dwReserved

This parameter must be zero.

### -param Code

This parameter must be zero.

## -remarks

The system sends a <a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> to the main window of each running application.

An application agrees to terminate by returning <b>TRUE</b> when it receives this message (or by allowing the 
<a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to process the message). If any application returns <b>FALSE</b> when it receives the 
<a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> message, the logoff is canceled.

After the system processes the results of the 
<a href="/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> message, it sends the 
<a href="/windows/desktop/Shutdown/wm-endsession">WM_ENDSESSION</a> message with the <i>wParam</i> parameter set to <b>TRUE</b> if the system is shutting down and to <b>FALSE</b> if it is not.


#### Examples

For an example, see 
<a href="/windows/desktop/Shutdown/how-to-log-off-the-current-user">How to Log Off the Current User</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>



<a href="/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>



<a href="/windows/desktop/Shutdown/logging-off">Logging Off</a>



<a href="/windows/desktop/Shutdown/system-shutdown-functions">System Shutdown
		  Functions</a>
