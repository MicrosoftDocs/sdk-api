---
UID: NS:winuser.tagKEYBDINPUT
title: tagKEYBDINPUT
author: windows-sdk-content
description: Contains information about a simulated keyboard event.
old-location: inputdev\keybdinput.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputstructures\keybdinput.htm
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: "*LPKEYBDINPUT, *PKEYBDINPUT, KEYBDINPUT, KEYBDINPUT structure [Keyboard and Mouse Input], KEYEVENTF_EXTENDEDKEY, KEYEVENTF_KEYUP, KEYEVENTF_SCANCODE, KEYEVENTF_UNICODE, PKEYBDINPUT, PKEYBDINPUT structure pointer [Keyboard and Mouse Input], _win32_KEYBDINPUT_str, _win32_keybdinput_str_cpp, inputdev.keybdinput, tagKEYBDINPUT, winui._win32_keybdinput_str, winuser/KEYBDINPUT, winuser/PKEYBDINPUT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: KEYBDINPUT, *PKEYBDINPUT, *LPKEYBDINPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - KEYBDINPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagKEYBDINPUT structure


## -description


Contains information about a simulated keyboard event. 


## -struct-fields




### -field wVk

Type: <b>WORD</b>

A <a href="https://msdn.microsoft.com/library/Dd375731(v=VS.85).aspx">virtual-key code</a>. The code must be a value in the range 1 to 254. If the <b>dwFlags</b> member specifies <b>KEYEVENTF_UNICODE</b>, <b>wVk</b> must be 0. 


### -field wScan

Type: <b>WORD</b>

A hardware scan code for the key. If <b>dwFlags</b> specifies <b>KEYEVENTF_UNICODE</b>, <b>wScan</b> specifies a Unicode character which is to be sent to the foreground application. 


### -field dwFlags

Type: <b>DWORD</b>

Specifies various aspects of a keystroke. This member can be certain combinations of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KEYEVENTF_EXTENDEDKEY"></a><a id="keyeventf_extendedkey"></a><dl>
<dt><b>KEYEVENTF_EXTENDEDKEY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
If specified, the scan code was preceded by a prefix byte that has the value 0xE0 (224).

</td>
</tr>
<tr>
<td width="40%"><a id="KEYEVENTF_KEYUP"></a><a id="keyeventf_keyup"></a><dl>
<dt><b>KEYEVENTF_KEYUP</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
If specified, the key is being released. If not specified, the key is being pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="KEYEVENTF_SCANCODE"></a><a id="keyeventf_scancode"></a><dl>
<dt><b>KEYEVENTF_SCANCODE</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
If specified, <b>wScan</b> identifies the key and <b>wVk</b> is ignored. 

</td>
</tr>
<tr>
<td width="40%"><a id="KEYEVENTF_UNICODE"></a><a id="keyeventf_unicode"></a><dl>
<dt><b>KEYEVENTF_UNICODE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
 If specified, the system synthesizes a <b>VK_PACKET</b> keystroke. The <b>wVk</b> parameter must be zero. This flag can only be combined with the <b>KEYEVENTF_KEYUP</b> flag. For more information, see the Remarks section. 

</td>
</tr>
</table>
 


### -field time

Type: <b>DWORD</b>

The time stamp for the event, in milliseconds. If this parameter is zero, the system will provide its own time stamp. 


### -field dwExtraInfo

Type: <b>ULONG_PTR</b>

An additional value associated with the keystroke. Use the <a href="https://msdn.microsoft.com/library/ms644937(v=VS.85).aspx">GetMessageExtraInfo</a> function to obtain this information. 


## -remarks



<b> INPUT_KEYBOARD</b> supports nonkeyboard-input methods—such as handwriting recognition or voice recognition—as if it were text input by using the <b>KEYEVENTF_UNICODE</b> flag. If <b>KEYEVENTF_UNICODE</b> is specified, <a href="https://msdn.microsoft.com/library/ms646310(v=VS.85).aspx">SendInput</a> sends a <a href="https://msdn.microsoft.com/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> or <a href="https://msdn.microsoft.com/library/ms646281(v=VS.85).aspx">WM_KEYUP</a> message to the foreground thread's message queue with <i>wParam</i> equal to <b>VK_PACKET</b>. Once <a href="https://msdn.microsoft.com/library/ms644936(v=VS.85).aspx">GetMessage</a> or <a href="https://msdn.microsoft.com/library/ms644943(v=VS.85).aspx">PeekMessage</a> obtains this message, passing the message to 
<a href="https://msdn.microsoft.com/library/ms644955(v=VS.85).aspx">TranslateMessage</a> posts a <a href="https://msdn.microsoft.com/library/ms646276(v=VS.85).aspx">WM_CHAR</a> message with the Unicode character originally specified by <b>wScan</b>. This Unicode character will automatically be converted to the appropriate ANSI value if it is posted to an ANSI window.

 Set the <b>KEYEVENTF_SCANCODE</b> flag to define keyboard input in terms of the scan code. This is useful to simulate a physical keystroke regardless of which keyboard is currently being used. The virtual key value of a key may alter depending on the current keyboard layout or what other keys were pressed, but the scan code will always be the same.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms644937(v=VS.85).aspx">GetMessageExtraInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550962">INPUT</a>



<a href="https://msdn.microsoft.com/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms646310(v=VS.85).aspx">SendInput</a>
 

 

