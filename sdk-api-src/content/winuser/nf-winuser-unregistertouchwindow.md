---
UID: NF:winuser.UnregisterTouchWindow
title: UnregisterTouchWindow function
author: windows-sdk-content
description: Registers a window as no longer being touch-capable.
old-location: wintouch\unregistertouchwindow.htm
old-project: wintouch
ms.assetid: 19b83312-b52b-45a5-9595-23d4621c4342
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: UnregisterTouchWindow, UnregisterTouchWindow function [Windows Touch], wintouch.unregistertouchwindow, winuser/UnregisterTouchWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	user32.dll
api_name:
-	UnregisterTouchWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UnregisterTouchWindow function


## -description


Registers a window as no longer being touch-capable.


## -parameters




### -param hwnd

TBD




#### - hWnd [in]

The handle of the window. The function fails with <b>ERROR_ACCESS_DENIED</b> if the calling thread does not own the specified window.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks



The <b>UnregisterTouchWindow</b>  function succeeds even if the specified window was not previously registered as being touch-capable.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/a70a7418-f79d-40c8-9219-3ce38a74da9f">RegisterTouchWindow</a>
 

 

