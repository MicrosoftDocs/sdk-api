---
UID: NF:winuser.GetKeyboardLayout
title: GetKeyboardLayout function
author: windows-sdk-content
description: Retrieves the active input locale identifier (formerly called the keyboard layout).
old-location: inputdev\getkeyboardlayout.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeyboardlayout.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetKeyboardLayout, GetKeyboardLayout function [Keyboard and Mouse Input], _win32_GetKeyboardLayout, _win32_getkeyboardlayout_cpp, inputdev.getkeyboardlayout, winui._win32_getkeyboardlayout, winuser/GetKeyboardLayout
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - GetKeyboardLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The return value is the input locale identifier for the thread. The low word contains a <a href="https://msdn.microsoft.com/076e2a43-256a-4646-a5c8-1d48ab08ce1a">Language Identifier</a> for the input language and the high word contains a device handle to the physical layout of the keyboard.




## -remarks



The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

Since the keyboard layout can be dynamically changed, applications that cache information about the current keyboard layout should process the <a href="https://msdn.microsoft.com/en-us/library/ms632629(v=VS.85).aspx">WM_INPUTLANGCHANGE</a> message to be informed of changes in the input language.

To get the KLID (keyboard layout ID) of the currently active HKL, call the  <a href="https://msdn.microsoft.com/en-us/library/ms646298(v=VS.85).aspx">GetKeyboardLayoutName</a>.

<b>Beginning in Windows 8:</b> The preferred method to retrieve the language associated with the current keyboard layout or input method is a call to <a href="https://msdn.microsoft.com/64c40fb5-3601-4673-b85d-d647e8a05298">Windows.Globalization.Language.CurrentInputMethodLanguageTag</a>. If your app passes language tags from <b>CurrentInputMethodLanguageTag</b> to any <a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support</a> functions, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms646289(v=VS.85).aspx">ActivateKeyboardLayout</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/202a4b42-513a-45de-894a-72e56c706a58">CreateThread</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646305(v=VS.85).aspx">LoadKeyboardLayout</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms632629(v=VS.85).aspx">WM_INPUTLANGCHANGE</a>
 

 

