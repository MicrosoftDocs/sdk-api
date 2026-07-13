---
UID: NF:winuser.UnloadKeyboardLayout
title: UnloadKeyboardLayout function (winuser.h)
description: Unloads an input locale identifier (formerly called a keyboard layout).
helpviewer_keywords: ["UnloadKeyboardLayout","UnloadKeyboardLayout function [Keyboard and Mouse Input]","_win32_UnloadKeyboardLayout","_win32_unloadkeyboardlayout_cpp","inputdev.unloadkeyboardlayout","winui._win32_unloadkeyboardlayout","winuser/UnloadKeyboardLayout"]
old-location: inputdev\unloadkeyboardlayout.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\unloadkeyboardlayout.htm
ms.date: 12/05/2018
ms.keywords: UnloadKeyboardLayout, UnloadKeyboardLayout function [Keyboard and Mouse Input], _win32_UnloadKeyboardLayout, _win32_unloadkeyboardlayout_cpp, inputdev.unloadkeyboardlayout, winui._win32_unloadkeyboardlayout, winuser/UnloadKeyboardLayout
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
 - UnloadKeyboardLayout
 - winuser/UnloadKeyboardLayout
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
 - ext-ms-win-ntuser-keyboard-l1-3-0.dll
 - User32.dll
api_name:
 - UnloadKeyboardLayout
---

# UnloadKeyboardLayout function


## -description

Unloads an input locale identifier (formerly called a keyboard layout).

## -parameters

### -param hkl [in]

Type: <b>HKL</b>

The input locale identifier to be unloaded.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. The function can fail for the following reasons: 

<ul>
<li>An invalid input locale identifier was passed.</li>
<li>The input locale identifier was preloaded.</li>
<li>The input locale identifier is in use.</li>
</ul>
To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input. 

<b>UnloadKeyboardLayout</b> cannot unload the system default input locale identifier if it is the only keyboard layout loaded. You must first load another input locale identifier before unloading the default input locale identifier.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-activatekeyboardlayout">ActivateKeyboardLayout</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-getkeyboardlayoutnamea">GetKeyboardLayoutName</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<a href="/windows/desktop/api/winuser/nf-winuser-loadkeyboardlayouta">LoadKeyboardLayout</a>



<b>Reference</b>