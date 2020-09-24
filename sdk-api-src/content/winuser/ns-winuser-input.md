---
UID: NS:winuser.tagINPUT
title: INPUT (winuser.h)
description: Used by SendInput to store information for synthesizing input events such as keystrokes, mouse movement, and mouse clicks.
helpviewer_keywords: ["*LPINPUT","*PINPUT","INPUT","INPUT structure [Keyboard and Mouse Input]","INPUT_HARDWARE","INPUT_KEYBOARD","INPUT_MOUSE","PINPUT","PINPUT structure pointer [Keyboard and Mouse Input]","_win32_INPUT_str","_win32_input_str_cpp","inputdev.input","winui._win32_input_str","winuser/INPUT","winuser/PINPUT"]
old-location: inputdev\input.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputstructures\input.htm
ms.date: 12/05/2018
ms.keywords: '*LPINPUT, *PINPUT, INPUT, INPUT structure [Keyboard and Mouse Input], INPUT_HARDWARE, INPUT_KEYBOARD, INPUT_MOUSE, PINPUT, PINPUT structure pointer [Keyboard and Mouse Input], _win32_INPUT_str, _win32_input_str_cpp, inputdev.input, winui._win32_input_str, winuser/INPUT, winuser/PINPUT'
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
targetos: Windows
req.typenames: INPUT, *PINPUT, *LPINPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagINPUT
 - winuser/tagINPUT
 - PINPUT
 - winuser/PINPUT
 - INPUT
 - winuser/INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - INPUT
---

# INPUT structure


## -description

Used by <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> to store information for synthesizing input events such as keystrokes, mouse movement, and mouse clicks.

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

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-mouseinput">MOUSEINPUT</a></b>

The information about a simulated mouse event.

### -field DUMMYUNIONNAME.ki

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-keybdinput">KEYBDINPUT</a></b>

The information about a simulated keyboard event.

### -field DUMMYUNIONNAME.hi

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-hardwareinput">HARDWAREINPUT</a></b>

The information about a simulated hardware event.

## -remarks

<b> INPUT_KEYBOARD</b> supports nonkeyboard input methods, such as handwriting recognition or voice recognition, as if it were text input by using the <b>KEYEVENTF_UNICODE</b> flag. For more information, see the remarks section of <a href="/windows/desktop/api/winuser/ns-winuser-keybdinput">KEYBDINPUT</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo">GetMessageExtraInfo</a>



<a href="/windows/desktop/api/winuser/ns-winuser-hardwareinput">HARDWAREINPUT</a>



<a href="/windows/desktop/api/winuser/ns-winuser-keybdinput">KEYBDINPUT</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<a href="/windows/desktop/api/winuser/ns-winuser-mouseinput">MOUSEINPUT</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a>



<a href="/windows/desktop/api/winuser/nf-winuser-keybd_event">keybd_event</a>



<a href="/windows/desktop/api/winuser/nf-winuser-mouse_event">mouse_event</a>