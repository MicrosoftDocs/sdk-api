---
UID: NF:winuser.RegisterTouchHitTestingWindow
title: RegisterTouchHitTestingWindow function
author: windows-sdk-content
description: Registers a window to process the WM_TOUCHHITTESTING notification.
old-location: input_touchhittest\registertouchhittestingwindow.htm
old-project: Input_TouchHitTest
ms.assetid: 52e48cea-b5c7-405f-8df6-26052304b62c
ms.author: windowssdkdev
ms.date: 03/27/2018
ms.keywords: RegisterTouchHitTestingWindow, RegisterTouchHitTestingWindow function, input_touchhittest.registertouchhittestingwindow, touch_hittest.registertouchhittestingwindow, winuser/RegisterTouchHitTestingWindow
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - User32.dll
 - Ext-MS-Win-NTUser-Touch-HitTest-l1-1-0.dll
 - MinUser.dll
api_name:
 - RegisterTouchHitTestingWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RegisterTouchHitTestingWindow function


## -description


Registers a window to process the  

<a href="https://msdn.microsoft.com/741F9D67-A914-46CF-91A3-EF40447E7438">WM_TOUCHHITTESTING</a> notification.


## -parameters




### -param hwnd [in]

The window that receives the <a href="https://msdn.microsoft.com/741F9D67-A914-46CF-91A3-EF40447E7438">WM_TOUCHHITTESTING</a>  notification.


### -param value [in]

One of the following values: 

<ul>
<li>
<a href="https://msdn.microsoft.com/D1ECCBFA-CD01-401E-A42E-4F954F5F0A32">TOUCH_HIT_TESTING_CLIENT</a>: Send <a href="https://msdn.microsoft.com/741F9D67-A914-46CF-91A3-EF40447E7438">WM_TOUCHHITTESTING</a>  messages to the target window.</li>
<li>
<a href="https://msdn.microsoft.com/D1ECCBFA-CD01-401E-A42E-4F954F5F0A32">TOUCH_HIT_TESTING_DEFAULT</a>: Don't send <a href="https://msdn.microsoft.com/741F9D67-A914-46CF-91A3-EF40447E7438">WM_TOUCHHITTESTING</a>  messages to the target window but continue to send the messages to child windows.
</li>
<li>
<a href="https://msdn.microsoft.com/D1ECCBFA-CD01-401E-A42E-4F954F5F0A32">TOUCH_HIT_TESTING_NONE</a>: Don't send <a href="https://msdn.microsoft.com/741F9D67-A914-46CF-91A3-EF40447E7438">WM_TOUCHHITTESTING</a>  messages to the target window or child windows.
</li>
</ul>

## -returns



If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

