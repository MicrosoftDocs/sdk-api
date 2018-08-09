---
UID: NF:winuser.CloseTouchInputHandle
title: CloseTouchInputHandle function
author: windows-sdk-content
description: Closes a touch input handle, frees process memory associated with it, and invalidates the handle.
old-location: wintouch\closetouchinputhandle.htm
old-project: wintouch
ms.assetid: bdc8bb94-3126-4183-9dfd-ba4844d98f29
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CloseTouchInputHandle, CloseTouchInputHandle function [Windows Touch], wintouch.closetouchinputhandle, winuser/CloseTouchInputHandle
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - CloseTouchInputHandle
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# CloseTouchInputHandle function


## -description


Closes a touch input handle, frees process memory associated with it, and invalidates the handle.


## -parameters




### -param hTouchInput [in]

The touch input handle received in the <b>LPARAM</b> of a touch message. The function fails with <b>ERROR_INVALID_HANDLE</b> if this handle is not valid. Note that the handle is not valid after it has been used in a successful call to <b>CloseTouchInputHandle</b> or after it has been passed to <a href="https://msdn.microsoft.com/9fba2013-17a3-499c-80dc-627e89c0edaf">DefWindowProc, PostMessage, SendMessage</a> or one of their variants.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks



Calling <b>CloseTouchInputHandle</b> will not free memory associated with values retrieved in a call to <a href="https://msdn.microsoft.com/18caab11-9c22-46ac-b89f-dd3e662bea1e">GetTouchInputInfo</a>. Values in structures passed to <b>GetTouchInputInfo</b>  will be valid until you delete them.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/18caab11-9c22-46ac-b89f-dd3e662bea1e">GetTouchInputInfo</a>
 

 

