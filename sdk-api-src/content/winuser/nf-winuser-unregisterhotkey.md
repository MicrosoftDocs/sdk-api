---
UID: NF:winuser.UnregisterHotKey
title: UnregisterHotKey function (winuser.h)
author: windows-sdk-content
description: Frees a hot key previously registered by the calling thread.
old-location: inputdev\unregisterhotkey.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\unregisterhotkey.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UnregisterHotKey, UnregisterHotKey function [Keyboard and Mouse Input], _win32_UnregisterHotKey, _win32_unregisterhotkey_cpp, inputdev.unregisterhotkey, winui._win32_unregisterhotkey, winuser/UnregisterHotKey
ms.topic: function
f1_keywords: ["winuser/UnregisterHotKey"]
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
 - Ext-MS-Win-RTCore-NTUser-iam-l1-1-0.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Iam-L1-1-1.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-3-0.dll
api_name:
 - UnregisterHotKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UnregisterHotKey function


## -description


Frees a hot key previously registered by the calling thread.


## -parameters




### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window associated with the hot key to be freed. This parameter should be <b>NULL</b> if the hot key is not associated with a window.


### -param id [in]

Type: <b>int</b>

The identifier of the hot key to be freed.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-registerhotkey">RegisterHotKey</a>



<a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-hotkey">WM_HOTKEY</a>
 

 

