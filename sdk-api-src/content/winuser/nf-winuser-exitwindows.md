---
UID: NF:winuser.ExitWindows
title: ExitWindows macro (winuser.h)
author: windows-sdk-content
description: Calls the ExitWindowsEx function to log off the interactive user.
old-location: base\exitwindows.htm
tech.root: Shutdown
ms.assetid: 7c76caac-459d-45df-ae00-bc208a9e7b22
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExitWindows, ExitWindows macro, _win32_exitwindows, base.exitwindows, winuser/ExitWindows
ms.topic: macro
f1_keywords: 
 - "winuser/ExitWindows"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - ExitWindows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ExitWindows macro


## -description


Calls the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> function to log off the interactive user. Applications should call <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a> directly.


## -parameters




### -param dwReserved

This parameter must be zero.


### -param Code

This parameter must be zero.


## -remarks



The system sends a <a href="https://docs.microsoft.com/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> to the main window of each running application.

An application agrees to terminate by returning <b>TRUE</b> when it receives this message (or by allowing the 
<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a> function to process the message). If any application returns <b>FALSE</b> when it receives the 
<a href="https://docs.microsoft.com/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> message, the logoff is canceled.

After the system processes the results of the 
<a href="https://docs.microsoft.com/windows/desktop/Shutdown/wm-queryendsession">WM_QUERYENDSESSION</a> message, it sends the 
<a href="https://docs.microsoft.com/windows/desktop/Shutdown/wm-endsession">WM_ENDSESSION</a> message with the <i>wParam</i> parameter set to <b>TRUE</b> if the system is shutting down and to <b>FALSE</b> if it is not.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/Shutdown/how-to-log-off-the-current-user">How to Log Off the Current User</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-defwindowproca">DefWindowProc</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-exitwindowsex">ExitWindowsEx</a>



<a href="https://docs.microsoft.com/windows/desktop/Shutdown/logging-off">Logging Off</a>



<a href="https://docs.microsoft.com/windows/desktop/Shutdown/system-shutdown-functions">System Shutdown
		  Functions</a>
 

 

