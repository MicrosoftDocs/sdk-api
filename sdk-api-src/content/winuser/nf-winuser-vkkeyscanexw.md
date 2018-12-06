---
UID: NF:winuser.VkKeyScanExW
title: VkKeyScanExW function
author: windows-sdk-content
description: Translates a character to the corresponding virtual-key code and shift state. The function translates the character using the input language and physical keyboard layout identified by the input locale identifier.
old-location: inputdev\vkkeyscanex.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\vkkeyscanex.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VkKeyScanEx, VkKeyScanEx function [Keyboard and Mouse Input], VkKeyScanExA, VkKeyScanExW, _win32_VkKeyScanEx, _win32_vkkeyscanex_cpp, inputdev.vkkeyscanex, winui._win32_vkkeyscanex, winuser/VkKeyScanEx, winuser/VkKeyScanExA, winuser/VkKeyScanExW
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
req.unicode-ansi: VkKeyScanExW (Unicode) and VkKeyScanExA (ANSI)
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
req.typenames: 
req.redist: 
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

Input locale identifier used to translate the character. This parameter can be any input locale identifier previously returned by the <a href="https://msdn.microsoft.com/6e35847e-d641-4ff2-80b6-a5b5293ebbdc">LoadKeyboardLayout</a> function.


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
    <a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a> and 
    <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a> messages.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/66fffda1-e0cc-4f6b-9456-870820d10601">GetKeyNameText</a>



<a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a>



<a href="https://msdn.microsoft.com/d6b31d2c-43b3-4502-a7ed-af564895f27e">GetKeyboardState</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<a href="https://msdn.microsoft.com/6e35847e-d641-4ff2-80b6-a5b5293ebbdc">LoadKeyboardLayout</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9c34dd1f-b423-4dcd-b29e-8bf64be57472">SetKeyboardState</a>



<a href="https://msdn.microsoft.com/6fe5fec1-51e2-4115-9c45-10074d47ec34">ToAsciiEx</a>
 

 

