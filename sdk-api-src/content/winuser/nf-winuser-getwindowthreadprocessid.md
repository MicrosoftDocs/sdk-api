---
UID: NF:winuser.GetWindowThreadProcessId
title: GetWindowThreadProcessId function (winuser.h)
description: Retrieves the identifier of the thread that created the specified window and, optionally, the identifier of the process that created the window.
helpviewer_keywords: ["GetWindowThreadProcessId","GetWindowThreadProcessId function [Windows and Messages]","_win32_GetWindowThreadProcessId","_win32_getwindowthreadprocessid_cpp","winmsg.getwindowthreadprocessid","winui._win32_getwindowthreadprocessid","winuser/GetWindowThreadProcessId"]
old-location: winmsg\getwindowthreadprocessid.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\getwindowthreadprocessid.htm
ms.date: 12/05/2018
ms.keywords: GetWindowThreadProcessId, GetWindowThreadProcessId function [Windows and Messages], _win32_GetWindowThreadProcessId, _win32_getwindowthreadprocessid_cpp, winmsg.getwindowthreadprocessid, winui._win32_getwindowthreadprocessid, winuser/GetWindowThreadProcessId
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
 - GetWindowThreadProcessId
 - winuser/GetWindowThreadProcessId
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
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - GetWindowThreadProcessId
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# GetWindowThreadProcessId function


## -description

Retrieves the identifier of the thread that created the specified window and, optionally, the identifier of the process that created the window.

## -parameters

### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window.

### -param lpdwProcessId [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that receives the process identifier. If this parameter is not <b>NULL</b>, <b>GetWindowThreadProcessId</b> copies the identifier of the process to the variable; otherwise, it does not. If the function fails, the value of the variable is unchanged.

## -returns

Type: <b>DWORD</b>

If the function succeeds, the return value is the identifier of the thread that created the window. If the window handle is invalid, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

## -see-also

<a href="/windows/desktop/winmsg/windows">Windows Overview</a>
