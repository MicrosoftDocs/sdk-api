---
UID: NF:winuser.GetKeyState
title: GetKeyState function
author: windows-sdk-content
description: Retrieves the status of the specified virtual key. The status specifies whether the key is up, down, or toggled (on, off&#8212;alternating each time the key is pressed).
old-location: inputdev\getkeystate.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeystate.htm
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: GetKeyState, GetKeyState function [Keyboard and Mouse Input], _win32_GetKeyState, _win32_getkeystate_cpp, inputdev.getkeystate, winui._win32_getkeystate, winuser/GetKeyState
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
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - api-ms-win-ntuser-ie-keyboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - GetKeyState
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetKeyState function


## -description


Retrieves the status of the specified virtual key. The status specifies whether the key is up, down, or toggled (on, off—alternating each time the key is pressed).


## -parameters




### -param nVirtKey [in]

Type: <b>int</b>

A virtual key. If the desired virtual key is a letter or digit (A through Z, a through z, or 0 through 9), 
     <i>nVirtKey</i> must be set to the ASCII value of that character. For other keys, it must be a virtual-key code.

If a non-English keyboard layout is used, virtual keys with values in the range ASCII A through Z and 0 through 9 are used to specify most of the character keys. For example, for the German keyboard layout, the virtual key of value ASCII O (0x4F) refers to the "o" key, whereas VK_OEM_1 refers to the "o with umlaut" key.


## -returns



Type: <b>SHORT</b>

The return value specifies the status of the specified virtual key, as follows:

<ul>
<li>If the high-order bit is 1, the key is down; otherwise, it is up.</li>
<li>If the low-order bit is 1, the key is toggled. A key, such as the CAPS LOCK key, is toggled if it is turned on. The key is off and untoggled if the low-order bit is 0. A toggle key's indicator light (if any) on the keyboard will be on when the key is toggled, and off when the key is untoggled.</li>
</ul>



## -remarks



The key status returned from this function changes as a thread reads key messages from its message queue. The status does not reflect the interrupt-level state associated with the hardware. Use the <a href="https://msdn.microsoft.com/library/ms646293(v=VS.85).aspx">GetAsyncKeyState</a> function to retrieve that information.

An application calls <b>GetKeyState</b> in response to a keyboard-input message. This function retrieves the state of the key when the input message was generated.

To retrieve state information for all the virtual keys, use the <a href="https://msdn.microsoft.com/library/ms646299(v=VS.85).aspx">GetKeyboardState</a> function.

An application can use the <a href="https://msdn.microsoft.com/library/Dd375731(v=VS.85).aspx">virtual key code</a> constants <b>VK_SHIFT</b>, <b>VK_CONTROL</b>, and <b>VK_MENU</b> as values for the 
    <i>nVirtKey</i> parameter. This gives the status of the SHIFT, CTRL, or ALT keys without distinguishing between left and right. An application can also use the following virtual-key code constants as values for 
    <i>nVirtKey</i> to distinguish between the left and right instances of those keys:

<b>VK_LSHIFT</b>
<b>VK_RSHIFT</b>
<b>VK_LCONTROL</b>
<b>VK_RCONTROL</b>
<b>VK_LMENU</b>
<b>VK_RMENU</b>
These left- and right-distinguishing constants are available to an application only through the <a href="https://msdn.microsoft.com/library/ms646299(v=VS.85).aspx">GetKeyboardState</a>, <a href="https://msdn.microsoft.com/library/ms646314(v=VS.85).aspx">SetKeyboardState</a>, <a href="https://msdn.microsoft.com/library/ms646293(v=VS.85).aspx">GetAsyncKeyState</a>, <b>GetKeyState</b>, and <a href="https://msdn.microsoft.com/library/ms646306(v=VS.85).aspx">MapVirtualKey</a> functions.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/library/ms646268(v=VS.85).aspx">Displaying Keyboard Input</a>.

<div class="code"></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms646293(v=VS.85).aspx">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/library/ms646299(v=VS.85).aspx">GetKeyboardState</a>



<a href="https://msdn.microsoft.com/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<a href="https://msdn.microsoft.com/library/ms646306(v=VS.85).aspx">MapVirtualKey</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms646314(v=VS.85).aspx">SetKeyboardState</a>
 

 

