---
UID: NF:winuser.GetCapture
title: GetCapture function
author: windows-sdk-content
description: Retrieves a handle to the window (if any) that has captured the mouse. Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders.
old-location: inputdev\getcapture.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputfunctions\getcapture.htm
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: GetCapture, GetCapture function [Keyboard and Mouse Input], _win32_GetCapture, _win32_getcapture_cpp, inputdev.getcapture, winui._win32_getcapture, winuser/GetCapture
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Ext-MS-Win-NTUser-mouse-l1-1-0.dll
 - api-ms-win-ntuser-ie-mouse-l1-1-0.dll
 - ie_stubs.dll
api_name:
 - GetCapture
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetCapture function


## -description


Retrieves a handle to the window (if any) that has captured the mouse. Only one window at a time can capture the mouse; this window receives mouse input whether or not the cursor is within its borders. 


## -parameters






## -returns



Type: <b>HWND</b>

The return value is a handle to the capture window associated with the current thread. If no window in the thread has captured the mouse, the return value is <b>NULL</b>. 




## -remarks



A <b>NULL</b> return value means the current thread has not captured the mouse. However, it is possible that another thread or process has captured the mouse. 


				 To get a handle to the capture window on another thread, use the <a href="https://msdn.microsoft.com/863e0735-a2d4-4962-99d8-bb6037770c50">GetGUIThreadInfo</a> function.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/863e0735-a2d4-4962-99d8-bb6037770c50">GetGUIThreadInfo</a>



<a href="https://msdn.microsoft.com/35f5e1ad-74d5-41bb-9016-b1c5de449550">Mouse Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/43e1f766-35b1-451d-9921-c1d4eebc4435">ReleaseCapture</a>



<a href="https://msdn.microsoft.com/f97cf81d-1f4c-4677-8e39-ca23f07aa95d">SetCapture</a>
 

 

