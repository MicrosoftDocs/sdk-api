---
UID: NF:winuser.IsWindowEnabled
title: IsWindowEnabled function
author: windows-sdk-content
description: Determines whether the specified window is enabled for mouse and keyboard input.
old-location: inputdev\iswindowenabled.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\iswindowenabled.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IsWindowEnabled, IsWindowEnabled function [Keyboard and Mouse Input], _win32_IsWindowEnabled, _win32_iswindowenabled_cpp, inputdev.iswindowenabled, winui._win32_iswindowenabled, winuser/IsWindowEnabled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-0.dll
 - Ext-MS-Win-NTUser-Keyboard-l1-1-1.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-keyboard-l1-1-2.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-0.dll
 - Ext-MS-Win-NTUser-Keyboard-L1-2-1.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsWindowEnabled
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IsWindowEnabled function


## -description


Determines whether the specified window is enabled for mouse and keyboard input.


## -parameters




### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested.


## -returns



Type: <b>BOOL</b>

If the window is enabled, the return value is nonzero.

If the window is not enabled, the return value is zero.




## -remarks



A child window receives input only if it is both enabled and visible.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6913efcd-4d12-4396-a4ae-f1fd6335f7a8">EnableWindow</a>



<a href="https://msdn.microsoft.com/6d64e6c4-80b3-48c1-bd1b-00eb3bbbcf4d">IsWindowVisible</a>



<a href="https://msdn.microsoft.com/a3f6ac32-cde9-440d-bbde-0d76b4b5d4a4">Keyboard Input</a>



<b>Reference</b>
 

 

