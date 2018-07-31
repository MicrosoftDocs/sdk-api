---
UID: NF:winuser.OemKeyScan
title: OemKeyScan function
author: windows-sdk-content
description: Maps OEMASCII codes 0 through 0x0FF into the OEM scan codes and shift states. The function provides information that allows a program to send OEM text to another program by simulating keyboard input.
old-location: inputdev\oemkeyscan.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\oemkeyscan.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: OemKeyScan, OemKeyScan function [Keyboard and Mouse Input], _win32_OemKeyScan, _win32_oemkeyscan_cpp, inputdev.oemkeyscan, winui._win32_oemkeyscan, winuser/OemKeyScan
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
api_name:
 - OemKeyScan
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OemKeyScan function


## -description


Maps OEMASCII codes 0 through 0x0FF into the OEM scan codes and shift states. The function provides information that allows a program to send OEM text to another program by simulating keyboard input. 


## -parameters




### -param wOemChar [in]

Type: <b>WORD</b>

The ASCII value of the OEM character. 


## -returns



Type: <b>DWORD</b>

The low-order word of the return value contains the scan code of the OEM character, and the high-order word contains the shift state, which can be a combination of the following bits. 

<table>
<tr>
<th>Bit</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Either SHIFT key is pressed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Either CTRL key is pressed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Either ALT key is pressed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>8</dt>
</dl>
</td>
<td width="60%">
The Hankaku key is pressed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>16</dt>
</dl>
</td>
<td width="60%">
Reserved (defined by the keyboard layout driver).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>32</dt>
</dl>
</td>
<td width="60%">
Reserved (defined by the keyboard layout driver).

</td>
</tr>
</table>
 

If the character cannot be produced by a single keystroke using the current keyboard layout, the return value is 
						–1. 




## -remarks



This function does not provide translations for characters that require CTRL+ALT or dead keys. Characters not translated by this function must be copied by simulating input using the ALT+ keypad mechanism. The NUMLOCK key must be off. 

This function does not provide translations for characters that cannot be typed with one keystroke using the current keyboard layout, such as characters with diacritics requiring dead keys. Characters not translated by this function may be simulated using the ALT+ keypad mechanism. The NUMLOCK key must be on. 

This function is implemented using the <a href="https://msdn.microsoft.com/en-us/library/ms646329(v=VS.85).aspx">VkKeyScan</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646329(v=VS.85).aspx">VkKeyScan</a>
 

 

