---
UID: NF:winuser.GetKeyboardLayoutNameW
title: GetKeyboardLayoutNameW function (winuser.h)
description: Retrieves the name of the active input locale identifier (formerly called the keyboard layout) for the calling thread. (Unicode)
helpviewer_keywords: ["GetKeyboardLayoutName", "GetKeyboardLayoutName function [Keyboard and Mouse Input]", "GetKeyboardLayoutNameW", "_win32_GetKeyboardLayoutName", "_win32_getkeyboardlayoutname_cpp", "inputdev.getkeyboardlayoutname", "winui._win32_getkeyboardlayoutname", "winuser/GetKeyboardLayoutName", "winuser/GetKeyboardLayoutNameW"]
old-location: inputdev\getkeyboardlayoutname.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeyboardlayoutname.htm
ms.date: 12/05/2018
ms.keywords: GetKeyboardLayoutName, GetKeyboardLayoutName function [Keyboard and Mouse Input], GetKeyboardLayoutNameA, GetKeyboardLayoutNameW, _win32_GetKeyboardLayoutName, _win32_getkeyboardlayoutname_cpp, inputdev.getkeyboardlayoutname, winui._win32_getkeyboardlayoutname, winuser/GetKeyboardLayoutName, winuser/GetKeyboardLayoutNameA, winuser/GetKeyboardLayoutNameW
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetKeyboardLayoutNameW (Unicode) and GetKeyboardLayoutNameA (ANSI)
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
 - GetKeyboardLayoutNameW
 - winuser/GetKeyboardLayoutNameW
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
 - GetKeyboardLayoutName
 - GetKeyboardLayoutNameA
 - GetKeyboardLayoutNameW
---

# GetKeyboardLayoutNameW function


## -description

Retrieves the name of the active input locale identifier (formerly called the keyboard layout) for the calling thread.

## -parameters

### -param pwszKLID [out]

Type: <b>LPTSTR</b>

The buffer (of at least <b>KL_NAMELENGTH</b> characters in length) that receives the name of the input locale identifier, including the terminating null character. This will be a copy of the string provided to the <a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a> function, unless layout substitution took place.

For a list of the input layouts that are supplied with Windows, see [Keyboard Identifiers and Input Method Editors for Windows](/windows-hardware/manufacture/desktop/windows-language-pack-default-values).

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

<b>Beginning in Windows 8:</b> The preferred method to retrieve the language associated with the current keyboard layout or input method is a call to <a href="/uwp/api/windows.globalization.language.currentinputmethodlanguagetag">Windows.Globalization.Language.CurrentInputMethodLanguageTag</a>. If your app passes language tags from <b>CurrentInputMethodLanguageTag</b> to any <a href="/windows/desktop/Intl/national-language-support-functions">National Language Support</a> functions, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

> [!NOTE]
> The winuser.h header defines GetKeyboardLayoutName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-activatekeyboardlayout">ActivateKeyboardLayout</a>

<b>Conceptual</b>

<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>

<a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>

<b>Reference</b>

<a href="/windows/desktop/api/winuser/nf-winuser-unloadkeyboardlayout">UnloadKeyboardLayout</a>
