---
UID: NC:winuser.TIMERPROC
title: TIMERPROC (winuser.h)
description: An application-defined callback function that processes WM_TIMER messages. The TIMERPROC type defines a pointer to this callback function. TimerProc is a placeholder for the application-defined function name.
helpviewer_keywords: ["TimerProc","TimerProc callback","TimerProc callback function [Windows and Messages]","_win32_TimerProc","_win32_timerproc_cpp","winmsg.timerproc","winui._win32_timerproc","winuser/TimerProc"]
old-location: winmsg\timerproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\timerproc.htm
ms.date: 09/30/2025
ms.keywords: TimerProc, TimerProc callback, TimerProc callback function [Windows and Messages], _win32_TimerProc, _win32_timerproc_cpp, winmsg.timerproc, winui._win32_timerproc, winuser/TimerProc
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TIMERPROC
 - winuser/TIMERPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winuser.h
api_name:
 - TimerProc
---

# TIMERPROC callback function

## -description

An application-defined callback function that processes [WM_TIMER](/windows/desktop/winmsg/wm-timer) messages. The **TIMERPROC** type defines a pointer to this callback function. _TimerProc_ is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

Type: **HWND**

A handle to the window associated with the timer. This parameter is typically named _hWnd_.

### -param unnamedParam2

Type: **UINT**

The [WM_TIMER](/windows/desktop/winmsg/wm-timer) message. This parameter is typically named _uMsg_.

### -param unnamedParam3

Type: **UINT_PTR**

The timer's identifier. This parameter is typically named _idEvent_.

### -param unnamedParam4

Type: **DWORD**

The number of milliseconds that have elapsed since the system was started. This is the value returned by the [GetTickCount](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount) function. This parameter is typically named _dwTime_.

## -remarks

> [!NOTE]
> The parameters are defined in the header with no names: `typedef VOID (CALLBACK* TIMERPROC)(HWND, UINT, UINT_PTR, DWORD);`. Therefore, the syntax block lists them as `unnamedParam1` - `unnamedParam4`. You can name these parameters anything in your app. However, they are usually named as shown in the parameter descriptions.

## -see-also

**Conceptual**

[Timers](/windows/desktop/winmsg/timers)

**Reference**

[KillTimer](/windows/desktop/api/winuser/nf-winuser-killtimer)

[SetTimer](/windows/desktop/api/winuser/nf-winuser-settimer)

[WM_TIMER](/windows/desktop/winmsg/wm-timer)
