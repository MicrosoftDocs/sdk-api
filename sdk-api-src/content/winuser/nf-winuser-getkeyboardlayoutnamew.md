---
UID: NF:winuser.GetKeyboardLayoutNameW
title: GetKeyboardLayoutNameW function
author: windows-sdk-content
description: Retrieves the name of the active input locale identifier (formerly called the keyboard layout) for the system.
old-location: inputdev\getkeyboardlayoutname.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeyboardlayoutname.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetKeyboardLayoutName, GetKeyboardLayoutName function [Keyboard and Mouse Input], GetKeyboardLayoutNameA, GetKeyboardLayoutNameW, _win32_GetKeyboardLayoutName, _win32_getkeyboardlayoutname_cpp, inputdev.getkeyboardlayoutname, winui._win32_getkeyboardlayoutname, winuser/GetKeyboardLayoutName, winuser/GetKeyboardLayoutNameA, winuser/GetKeyboardLayoutNameW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: POINTER_DEVICE_TYPE
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
 - GetKeyboardLayoutName
 - GetKeyboardLayoutNameA
 - GetKeyboardLayoutNameW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetKeyboardLayoutNameW function


## -description


Retrieves the name of the active input locale identifier (formerly called the keyboard layout) for the system.


## -parameters




### -param pwszKLID [out]

Type: <b>LPTSTR</b>

The buffer (of at least <b>KL_NAMELENGTH</b> characters in length) that receives the name of the input locale identifier, including the terminating null character. This will be a copy of the string provided to the <a href="https://msdn.microsoft.com/library/ms646305(v=VS.85).aspx">LoadKeyboardLayout</a> function, unless layout substitution took place.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

<b>Beginning in Windows 8:</b> The preferred method to retrieve the language associated with the current keyboard layout or input method is a call to <a href="https://msdn.microsoft.com/64c40fb5-3601-4673-b85d-d647e8a05298">Windows.Globalization.Language.CurrentInputMethodLanguageTag</a>. If your app passes language tags from <b>CurrentInputMethodLanguageTag</b> to any <a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support</a> functions, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms646289(v=VS.85).aspx">ActivateKeyboardLayout</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<a href="https://msdn.microsoft.com/library/ms646305(v=VS.85).aspx">LoadKeyboardLayout</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms646324(v=VS.85).aspx">UnloadKeyboardLayout</a>
 

 

