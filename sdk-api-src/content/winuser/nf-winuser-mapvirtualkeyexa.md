---
UID: NF:winuser.MapVirtualKeyExA
title: MapVirtualKeyExA function (winuser.h)
description: Translates (maps) a virtual-key code into a scan code or character value, or translates a scan code into a virtual-key code. The function translates the codes using the input language and an input locale identifier. (ANSI)
helpviewer_keywords: ["MAPVK_VK_TO_CHAR", "MAPVK_VK_TO_VSC", "MAPVK_VK_TO_VSC_EX", "MAPVK_VSC_TO_VK", "MAPVK_VSC_TO_VK_EX", "MapVirtualKeyExA", "winuser/MapVirtualKeyExA"]
old-location: inputdev\mapvirtualkeyex.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\mapvirtualkeyex.htm
ms.date: 12/05/2018
ms.keywords: MAPVK_VK_TO_CHAR, MAPVK_VK_TO_VSC, MAPVK_VK_TO_VSC_EX, MAPVK_VSC_TO_VK, MAPVK_VSC_TO_VK_EX, MapVirtualKeyEx, MapVirtualKeyEx function [Keyboard and Mouse Input], MapVirtualKeyExA, MapVirtualKeyExW, _win32_MapVirtualKeyEx, _win32_mapvirtualkeyex_cpp, inputdev.mapvirtualkeyex, winui._win32_mapvirtualkeyex, winuser/MapVirtualKeyEx, winuser/MapVirtualKeyExA, winuser/MapVirtualKeyExW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MapVirtualKeyExW (Unicode) and MapVirtualKeyExA (ANSI)
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
 - MapVirtualKeyExA
 - winuser/MapVirtualKeyExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
 - MapVirtualKeyEx
 - MapVirtualKeyExA
 - MapVirtualKeyExW
---

# MapVirtualKeyExA function

## -description

Translates (maps) a virtual-key code into a scan code or character value, or translates a scan code into a virtual-key code. The function translates the codes using the input language and an input locale identifier.

## -parameters

### -param uCode [in]

Type: **UINT**

The [virtual key code](/windows/desktop/inputdev/virtual-key-codes) or scan code for a key. How this value is interpreted depends on the value of the *uMapType* parameter.

### -param uMapType [in]

Type: **UINT**

The translation to perform. The value of this parameter depends on the value of the <i>uCode</i> parameter.

| Value | Meaning |
|-------|---------|
| **MAPVK\_VK\_TO\_VSC**<br>0 | The *uCode* parameter is a virtual-key code and is translated into a scan code. If it is a virtual-key code that does not distinguish between left- and right-hand keys, the left-hand scan code is returned. If there is no translation, the function returns 0. |
| **MAPVK\_VSC\_TO\_VK**<br>1 | The *uCode* parameter is a scan code and is translated into a virtual-key code that does not distinguish between left- and right-hand keys. If there is no translation, the function returns 0.<br>**Windows Vista and later:** the high byte of the *uCode* value can contain either 0xe0 or 0xe1 to specify the extended scan code. |
| **MAPVK\_VK\_TO\_CHAR**<br>2 | The *uCode* parameter is a virtual-key code and is translated into an unshifted character value in the low order word of the return value. Dead keys (diacritics) are indicated by setting the top bit of the return value. If there is no translation, the function returns 0. See Remarks. |
| **MAPVK\_VSC\_TO\_VK\_EX**<br>3 | The *uCode* parameter is a scan code and is translated into a virtual-key code that distinguishes between left- and right-hand keys. If there is no translation, the function returns 0.<br>**Windows Vista and later:** the high byte of the *uCode* value can contain either 0xe0 or 0xe1 to specify the extended scan code. |
| **MAPVK\_VK\_TO\_VSC\_EX**<br>4 | **Windows Vista and later:** The *uCode* parameter is a virtual-key code and is translated into a scan code. If it is a virtual-key code that does not distinguish between left- and right-hand keys, the left-hand scan code is returned. If the scan code is an extended scan code, the high byte of the returned value will contain either 0xe0 or 0xe1 to specify the extended scan code. If there is no translation, the function returns 0. |

### -param dwhkl [in, out, optional]

Type: **HKL**

Input locale identifier to use for translating the specified code. This parameter can be any input locale identifier previously returned by the [LoadKeyboardLayout](nf-winuser-loadkeyboardlayouta.md) function.

## -returns

Type: **UINT**

The return value is either a scan code, a virtual-key code, or a character value, depending on the value of *uCode* and *uMapType*. If there is no translation, the return value is zero.

## -remarks

The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

An application can use **MapVirtualKeyEx** to translate scan codes to the virtual-key code constants **VK_SHIFT**, **VK_CONTROL**, and **VK_MENU**, and vice versa. These translations do not distinguish between the left and right instances of the SHIFT, CTRL, or ALT keys.

An application can get the scan code corresponding to the left or right instance of one of these keys by calling **MapVirtualKeyEx** with *uCode* set to one of the following virtual-key code constants:

- **VK\_LSHIFT**
- **VK\_RSHIFT**
- **VK\_LCONTROL**
- **VK\_RCONTROL**
- **VK\_LMENU**
- **VK\_RMENU**

These left- and right-distinguishing constants are available to an application only through the [GetKeyboardState](nf-winuser-getkeyboardstate.md), [SetKeyboardState](nf-winuser-setkeyboardstate.md), [GetAsyncKeyState](nf-winuser-getasynckeystate.md), [GetKeyState](nf-winuser-getkeystate.md), [MapVirtualKey](nf-winuser-mapvirtualkeya.md), and **MapVirtualKeyEx** functions. For list complete table of virtual key codes, see [Virtual Key Codes](/windows/win32/inputdev/virtual-key-codes).

In **MAPVK\_VK\_TO\_CHAR** mode [virtual-key codes](/windows/win32/inputdev/virtual-key-codes), the 'A'..'Z' keys are translated to upper-case 'A'..'Z' characters regardless of current keyboard layout. If you want to translate a virtual-key code to the corresponding character, use the [ToAscii](/windows/win32/api/winuser/nf-winuser-toascii) function.

> [!NOTE]
> The winuser.h header defines MapVirtualKeyEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

- <a href="/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeystate">GetKeyState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardstate">GetKeyboardState</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-mapvirtualkeya">MapVirtualKey</a>
- <a href="/windows/desktop/api/winuser/nf-winuser-setkeyboardstate">SetKeyboardState</a>
- [LoadKeyboardLayout](nf-winuser-loadkeyboardlayouta.md)
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
- [Keyboard Input Overview](/windows/win32/inputdev/about-keyboard-input)
