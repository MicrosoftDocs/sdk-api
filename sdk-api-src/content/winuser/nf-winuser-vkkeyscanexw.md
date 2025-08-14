---
UID: NF:winuser.VkKeyScanExW
title: VkKeyScanExW function (winuser.h)
description: Translates a character to the corresponding virtual-key code and shift state. The function translates the character using the input language and physical keyboard layout identified by the input locale identifier. (Unicode)
helpviewer_keywords: ["VkKeyScanEx", "VkKeyScanEx function [Keyboard and Mouse Input]", "VkKeyScanExW", "_win32_VkKeyScanEx", "_win32_vkkeyscanex_cpp", "inputdev.vkkeyscanex", "winui._win32_vkkeyscanex", "winuser/VkKeyScanEx", "winuser/VkKeyScanExW"]
old-location: inputdev\vkkeyscanex.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\vkkeyscanex.htm
ms.date: 12/05/2018
ms.keywords: VkKeyScanEx, VkKeyScanEx function [Keyboard and Mouse Input], VkKeyScanExA, VkKeyScanExW, _win32_VkKeyScanEx, _win32_vkkeyscanex_cpp, inputdev.vkkeyscanex, winui._win32_vkkeyscanex, winuser/VkKeyScanEx, winuser/VkKeyScanExA, winuser/VkKeyScanExW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VkKeyScanExW
 - winuser/VkKeyScanExW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-keyboard-l1-3-2.dll
 - ext-ms-win-ntuser-keyboard-l1-3-1.dll
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

Input locale identifier used to translate the character. This parameter can be any input locale identifier previously returned by the <a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a> function.

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
    <a href="/windows/desktop/inputdev/wm-keyup">WM_KEYUP</a> and 
    <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> messages.





> [!NOTE]
> The winuser.h header defines VkKeyScanEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

- <a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeynametexta">GetKeyNameText</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-setkeyboardstate">SetKeyboardState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-toasciiex">ToAsciiEx</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
