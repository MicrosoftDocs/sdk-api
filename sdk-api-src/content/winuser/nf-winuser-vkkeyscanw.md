---
UID: NF:winuser.VkKeyScanW
title: VkKeyScanW function (winuser.h)
author: windows-sdk-content
description: Translates a character to the corresponding virtual-key code and shift state for the current keyboard.
old-location: inputdev\vkkeyscan.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\vkkeyscan.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VkKeyScan, VkKeyScan function [Keyboard and Mouse Input], VkKeyScanA, VkKeyScanW, _win32_VkKeyScan, _win32_vkkeyscan_cpp, inputdev.vkkeyscan, winui._win32_vkkeyscan, winuser/VkKeyScan, winuser/VkKeyScanA, winuser/VkKeyScanW
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
 - VkKeyScan
 - VkKeyScanA
 - VkKeyScanW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VkKeyScanW function


## -description


<p class="CCE_Message">[This function has been superseded by the <a href="https://msdn.microsoft.com/en-us/library/ms646332(v=VS.85).aspx">VkKeyScanEx</a> function. You can still use <b>VkKeyScan</b>, however, if you do not need to specify a keyboard layout.]

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

<b>VkKeyScan</b> is used by applications that send characters by using the <a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a> and <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> messages.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646293(v=VS.85).aspx">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646300(v=VS.85).aspx">GetKeyNameText</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646301(v=VS.85).aspx">GetKeyState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646299(v=VS.85).aspx">GetKeyboardState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646314(v=VS.85).aspx">SetKeyboardState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646332(v=VS.85).aspx">VkKeyScanEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a>
 

 

