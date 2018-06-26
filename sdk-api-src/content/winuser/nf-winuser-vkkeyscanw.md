---
UID: NF:winuser.VkKeyScanW
title: VkKeyScanW function
author: windows-sdk-content
description: Translates a character to the corresponding virtual-key code and shift state for the current keyboard.
old-location: inputdev\vkkeyscan.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\vkkeyscan.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: VkKeyScan, VkKeyScan function [Keyboard and Mouse Input], VkKeyScanA, VkKeyScanW, _win32_VkKeyScan, _win32_vkkeyscan_cpp, inputdev.vkkeyscan, winui._win32_vkkeyscan, winuser/VkKeyScan, winuser/VkKeyScanA, winuser/VkKeyScanW
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
req.unicode-ansi: VkKeyScanW (Unicode) and VkKeyScanA (ANSI)
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
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - VkKeyScan
 - VkKeyScanA
 - VkKeyScanW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# VkKeyScanW function


## -description


<p class="CCE_Message">[This function has been superseded by the <a href="https://msdn.microsoft.com/f7fc172e-29a7-48c5-a966-d3d08dd94127">VkKeyScanEx</a> function. You can still use <b>VkKeyScan</b>, however, if you do not need to specify a keyboard layout.]

Translates a character to the corresponding virtual-key code and shift state for the current keyboard.


## -parameters




### -param ch [in]

Type: <b>TCHAR</b>

The character to be translated into a virtual-key code.


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



For keyboard layouts that use the right-hand ALT key as a shift key (for example, the French keyboard layout), the shift state is represented by the value 6, because the right-hand ALT key is converted internally into CTRL+ALT.

Translations for the numeric keypad (<b>VK_NUMPAD0</b> through <b>VK_DIVIDE</b>) are ignored. This function is intended to translate characters into keystrokes from the main keyboard section only. For example, the character "7" is translated into VK_7, not VK_NUMPAD7.

<b>VkKeyScan</b> is used by applications that send characters by using the <a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a> and <a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a> messages.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/edc449e4-f37d-4f2c-8add-45b905bd3326">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/66fffda1-e0cc-4f6b-9456-870820d10601">GetKeyNameText</a>



<a href="https://msdn.microsoft.com/41c7bcc7-0a14-420c-b338-7ca13c95b7b8">GetKeyState</a>



<a href="https://msdn.microsoft.com/d6b31d2c-43b3-4502-a7ed-af564895f27e">GetKeyboardState</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/9c34dd1f-b423-4dcd-b29e-8bf64be57472">SetKeyboardState</a>



<a href="https://msdn.microsoft.com/f7fc172e-29a7-48c5-a966-d3d08dd94127">VkKeyScanEx</a>



<a href="https://msdn.microsoft.com/0e37149f-445c-4b20-ad68-fdf39428ac91">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/67d9d82d-fab0-4aec-a337-7a9cb2b0b586">WM_KEYUP</a>
 

 

