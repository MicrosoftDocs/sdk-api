---
UID: NS:wincon._CONSOLE_READCONSOLE_CONTROL
title: "_CONSOLE_READCONSOLE_CONTROL"
author: windows-driver-content
description: Contains information for a console read operation.
old-location: consoles\console_readconsole_control.htm
old-project: consoles
ms.assetid: 6a8451a6-d692-43af-88c4-972c4dc5e07c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: "*PCONSOLE_READCONSOLE_CONTROL, CAPSLOCK_ON, CONSOLE_READCONSOLE_CONTROL, CONSOLE_READCONSOLE_CONTROL structure [Consoles], ENHANCED_KEY, LEFT_ALT_PRESSED, LEFT_CTRL_PRESSED, NUMLOCK_ON, PCONSOLE_READCONSOLE_CONTROL, PCONSOLE_READCONSOLE_CONTROL structure pointer [Consoles], RIGHT_ALT_PRESSED, RIGHT_CTRL_PRESSED, SCROLLLOCK_ON, SHIFT_PRESSED, _CONSOLE_READCONSOLE_CONTROL, base.console_readconsole_control, consoleapi/CONSOLE_READCONSOLE_CONTROL, consoleapi/PCONSOLE_READCONSOLE_CONTROL, consoles.console_readconsole_control"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincon.h
req.include-header: Wincon.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: CONSOLE_READCONSOLE_CONTROL, *PCONSOLE_READCONSOLE_CONTROL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	consoleapi.h
api_name:
-	CONSOLE_READCONSOLE_CONTROL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CONSOLE_READCONSOLE_CONTROL structure


## -description


Contains information for a console read operation.


## -struct-fields




### -field nLength

The size of the structure. Set this member to <code>sizeof(CONSOLE_READCONSOLE_CONTROL)</code>.


### -field nInitialChars

The number of characters to skip (and thus preserve) before writing newly read input in the buffer passed to the <a href="https://msdn.microsoft.com/1aa9ecac-a9b9-4e6d-9206-7a57013de657">ReadConsole</a> function. This value must be less than the <i>nNumberOfCharsToRead</i> parameter of the <b>ReadConsole</b> function.


### -field dwCtrlWakeupMask

A user-defined control character used to  signal that the read is complete. 


### -field dwControlKeyState

The state of the control keys. This member can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CAPSLOCK_ON"></a><a id="capslock_on"></a><dl>
<dt><b>CAPSLOCK_ON</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
The CAPS LOCK light is on.

</td>
</tr>
<tr>
<td width="40%"><a id="ENHANCED_KEY"></a><a id="enhanced_key"></a><dl>
<dt><b>ENHANCED_KEY</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
The key is enhanced.

</td>
</tr>
<tr>
<td width="40%"><a id="LEFT_ALT_PRESSED"></a><a id="left_alt_pressed"></a><dl>
<dt><b>LEFT_ALT_PRESSED</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The left ALT key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="LEFT_CTRL_PRESSED"></a><a id="left_ctrl_pressed"></a><dl>
<dt><b>LEFT_CTRL_PRESSED</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The left CTRL key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="NUMLOCK_ON"></a><a id="numlock_on"></a><dl>
<dt><b>NUMLOCK_ON</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The NUM LOCK light is on.

</td>
</tr>
<tr>
<td width="40%"><a id="RIGHT_ALT_PRESSED"></a><a id="right_alt_pressed"></a><dl>
<dt><b>RIGHT_ALT_PRESSED</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The right ALT key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="RIGHT_CTRL_PRESSED"></a><a id="right_ctrl_pressed"></a><dl>
<dt><b>RIGHT_CTRL_PRESSED</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The right CTRL key is pressed.

</td>
</tr>
<tr>
<td width="40%"><a id="SCROLLLOCK_ON"></a><a id="scrolllock_on"></a><dl>
<dt><b>SCROLLLOCK_ON</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The SCROLL LOCK light is on.

</td>
</tr>
<tr>
<td width="40%"><a id="SHIFT_PRESSED"></a><a id="shift_pressed"></a><dl>
<dt><b>SHIFT_PRESSED</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The SHIFT key is pressed.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/1aa9ecac-a9b9-4e6d-9206-7a57013de657">ReadConsole</a>
 

 

