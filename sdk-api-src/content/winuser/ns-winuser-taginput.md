---
UID: NS:winuser.tagINPUT
title: tagINPUT
author: windows-sdk-content
description: Used by SendInput to store information for synthesizing input events such as keystrokes, mouse movement, and mouse clicks.
old-location: inputdev\input.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputstructures\input.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPINPUT, *PINPUT, INPUT, INPUT structure [Keyboard and Mouse Input], INPUT_HARDWARE, INPUT_KEYBOARD, INPUT_MOUSE, PINPUT, PINPUT structure pointer [Keyboard and Mouse Input], _win32_INPUT_str, _win32_input_str_cpp, inputdev.input, tagINPUT, winui._win32_input_str, winuser/INPUT, winuser/PINPUT"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - INPUT
product: Windows
targetos: Windows
req.typenames: INPUT, *PINPUT, *LPINPUT
req.redist: 
---

# tagINPUT structure


## -description


Used by <a href="https://msdn.microsoft.com/en-us/library/ms646310(v=VS.85).aspx">SendInput</a> to store information for synthesizing input events such as keystrokes, mouse movement, and mouse clicks.


## -struct-fields




### -field type

Type: <b>DWORD</b>

The type of the input event. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INPUT_MOUSE"></a><a id="input_mouse"></a><dl>
<dt><b>INPUT_MOUSE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The event is a mouse event. Use the <b>mi</b> structure of the union.

</td>
</tr>
<tr>
<td width="40%"><a id="INPUT_KEYBOARD"></a><a id="input_keyboard"></a><dl>
<dt><b>INPUT_KEYBOARD</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The event is a keyboard event. Use the <b>ki</b> structure of the union.

</td>
</tr>
<tr>
<td width="40%"><a id="INPUT_HARDWARE"></a><a id="input_hardware"></a><dl>
<dt><b>INPUT_HARDWARE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The event is a hardware event. Use the <b>hi</b> structure of the union.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.mi

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms646273(v=VS.85).aspx">MOUSEINPUT</a></b>

The information about a simulated mouse event. 


### -field DUMMYUNIONNAME.ki

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms646271(v=VS.85).aspx">KEYBDINPUT</a></b>

The information about a simulated keyboard event. 


### -field DUMMYUNIONNAME.hi

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms646269(v=VS.85).aspx">HARDWAREINPUT</a></b>

The information about a simulated hardware event. 


## -remarks



<b> INPUT_KEYBOARD</b> supports nonkeyboard input methods, such as handwriting recognition or voice recognition, as if it were text input by using the <b>KEYEVENTF_UNICODE</b> flag. For more information, see the remarks section of <a href="https://msdn.microsoft.com/en-us/library/ms646271(v=VS.85).aspx">KEYBDINPUT</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644937(v=VS.85).aspx">GetMessageExtraInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646269(v=VS.85).aspx">HARDWAREINPUT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646271(v=VS.85).aspx">KEYBDINPUT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646273(v=VS.85).aspx">MOUSEINPUT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646310(v=VS.85).aspx">SendInput</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646304(v=VS.85).aspx">keybd_event</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646260(v=VS.85).aspx">mouse_event</a>
 

 

