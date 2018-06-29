---
UID: NF:winuser.GetForegroundWindow
title: GetForegroundWindow function
author: windows-sdk-content
description: Retrieves a handle to the foreground window (the window with which the user is currently working). The system assigns a slightly higher priority to the thread that creates the foreground window than it does to other threads.
old-location: winmsg\getforegroundwindow.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getforegroundwindow.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: GetForegroundWindow, GetForegroundWindow function [Windows and Messages], _win32_GetForegroundWindow, _win32_getforegroundwindow_cpp, winmsg.getforegroundwindow, winui._win32_getforegroundwindow, winuser/GetForegroundWindow
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
req.typenames: POINTER_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetForegroundWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetForegroundWindow function


## -description


Retrieves a handle to the foreground window (the window with which the user is currently working). The system assigns a slightly higher priority to the thread that creates the foreground window than it does to other threads. 


## -parameters






## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

The return value is a handle to the foreground window. The foreground window can be <b>NULL</b> in certain circumstances, such as when a window is losing activation. 




## -see-also




<b>Conceptual</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms633539(v=VS.85).aspx">SetForegroundWindow</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

