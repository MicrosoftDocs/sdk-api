---
UID: NF:winuser.IsWindowEnabled
title: IsWindowEnabled function (winuser.h)
description: Determines whether the specified window is enabled for mouse and keyboard input.
helpviewer_keywords: ["IsWindowEnabled","IsWindowEnabled function [Keyboard and Mouse Input]","_win32_IsWindowEnabled","_win32_iswindowenabled_cpp","inputdev.iswindowenabled","winui._win32_iswindowenabled","winuser/IsWindowEnabled"]
old-location: inputdev\iswindowenabled.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\iswindowenabled.htm
ms.date: 12/05/2018
ms.keywords: IsWindowEnabled, IsWindowEnabled function [Keyboard and Mouse Input], _win32_IsWindowEnabled, _win32_iswindowenabled_cpp, inputdev.iswindowenabled, winui._win32_iswindowenabled, winuser/IsWindowEnabled
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
 - IsWindowEnabled
 - winuser/IsWindowEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
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
req.apiset: ext-ms-win-ntuser-window-l1-1-4 (introduced in Windows 10, version 10.0.14393)
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



<a href="/windows/desktop/api/winuser/nf-winuser-enablewindow">EnableWindow</a>



<a href="/windows/desktop/api/winuser/nf-winuser-iswindowvisible">IsWindowVisible</a>



<a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>



<b>Reference</b>
