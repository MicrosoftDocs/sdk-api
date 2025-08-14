---
UID: NF:winuser.IsWindowUnicode
title: IsWindowUnicode function (winuser.h)
description: Determines whether the specified window is a native Unicode window.
helpviewer_keywords: ["IsWindowUnicode","IsWindowUnicode function [Windows and Messages]","_win32_IsWindowUnicode","_win32_iswindowunicode_cpp","winmsg.iswindowunicode","winui._win32_iswindowunicode","winuser/IsWindowUnicode"]
old-location: winmsg\iswindowunicode.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\iswindowunicode.htm
ms.date: 12/05/2018
ms.keywords: IsWindowUnicode, IsWindowUnicode function [Windows and Messages], _win32_IsWindowUnicode, _win32_iswindowunicode_cpp, winmsg.iswindowunicode, winui._win32_iswindowunicode, winuser/IsWindowUnicode
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
 - IsWindowUnicode
 - winuser/IsWindowUnicode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsWindowUnicode
req.apiset: ext-ms-win-ntuser-window-l1-1-1 (introduced in Windows 8.1)
---

# IsWindowUnicode function


## -description

Determines whether the specified window is a native Unicode window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested.

## -returns

Type: <b>BOOL</b>

If the window is a native Unicode window, the return value is nonzero.

If the window is not a native Unicode window, the return value is zero. The window is a native ANSI window.

## -remarks

The character set of a window is determined by the use of the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassa">RegisterClass</a> function. If the window class was registered with the ANSI version of <b>RegisterClass</b> (<b>RegisterClassA</b>), the character set of the window is ANSI. If the window class was registered with the Unicode version of <b>RegisterClass</b> (<b>RegisterClassW</b>), the character set of the window is Unicode. 

The system does automatic two-way translation (Unicode to ANSI) for window messages. For example, if an ANSI window message is sent to a window that uses the Unicode character set, the system translates that message into a Unicode message before calling the window procedure. The system calls <b>IsWindowUnicode</b> to determine whether to translate the message.

## -see-also

<a href="/windows/desktop/winmsg/windows">Windows Overview</a>
