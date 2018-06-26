---
UID: NF:winuser.GetKeyboardState
title: GetKeyboardState function
author: windows-sdk-content
description: Copies the status of the 256 virtual keys to the specified buffer.
old-location: inputdev\getkeyboardstate.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeyboardstate.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetKeyboardState, GetKeyboardState function [Keyboard and Mouse Input], _win32_GetKeyboardState, _win32_getkeyboardstate_cpp, inputdev.getkeyboardstate, winui._win32_getkeyboardstate, winuser/GetKeyboardState
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
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - api-ms-win-ntuser-ie-keyboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Rawinput-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetKeyboardState
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetKeyboardState function


## -description


Copies the status of the 256 virtual keys to the specified buffer. 


## -parameters




### -param lpKeyState [out]

Type: <b>PBYTE</b>

The 256-byte array that receives the status data for each virtual key. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



An application can call this function to retrieve the current status of all the virtual keys. The status changes as a thread removes keyboard messages from its message queue. The status does not change as keyboard messages are posted to the thread's message queue, nor does it change as keyboard messages are posted to or retrieved from message queues of other threads. (Exception: Threads that are connected through <a href="https://msdn.microsoft.com/0c343fab-56ae-4c70-a79e-0c5f827158a3">AttachThreadInput</a> share the same keyboard state.)

When the function returns, each member of the array pointed to by the 
				<i>lpKeyState</i> parameter contains status data for a virtual key. If the high-order bit is 1, the key is down; otherwise, it is up. If the key is a toggle key, for example CAPS LOCK, then the low-order bit is 1 when the key is toggled and is 0 if the key is untoggled.  The low-order bit is meaningless for non-toggle keys. A toggle key is said to be toggled when it is turned on.
A toggle key's indicator light (if any) on the keyboard will be on when the key is toggled, and off when the key is untoggled. 

To retrieve status information for an individual key, use the <a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a> function. To retrieve the current state for an individual key regardless of whether the corresponding keyboard message has been retrieved from the message queue, use the <a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a> function.

An application can use the virtual-key code constants <b>VK_SHIFT</b>, <b>VK_CONTROL</b> and <b>VK_MENU</b> as indices into the array pointed to by 
				<i>lpKeyState</i>. This gives the status of the SHIFT, CTRL, or ALT keys without distinguishing between left and right. An application can also use the following virtual-key code constants as indices to distinguish between the left and right instances of those keys: 

<table class="clsStd">
<tr>
<td><b>VK_LSHIFT</b></td>
</tr>
<tr>
<td><b>VK_RSHIFT</b></td>
</tr>
<tr>
<td><b>VK_LCONTROL</b></td>
</tr>
<tr>
<td><b>VK_RCONTROL</b></td>
</tr>
<tr>
<td><b>VK_LMENU</b></td>
</tr>
<tr>
<td><b>VK_RMENU</b></td>
</tr>
</table>
 

These left- and right-distinguishing constants are available to an application only through the <b>GetKeyboardState</b>, <a href="https://msdn.microsoft.com/9c34dd1f-b423-4dcd-b29e-8bf64be57472">SetKeyboardState</a>, <a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a>, <a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a>, and <a href="https://msdn.microsoft.com/d287c66d-def1-4794-a95b-fa7c93e7bd35">MapVirtualKey</a> functions. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<a href="https://msdn.microsoft.com/d287c66d-def1-4794-a95b-fa7c93e7bd35">MapVirtualKey</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9c34dd1f-b423-4dcd-b29e-8bf64be57472">SetKeyboardState</a>
 

 

