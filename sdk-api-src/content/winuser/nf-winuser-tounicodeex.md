---
UID: NF:winuser.ToUnicodeEx
title: ToUnicodeEx function (winuser.h)
description: Translates the specified virtual-key code and keyboard state to the corresponding Unicode character or characters. (ToUnicodeEx)
helpviewer_keywords: ["ToUnicodeEx","ToUnicodeEx function [Keyboard and Mouse Input]","_win32_ToUnicodeEx","_win32_tounicodeex_cpp","inputdev.tounicodeex","winui._win32_tounicodeex","winuser/ToUnicodeEx"]
old-location: inputdev\tounicodeex.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\tounicodeex.htm
ms.date: 12/05/2018
ms.keywords: ToUnicodeEx, ToUnicodeEx function [Keyboard and Mouse Input], _win32_ToUnicodeEx, _win32_tounicodeex_cpp, inputdev.tounicodeex, winui._win32_tounicodeex, winuser/ToUnicodeEx
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
 - ToUnicodeEx
 - winuser/ToUnicodeEx
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
 - api-ms-win-ntuser-ie-keyboard-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - ToUnicodeEx
---

# ToUnicodeEx function


## -description

Translates the specified virtual-key code and keyboard state to the corresponding Unicode character or characters.

## -parameters

### -param wVirtKey [in]

Type: <b>UINT</b>

The virtual-key code to be translated. See <a href="/windows/desktop/inputdev/virtual-key-codes">Virtual-Key Codes</a>.

### -param wScanCode [in]

Type: <b>UINT</b>

The hardware <a href="/windows/win32/inputdev/about-keyboard-input#scan-codes">scan code</a> of the key to be translated. The high-order bit of this value is set if the key is up.

### -param lpKeyState [in]

Type: <b>const BYTE*</b>

A pointer to a 256-byte array that contains the current keyboard state. Each element (byte) in the array contains the state of one key. 

If the high-order bit of a byte is set, the key is down. The low bit, if set, indicates that the key is toggled on. In this function, only the toggle bit of the CAPS LOCK key is relevant. The toggle state of the NUM LOCK and SCROLL LOCK keys is ignored. See <a href="/windows/win32/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a> for more info.

### -param pwszBuff [out]

Type: <b>LPWSTR</b>

The buffer that receives the translated character or characters as array of UTF-16 code units. This buffer may be returned without being null-terminated even though the variable name suggests that it is null-terminated. You can use the return value of this method to determine how many characters were written.

### -param cchBuff [in]

Type: <b>int</b>

The size, in characters, of the buffer pointed to by the <i>pwszBuff</i> parameter.

### -param wFlags [in]

Type: <b>UINT</b>

The behavior of the function. 

If bit 0 is set, a menu is active. In this mode <b>Alt+Numeric keypad</b> key combinations are not handled.

If bit 1 is set, **ToUnicodeEx** will translate scancodes marked as key break events in addition to its usual treatment of key make events.

If bit 2 is set, keyboard state is not changed (Windows 10, version 1607 and newer)

All other bits (through 31) are reserved.

### -param dwhkl [in, optional]

Type: <b>HKL</b>

The input locale identifier used to translate the specified code. This parameter can be any input locale identifier previously returned by the <a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a> function.

## -returns

Type: <b>int</b>

The function returns one of the following values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><i>value</i> < 0 </dt>
</dl>
</td>
<td width="60%">
The specified virtual key is a <a href="/windows/win32/inputdev/about-keyboard-input#dead-character-messages">dead key</a> character (accent or diacritic). This value is returned regardless of the keyboard layout, even if several characters have been typed and are stored in the keyboard state. If possible, even with Unicode keyboard layouts, the function has written a spacing version of the dead-key character to the buffer specified by <i>pwszBuff</i>. For example, the function writes the character ACUTE ACCENT (U+00B4), rather than the character COMBINING ACUTE ACCENT (U+0301).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The specified virtual key has no translation for the current state of the keyboard. Nothing was written to the buffer specified by <i>pwszBuff</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><i>value</i> > 0 </dt>
</dl>
</td>
<td width="60%">
One or more UTF-16 code units were written to the buffer specified by <i>pwszBuff</i>. Returned <i>pwszBuff</i> may contain more characters than the return value specifies. When this happens, any extra characters are invalid and should be ignored.

</td>
</tr>
</table>

## -remarks

The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

Some keyboard layouts may return several characters and/or supplementary characters as <a href="/windows/win32/intl/surrogates-and-supplementary-characters">surrogate pairs</a> in <i>pwszBuff</i>. If dead key character (accent or diacritic) stored in the keyboard layout could not be combined with the specified virtual key to form a single character then the previous entered dead character can be combined with the current character.

The parameters supplied to the <b>ToUnicodeEx</b> function might not be sufficient to translate the virtual-key code because a previous <a href="/windows/win32/inputdev/about-keyboard-input#dead-character-messages">dead key</a> is stored in the keyboard layout.

Typically, <b>ToUnicodeEx</b> performs the translation based on the virtual-key code. In some cases, however, bit 15 of the <i>wScanCode</i> parameter can be used to distinguish between a key press and a key release (for example for ALT+numpad key entry).

As <b>ToUnicodeEx</b> translates the virtual-key code, it also changes the state of the kernel-mode keyboard buffer. This state-change affects dead keys, ligatures, <b>Alt+Numeric keypad</b> key entry, and so on. It might also cause undesired side-effects if used in conjunction with <a href="/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a> (which also changes the state of the kernel-mode keyboard buffer).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-toasciiex">ToAsciiEx</a>



<a href="/windows/desktop/api/winuser/nf-winuser-vkkeyscana">VkKeyScan</a>
