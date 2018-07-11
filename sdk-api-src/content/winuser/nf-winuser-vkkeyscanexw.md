---
UID: NF:winuser.VkKeyScanExW
title: VkKeyScanExW function
author: windows-sdk-content
description: Translates a character to the corresponding virtual-key code and shift state. The function translates the character using the input language and physical keyboard layout identified by the input locale identifier.
old-location: inputdev\vkkeyscanex.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\vkkeyscanex.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: VkKeyScanEx, VkKeyScanEx function [Keyboard and Mouse Input], VkKeyScanExA, VkKeyScanExW, _win32_VkKeyScanEx, _win32_vkkeyscanex_cpp, inputdev.vkkeyscanex, winui._win32_vkkeyscanex, winuser/VkKeyScanEx, winuser/VkKeyScanExA, winuser/VkKeyScanExW
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
req.unicode-ansi: VkKeyScanExW (Unicode) and VkKeyScanExA (ANSI)
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
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - VkKeyScanEx
 - VkKeyScanExA
 - VkKeyScanExW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# VkKeyScanExW function


## -description


Translates a character to the corresponding virtual-key code and shift state. The function translates the character using the input language and physical keyboard layout identified by the input locale identifier.


## -parameters




### -param ch [in]

Type: <b>TCHAR</b>

The character to be translated into a virtual-key code.


### -param dwhkl [in]

Type: <b>HKL</b>

Input locale identifier used to translate the character. This parameter can be any input locale identifier previously returned by the <a href="https://msdn.microsoft.com/library/ms646305(v=VS.85).aspx">LoadKeyboardLayout</a> function.


## -returns



Type: <b>SHORT</b>

If the function succeeds, the low-order byte of the return value contains the virtual-key code and the high-order byte contains the shift state, which can be a combination of the following flag bits.

<table>
<tr>
<th>Return value</th>
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
The Hankaku key is pressed

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
 

If the function finds no key that translates to the passed character code, both the low-order and high-order bytes contain 
      –1.




## -remarks



The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

For keyboard layouts that use the right-hand ALT key as a shift key (for example, the French keyboard layout), the shift state is represented by the value 6, because the right-hand ALT key is converted internally into CTRL+ALT.

Translations for the numeric keypad (VK_NUMPAD0 through VK_DIVIDE) are ignored. This function is intended to translate characters into keystrokes from the main keyboard section only. For example, the character "7" is translated into VK_7, not VK_NUMPAD7.

<b>VkKeyScanEx</b> is used by applications that send characters by using the 
    <a href="https://msdn.microsoft.com/library/ms646281(v=VS.85).aspx">WM_KEYUP</a> and 
    <a href="https://msdn.microsoft.com/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> messages.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms646293(v=VS.85).aspx">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/library/ms646300(v=VS.85).aspx">GetKeyNameText</a>



<a href="https://msdn.microsoft.com/library/ms646301(v=VS.85).aspx">GetKeyState</a>



<a href="https://msdn.microsoft.com/library/ms646299(v=VS.85).aspx">GetKeyboardState</a>



<a href="https://msdn.microsoft.com/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<a href="https://msdn.microsoft.com/library/ms646305(v=VS.85).aspx">LoadKeyboardLayout</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms646314(v=VS.85).aspx">SetKeyboardState</a>



<a href="https://msdn.microsoft.com/library/ms646318(v=VS.85).aspx">ToAsciiEx</a>
 

 

