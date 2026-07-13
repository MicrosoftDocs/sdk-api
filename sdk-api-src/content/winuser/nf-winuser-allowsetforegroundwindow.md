---
UID: NF:winuser.AllowSetForegroundWindow
title: AllowSetForegroundWindow function (winuser.h)
description: Enables the specified process to set the foreground window using the SetForegroundWindow function. The calling process must already be able to set the foreground window. For more information, see Remarks later in this topic.
helpviewer_keywords: ["AllowSetForegroundWindow","AllowSetForegroundWindow function [Windows and Messages]","_win32_AllowSetForegroundWindow","_win32_allowsetforegroundwindow_cpp","winmsg.allowsetforegroundwindow","winui._win32_allowsetforegroundwindow","winuser/AllowSetForegroundWindow"]
old-location: winmsg\allowsetforegroundwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\allowsetforegroundwindow.htm
ms.date: 10/06/2025
ms.keywords: AllowSetForegroundWindow, AllowSetForegroundWindow function [Windows and Messages], _win32_AllowSetForegroundWindow, _win32_allowsetforegroundwindow_cpp, winmsg.allowsetforegroundwindow, winui._win32_allowsetforegroundwindow, winuser/AllowSetForegroundWindow
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
 - AllowSetForegroundWindow
 - winuser/AllowSetForegroundWindow
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
 - AllowSetForegroundWindow
req.apiset: ext-ms-win-ntuser-window-l1-1-0 (introduced in Windows 8)
---

# AllowSetForegroundWindow function


## -description

Enables the specified process to set the foreground window using the <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> function. The calling process must already be able to set the foreground window. For more information, see Remarks later in this topic.

## -parameters

### -param dwProcessId [in]

Type: <b>DWORD</b>

The identifier of the process that will be enabled to set the foreground window. If this parameter is <b>ASFW_ANY</b>, all processes will be enabled to set the foreground window.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. The function will fail if the calling process cannot set the foreground window. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The system restricts which processes can set the foreground window. Normally, a process can set the foreground window by calling the [**SetForegroundWindow**](nf-winuser-setforegroundwindow.md) function only if:

- All of the following conditions are true:
  - The calling process belongs to a desktop application, not a UWP app or a Windows Store app designed for Windows 8 or 8.1.
  - The foreground process has not disabled calls to **SetForegroundWindow** by a previous call to the [**LockSetForegroundWindow**](nf-winuser-locksetforegroundwindow.md) function.
  - No menus are active.
- Additionally, at least one of the following conditions is true:
  - The foreground lock time-out has expired (see [**SPI_GETFOREGROUNDLOCKTIMEOUT** in **SystemParametersInfo**](nf-winuser-systemparametersinfoa.md#SPI_GETFOREGROUNDLOCKTIMEOUT)).
  - The calling process is the foreground process.
  - The calling process was started by the foreground process.
  - There is currently no foreground window, and thus no foreground process.
  - The calling process received the last input event.
  - Either the foreground process or the calling process is being debugged.

A process that can set the foreground window can enable another process to set the foreground window
by calling **AllowSetForegroundWindow**. The process specified by the *dwProcessId* parameter
loses the ability to set the foreground window the next time that either the user generates input,
unless the input is directed at that process, or the next time a process calls
**AllowSetForegroundWindow**, unless the same process is specified as in the previous call to
**AllowSetForegroundWindow**.

## -see-also

**Conceptual**

[LockSetForegroundWindow](nf-winuser-locksetforegroundwindow.md)

**Reference**

[SetForegroundWindow](nf-winuser-setforegroundwindow.md)

[Windows](/windows/win32/winmsg/windows)
