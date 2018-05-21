---
UID: NF:winuser.FlashWindow
title: FlashWindow function
author: windows-driver-content
description: Flashes the specified window one time. It does not change the active state of the window.
old-location: base\flashwindow.htm
old-project: Debug
ms.assetid: c4af997d-5cb8-4d5d-ae8d-1e0cc724fe02
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: FlashWindow, FlashWindow function, _win32_flashwindow, base.flashwindow, winuser/FlashWindow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	User32.dll
api_name:
-	FlashWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# FlashWindow function


## -description


Flashes the specified window one time. It does not change the active state of the window.

To flash the window a specified number of times, use the 
<a href="https://msdn.microsoft.com/474ec2d9-3ee9-4622-843e-d6ae36fedd7f">FlashWindowEx</a> function.


## -parameters




### -param hWnd [in]

A handle to the window to be flashed. The window can be either open or minimized.


### -param bInvert [in]

If this parameter is <b>TRUE</b>, the window is flashed from one state to the other. If it is <b>FALSE</b>, the window is returned to its original state (either active or inactive). 




When an application is minimized and this parameter is <b>TRUE</b>, the taskbar window button flashes active/inactive. If it is <b>FALSE</b>, the taskbar window button flashes inactive, meaning that it does not change colors. It flashes, as if it were being redrawn, but it does not provide the visual invert clue to the user.


## -returns



The return value specifies the window's state before the call to the 
<b>FlashWindow</b> function. If the window caption was drawn as active before the call, the return value is nonzero. Otherwise, the return value is zero.




## -remarks



Flashing a window means changing the appearance of its caption bar as if the window were changing from inactive to active status, or vice versa. (An inactive caption bar changes to an active caption bar; an active caption bar changes to an inactive caption bar.)

Typically, a window is flashed to inform the user that the window requires attention but that it does not currently have the keyboard focus.

The 
<b>FlashWindow</b> function flashes the window only once; for repeated flashing, the application should create a system timer.




## -see-also




<a href="https://msdn.microsoft.com/ae8ad3a2-1f1a-46d6-adaa-74c50c07dcc5">Error Handling Functions</a>



<a href="https://msdn.microsoft.com/35b6e93c-323a-4592-9394-a2e9dd79d9e6">Notifying the User</a>
 

 

