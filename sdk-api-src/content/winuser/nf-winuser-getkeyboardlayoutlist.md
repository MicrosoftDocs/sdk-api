---
UID: NF:winuser.GetKeyboardLayoutList
title: GetKeyboardLayoutList function
author: windows-sdk-content
description: Retrieves the input locale identifiers (formerly called keyboard layout handles) corresponding to the current set of input locales in the system. The function copies the identifiers to the specified buffer.
old-location: inputdev\getkeyboardlayoutlist.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\getkeyboardlayoutlist.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetKeyboardLayoutList, GetKeyboardLayoutList function [Keyboard and Mouse Input], _win32_GetKeyboardLayoutList, _win32_getkeyboardlayoutlist_cpp, inputdev.getkeyboardlayoutlist, winui._win32_getkeyboardlayoutlist, winuser/GetKeyboardLayoutList
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
 - GetKeyboardLayoutList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetKeyboardLayoutList function


## -description


Retrieves the input locale identifiers (formerly called keyboard layout handles) corresponding to the current set of input locales in the system. The function copies the identifiers to the specified buffer.


## -parameters




### -param nBuff [in]

Type: <b>int</b>

The maximum number of handles that the buffer can hold.


### -param lpList [out]

Type: <b>HKL*</b>

A pointer to the buffer that receives the array of input locale identifiers.


## -returns



Type: <b>int</b>

If the function succeeds, the return value is the number of input locale identifiers copied to the buffer or, if 
      <i>nBuff</i> is zero, the return value is the size, in array elements, of the buffer needed to receive all current input locale identifiers.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The input locale identifier is a broader concept than a keyboard layout, since it can also encompass a speech-to-text converter, an Input Method Editor (IME), or any other form of input.

<b>Beginning in Windows 8:</b> The preferred method to retrieve the language associated with the current keyboard layout or input method is a call to <a href="https://msdn.microsoft.com/64c40fb5-3601-4673-b85d-d647e8a05298">Windows.Globalization.Language.CurrentInputMethodLanguageTag</a>. If your app passes language tags from <b>CurrentInputMethodLanguageTag</b> to any <a href="https://msdn.microsoft.com/7c72c4de-83be-4b7e-9ed8-b0236c1df8a4">National Language Support</a> functions, it must first convert the tags by calling <a href="https://msdn.microsoft.com/99264b22-3fb5-47e2-b0b9-42a6768e67c1">ResolveLocaleName</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646296(v=VS.85).aspx">GetKeyboardLayout</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<b>Reference</b>
 

 

