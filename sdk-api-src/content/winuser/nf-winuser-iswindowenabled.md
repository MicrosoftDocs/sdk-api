---
UID: NF:winuser.IsWindowEnabled
title: IsWindowEnabled function
author: windows-sdk-content
description: Determines whether the specified window is enabled for mouse and keyboard input.
old-location: inputdev\iswindowenabled.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\iswindowenabled.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IsWindowEnabled, IsWindowEnabled function [Keyboard and Mouse Input], _win32_IsWindowEnabled, _win32_iswindowenabled_cpp, inputdev.iswindowenabled, winui._win32_iswindowenabled, winuser/IsWindowEnabled
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
req.typenames: 
req.redist: 
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



<a href="https://msdn.microsoft.com/en-us/library/ms646291(v=VS.85).aspx">EnableWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633530(v=VS.85).aspx">IsWindowVisible</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<b>Reference</b>
 

 

