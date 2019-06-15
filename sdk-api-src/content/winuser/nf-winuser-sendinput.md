---
UID: NF:winuser.SendInput
title: SendInput function (winuser.h)
author: windows-sdk-content
description: Synthesizes keystrokes, mouse motions, and button clicks.
old-location: inputdev\sendinput.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\sendinput.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SendInput, SendInput function [Keyboard and Mouse Input], _win32_SendInput, _win32_sendinput_cpp, inputdev.sendinput, winui._win32_sendinput, winuser/SendInput
ms.topic: function
f1_keywords: ["winuser/SendInput"]
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
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - SendInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SendInput function


## -description


Synthesizes keystrokes, mouse motions, and button clicks.


## -parameters




### -param cInputs [in]

Type: <b>UINT</b>

The number of structures in the <i>pInputs</i> array.


### -param pInputs [in]

Type: <b>LPINPUT</b>

An array of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-taginput">INPUT</a> structures. Each structure represents an event to be inserted into the keyboard or mouse input stream.


### -param cbSize [in]

Type: <b>int</b>

The size, in bytes, of an <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-taginput">INPUT</a> structure. If <i>cbSize</i> is not the size of an <b>INPUT</b> structure, the function fails.


## -returns



Type: <b>UINT</b>

The function returns the number of events that it successfully inserted into the keyboard or mouse input stream. If the function returns zero, the input was already blocked by another thread. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

This function fails when it is blocked by UIPI. Note that neither <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> nor the return value will indicate the failure was caused by UIPI blocking.




## -remarks



This function is subject to UIPI. Applications are permitted to inject input only into applications that are at an equal or lesser integrity level.

The <b>SendInput</b> function inserts the events in the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-taginput">INPUT</a> structures serially into the keyboard or mouse input stream. These events are not interspersed with other keyboard or mouse input events inserted either by the user (with the keyboard or mouse) or by calls to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-keybd_event">keybd_event</a>, <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-mouse_event">mouse_event</a>, or other calls to <b>SendInput</b>.

This function does not reset the keyboard's current state. Any keys that are already pressed when the function is called might interfere with the events that this function generates. To avoid this problem, check the keyboard's state with the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a> function and correct as necessary.

Because the touch keyboard uses the surrogate macros defined in winnls.h to send input to the system, a listener on the keyboard event hook must decode input originating from the touch keyboard. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Intl/surrogates-and-supplementary-characters">Surrogates and Supplementary Characters</a>.

An accessibility application can use <b>SendInput</b> to inject keystrokes corresponding to application launch shortcut keys that are handled by the shell.  This  functionality is not guaranteed to work for other types of applications.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getasynckeystate">GetAsyncKeyState</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-taginput">INPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/Intl/surrogates-and-supplementary-characters">Surrogates and Supplementary Characters</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-keybd_event">keybd_event</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-mouse_event">mouse_event</a>
 

 

