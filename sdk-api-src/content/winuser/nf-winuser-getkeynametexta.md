---
UID: NF:winuser.GetKeyNameTextA
title: GetKeyNameTextA function (winuser.h)
description: Retrieves a string that represents the name of a key. (ANSI)
helpviewer_keywords: ["GetKeyNameTextA", "winuser/GetKeyNameTextA"]
old-location: inputdev\getkeynametext.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeynametext.htm
ms.date: 08/18/2023
ms.keywords: GetKeyNameText, GetKeyNameText function [Keyboard and Mouse Input], GetKeyNameTextA, GetKeyNameTextW, _win32_GetKeyNameText, _win32_getkeynametext_cpp, inputdev.getkeynametext, winui._win32_getkeynametext, winuser/GetKeyNameText, winuser/GetKeyNameTextA, winuser/GetKeyNameTextW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetKeyNameTextW (Unicode) and GetKeyNameTextA (ANSI)
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
 - GetKeyNameTextA
 - winuser/GetKeyNameTextA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - GetKeyNameText
 - GetKeyNameTextA
 - GetKeyNameTextW
---

# GetKeyNameTextA function


## -description

Retrieves a string that represents the name of a key.

## -parameters

### -param lParam [in]

Type: <b>LONG</b>

The second parameter of the keyboard message (such as <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a>) to be processed. The function interprets the following bit positions in the <i>lParam</i>.

| Bits  | Meaning |
|-------|---------|
| 16-23 | The scan code. The value depends on the OEM. |
| 24    | Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard. The value is 1 if it is an extended key; otherwise, it is 0. |
| 25    | "Do not care" bit. The application calling this function sets this bit to indicate that the function should not distinguish between left and right CTRL and SHIFT keys, for example. |

For more detail, see [Keystroke Message Flags](/windows/win32/inputdev/about-keyboard-input#keystroke-message-flags).

### -param lpString [out]

Type: <b>LPTSTR</b>

The buffer that will receive the key name.

### -param cchSize [in]

Type: <b>int</b>

The maximum length, in characters, of the key name, including the terminating null character. (This parameter should be equal to the size of the buffer pointed to by the <i>lpString</i> parameter.)

## -returns

Type: <b>int</b>

If the function succeeds, a null-terminated string is copied into the specified buffer, and the return value is the length of the string, in characters, not counting the terminating null character.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The format of the key-name string depends on the current keyboard layout.

The keyboard layout maintains a list of names in the form of character strings for keys with names longer than a single character.
The key name is translated according to the [currently active keyboard layout](/windows/win32/inputdev/about-keyboard-input#languages-locales-and-keyboard-layouts), therefore the function might return different results for different [keyboard layouts](/globalization/windows-keyboard-layouts).

The name of a character key is the character itself. The names of dead keys are spelled out in full.

Character keys that are mapped to the 'A'..'Z' [virtual-key codes](/windows/win32/inputdev/virtual-key-codes) are translated to the <U+0041 LATIN CAPITAL LETTER A>..<U+005A LATIN CAPITAL LETTER Z> characters regardless of current keyboard layout. In this case, use the [ToUnicode](/windows/win32/api/winuser/nf-winuser-tounicode) or [ToUnicodeEx](/windows/win32/api/winuser/nf-winuser-tounicodeex) methods to get the character for the corresponding key press.

This method might not work properly with some [keyboard layouts](/globalization/windows-keyboard-layouts) that produce multiple characters (such as ligatures) or supplementary Unicode characters on a single key press.

The winuser.h header defines GetKeyNameText as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[Keyboard Input](/windows/desktop/inputdev/keyboard-input)

[Keyboard Layouts](/globalization/windows-keyboard-layouts)

[Keyboard Layout Samples](/samples/microsoft/windows-driver-samples/keyboard-layout-samples)

[ToUnicode](/windows/win32/api/winuser/nf-winuser-tounicode)

[ToUnicodeEx](/windows/win32/api/winuser/nf-winuser-tounicodeex)
