---
UID: NF:winuser.ToAsciiEx
title: ToAsciiEx function (winuser.h)
description: Translates the specified virtual-key code and keyboard state to the corresponding character or characters. The function translates the code using the input language and physical keyboard layout identified by the input locale identifier.
helpviewer_keywords: ["ToAsciiEx","ToAsciiEx function [Keyboard and Mouse Input]","_win32_ToAsciiEx","_win32_toasciiex_cpp","inputdev.toasciiex","winui._win32_toasciiex","winuser/ToAsciiEx"]
old-location: inputdev\toasciiex.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\toasciiex.htm
ms.date: 12/05/2018
ms.keywords: ToAsciiEx, ToAsciiEx function [Keyboard and Mouse Input], _win32_ToAsciiEx, _win32_toasciiex_cpp, inputdev.toasciiex, winui._win32_toasciiex, winuser/ToAsciiEx
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ToAsciiEx
 - winuser/ToAsciiEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - ToAsciiEx
---

# ToAsciiEx function


## -description

Translates the specified virtual-key code and keyboard state to the corresponding character or characters. The function translates the code using the input language and physical keyboard layout identified by the input locale identifier.

## -parameters

### -param uVirtKey [in]

Type: <b>UINT</b>

The virtual-key code to be translated. See <a href="/windows/desktop/inputdev/virtual-key-codes">Virtual-Key Codes</a>.

### -param uScanCode [in]

Type: <b>UINT</b>

The hardware scan code of the key to be translated. The high-order bit of this value is set if the key is up (not pressed).

### -param lpKeyState [in, optional]

Type: <b>const BYTE*</b>

A pointer to a 256-byte array that contains the current keyboard state. Each element (byte) in the array contains the state of one key. If the high-order bit of a byte is set, the key is down (pressed).

The low bit, if set, indicates that the key is toggled on. In this function, only the toggle bit of the CAPS LOCK key is relevant. The toggle state of the NUM LOCK and SCOLL LOCK keys is ignored.

### -param lpChar [out]

Type: <b>LPWORD</b>

A pointer to the buffer that receives the translated character or characters.

### -param uFlags [in]

Type: <b>UINT</b>

This parameter must be 1 if a menu is active, zero otherwise.

### -param dwhkl [in, optional]

Type: <b>HKL</b>

Input locale identifier to use to translate the code. This parameter can be any input locale identifier previously returned by the <a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a> function.

## -returns

Type: <b>int</b>

If the specified key is a dead key, the return value is negative. Otherwise, it is one of the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The specified virtual key has no translation for the current state of the keyboard.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
One character was copied to the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Two characters were copied to the buffer. This usually happens when a dead-key character (accent or diacritic) stored in the keyboard layout cannot be composed with the specified virtual key to form a single character.

</td>
</tr>
</table>

## -remarks

The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

The parameters supplied to the <b>ToAsciiEx</b> function might not be sufficient to translate the virtual-key code, because a previous dead key is stored in the keyboard layout.

Typically, <b>ToAsciiEx</b> performs the translation based on the virtual-key code. In some cases, however, bit 15 of the 
    <i>uScanCode</i> parameter may be used to distinguish between a key press and a key release. The scan code is used for translating ALT+number key combinations.

Although NUM LOCK is a toggle key that affects keyboard behavior, <b>ToAsciiEx</b> ignores the toggle setting (the low bit) of 
    <i>lpKeyState</i> (<b>VK_NUMLOCK</b>) because the 
    <i>uVirtKey</i> parameter alone is sufficient to distinguish the cursor movement keys (<b>VK_HOME</b>, <b>VK_INSERT</b>, and so on) from the numeric keys (<b>VK_DECIMAL</b>, <b>VK_NUMPAD0</b> - <b>VK_NUMPAD9</b>).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>



<a href="/windows/desktop/api/winuser/nf-winuser-mapvirtualkeyexa">MapVirtualKeyEx</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-tounicodeex">ToUnicodeEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-vkkeyscana">VkKeyScan</a>