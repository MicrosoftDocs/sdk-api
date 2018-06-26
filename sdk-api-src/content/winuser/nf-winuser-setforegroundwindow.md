---
UID: NF:winuser.SetForegroundWindow
title: SetForegroundWindow function
author: windows-sdk-content
description: Brings the thread that created the specified window into the foreground and activates the window.
old-location: winmsg\setforegroundwindow.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\setforegroundwindow.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: SetForegroundWindow, SetForegroundWindow function [Windows and Messages], _win32_SetForegroundWindow, _win32_setforegroundwindow_cpp, winmsg.setforegroundwindow, winui._win32_setforegroundwindow, winuser/SetForegroundWindow
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
 - SetForegroundWindow
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SetForegroundWindow function


## -description


Brings the thread that created the specified window into the foreground and activates the window. Keyboard input is directed to the window, and various visual cues are changed for the user. The system assigns a slightly higher priority to the thread that created the foreground window than it does to other threads. 


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window that should be activated and brought to the foreground. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the window was brought to the foreground, the return value is nonzero.
                    
                    

If the window was not brought to the foreground, the return value is zero.




## -remarks



 The system restricts which processes can set the foreground window. A process can set the foreground window only if one of the following conditions is true:

				

<ul>
<li>The process is the foreground process.</li>
<li>The process was started by the foreground process.</li>
<li>The process received the last input event.</li>
<li>There is no foreground process.</li>
<li>The process is being debugged.</li>
<li>The foreground process is not a Modern Application or the Start Screen.</li>
<li>The foreground is not locked (see <a href="https://msdn.microsoft.com/86628916-34ba-4988-bdec-4111f0d29810">LockSetForegroundWindow</a>).</li>
<li>The foreground lock time-out has expired (see <b>SPI_GETFOREGROUNDLOCKTIMEOUT</b> in <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>).</li>
<li>No menus are active.</li>
</ul>
An application cannot force a window to the foreground while the user is working with another window. Instead, Windows flashes the taskbar button of the window to notify the user.

A process that can set the foreground window can enable another process to set the foreground window by calling the <a href="https://msdn.microsoft.com/2d20519e-4d21-4722-8e26-bab933763326">AllowSetForegroundWindow</a> function. The process specified by <i>dwProcessId</i> loses the ability to set the foreground window the next time the user generates input, unless the input is directed at that process, or the next time a process calls <b>AllowSetForegroundWindow</b>, unless that process is specified. 

The foreground process can disable calls to <b>SetForegroundWindow</b> by calling the <a href="https://msdn.microsoft.com/86628916-34ba-4988-bdec-4111f0d29810">LockSetForegroundWindow</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/2d20519e-4d21-4722-8e26-bab933763326">AllowSetForegroundWindow</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/474ec2d9-3ee9-4622-843e-d6ae36fedd7f">FlashWindowEx</a>



<a href="https://msdn.microsoft.com/ee30a5fc-a229-4b84-b1f7-2d071d641a22">GetForegroundWindow</a>



<a href="https://msdn.microsoft.com/86628916-34ba-4988-bdec-4111f0d29810">LockSetForegroundWindow</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3a761bd3-5eba-4263-b670-405d91996a89">SetActiveWindow</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

