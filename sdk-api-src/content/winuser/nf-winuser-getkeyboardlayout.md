---
UID: NF:winuser.GetKeyboardLayout
title: GetKeyboardLayout function (winuser.h)
description: Retrieves the active input locale identifier (formerly called the keyboard layout).
helpviewer_keywords: ["GetKeyboardLayout","GetKeyboardLayout function [Keyboard and Mouse Input]","_win32_GetKeyboardLayout","_win32_getkeyboardlayout_cpp","inputdev.getkeyboardlayout","winui._win32_getkeyboardlayout","winuser/GetKeyboardLayout"]
old-location: inputdev\getkeyboardlayout.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeyboardlayout.htm
ms.date: 12/05/2018
ms.keywords: GetKeyboardLayout, GetKeyboardLayout function [Keyboard and Mouse Input], _win32_GetKeyboardLayout, _win32_getkeyboardlayout_cpp, inputdev.getkeyboardlayout, winui._win32_getkeyboardlayout, winuser/GetKeyboardLayout
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
 - GetKeyboardLayout
 - winuser/GetKeyboardLayout
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
 - GetKeyboardLayout
---

# GetKeyboardLayout function


## -description

Retrieves the active input locale identifier (formerly called the keyboard layout).

## -parameters

### -param idThread [in]

Type: <b>DWORD</b>

The identifier of the thread to query, or 0 for the current thread.

## -returns

Type: <b>HKL</b>

The return value is the input locale identifier for the thread. The low word contains a <a href="/windows/desktop/Intl/language-identifiers">Language Identifier</a> for the input language and the high word contains a device handle to the physical layout of the keyboard.

## -remarks

The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

Since the keyboard layout can be dynamically changed, applications that cache information about the current keyboard layout should process the <a href="/windows/desktop/winmsg/wm-inputlangchange">WM_INPUTLANGCHANGE</a> message to be informed of changes in the input language.

To get the KLID (keyboard layout ID) of the currently active HKL, call the  <a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardlayoutnamea">GetKeyboardLayoutName</a>.

<b>Beginning in Windows 8:</b> The preferred method to retrieve the language associated with the current keyboard layout or input method is a call to <a href="/uwp/api/windows.globalization.language.currentinputmethodlanguagetag">Windows.Globalization.Language.CurrentInputMethodLanguageTag</a>. If your app passes language tags from <b>CurrentInputMethodLanguageTag</b> to any <a href="/windows/desktop/Intl/national-language-support-functions">National Language Support</a> functions, it must first convert the tags by calling <a href="/windows/desktop/api/winnls/nf-winnls-resolvelocalename">ResolveLocaleName</a>.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-activatekeyboardlayout">ActivateKeyboardLayout</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createthread">CreateThread</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/winmsg/wm-inputlangchange">WM_INPUTLANGCHANGE</a>