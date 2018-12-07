---
UID: NF:winuser.ExitWindows
title: ExitWindows macro
author: windows-sdk-content
description: Calls the ExitWindowsEx function to log off the interactive user.
old-location: base\exitwindows.htm
tech.root: Shutdown
ms.assetid: 7c76caac-459d-45df-ae00-bc208a9e7b22
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ExitWindows, ExitWindows macro, _win32_exitwindows, base.exitwindows, winuser/ExitWindows
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ExitWindows macro


## -description


Calls the <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a> function to log off the interactive user. Applications should call <a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a> directly.


## -parameters




### -param dwReserved

This parameter must be zero.


### -param Code

This parameter must be zero.


## -remarks



The system sends a <a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> to the main window of each running application.

An application agrees to terminate by returning <b>TRUE</b> when it receives this message (or by allowing the 
<a href="https://msdn.microsoft.com/en-us/library/ms633572(v=VS.85).aspx">DefWindowProc</a> function to process the message). If any application returns <b>FALSE</b> when it receives the 
<a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> message, the logoff is canceled.

After the system processes the results of the 
<a href="https://msdn.microsoft.com/7ad73444-f1f6-4b73-8450-0580b146a5a6">WM_QUERYENDSESSION</a> message, it sends the 
<a href="https://msdn.microsoft.com/9bf04f24-da1e-4680-a47b-28e9c500635e">WM_ENDSESSION</a> message with the <i>wParam</i> parameter set to <b>TRUE</b> if the system is shutting down and to <b>FALSE</b> if it is not.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/74be3505-c4bd-4ae2-aaed-700382839006">How to Log Off the Current User</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms633572(v=VS.85).aspx">DefWindowProc</a>



<a href="https://msdn.microsoft.com/f44ccb66-10bd-4ee6-93e1-16948cf10e50">ExitWindowsEx</a>



<a href="https://msdn.microsoft.com/906d92f1-7cbe-454e-9c71-34b4383aebab">Logging Off</a>



<a href="https://msdn.microsoft.com/6a08a769-1acf-49eb-ba95-beaf56a374bf">System Shutdown
		  Functions</a>
 

 

