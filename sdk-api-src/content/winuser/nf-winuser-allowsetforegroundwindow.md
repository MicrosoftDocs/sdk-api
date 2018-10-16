---
UID: NF:winuser.AllowSetForegroundWindow
title: AllowSetForegroundWindow function
author: windows-sdk-content
description: Enables the specified process to set the foreground window using the SetForegroundWindow function. The calling process must already be able to set the foreground window. For more information, see Remarks later in this topic.
old-location: winmsg\allowsetforegroundwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\allowsetforegroundwindow.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: AllowSetForegroundWindow, AllowSetForegroundWindow function [Windows and Messages], _win32_AllowSetForegroundWindow, _win32_allowsetforegroundwindow_cpp, winmsg.allowsetforegroundwindow, winui._win32_allowsetforegroundwindow, winuser/AllowSetForegroundWindow
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
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
 - AllowSetForegroundWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AllowSetForegroundWindow function


## -description


Enables the specified process to set the foreground window using the <a href="https://msdn.microsoft.com/c728ff42-1a5e-45c9-b2ab-5e28ad430a2d">SetForegroundWindow</a> function. The calling process must already be able to set the foreground window. For more information, see Remarks later in this topic.


## -parameters




### -param dwProcessId [in]

Type: <b>DWORD</b>

The identifier of the process that will be enabled to set the foreground window. If this parameter is <b>ASFW_ANY</b>, all processes will be enabled to set the foreground window. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. The function will fail if the calling process cannot set the foreground window. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The system restricts which processes can set the foreground window. A process can set the foreground window only if one of the following conditions is true: 

<ul>
<li>The process is the foreground process. </li>
<li>The process was started by the foreground process. </li>
<li>The process received the last input event. </li>
<li>There is no foreground process. </li>
<li>The foreground process is being debugged. </li>
<li>The foreground is not locked (see <a href="https://msdn.microsoft.com/86628916-34ba-4988-bdec-4111f0d29810">LockSetForegroundWindow</a>). </li>
<li>The foreground lock time-out has expired (see <b>SPI_GETFOREGROUNDLOCKTIMEOUT</b> in <a href="https://msdn.microsoft.com/9b99465c-e12d-413c-8e69-b46b52f2f11f">SystemParametersInfo</a>). </li>
<li>No menus are active. </li>
</ul>
A process that can set the foreground window can enable another process to set the foreground window by calling <b>AllowSetForegroundWindow</b>. The process specified by <i>dwProcessId</i> loses the ability to set the foreground window the next time the user generates input, unless the input is directed at that process, or the next time a process calls <b>AllowSetForegroundWindow</b>, unless that process is specified. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/86628916-34ba-4988-bdec-4111f0d29810">LockSetForegroundWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/c728ff42-1a5e-45c9-b2ab-5e28ad430a2d">SetForegroundWindow</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

