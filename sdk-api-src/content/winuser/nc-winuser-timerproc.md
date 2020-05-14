---
UID: NC:winuser.TIMERPROC
title: TIMERPROC (winuser.h)
description: An application-defined callback function that processes WM_TIMER messages. The TIMERPROC type defines a pointer to this callback function. TimerProc is a placeholder for the application-defined function name.helpviewer_keywords: ["TimerProc","TimerProc callback","TimerProc callback function [Windows and Messages]","_win32_TimerProc","_win32_timerproc_cpp","winmsg.timerproc","winui._win32_timerproc","winuser/TimerProc"]
old-location: winmsg\timerproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\timerproc.htm
ms.date: 12/05/2018
ms.keywords: TimerProc, TimerProc callback, TimerProc callback function [Windows and Messages], _win32_TimerProc, _win32_timerproc_cpp, winmsg.timerproc, winui._win32_timerproc, winuser/TimerProc
f1_keywords:
- winuser/TimerProc
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Winuser.h
api_name:
- TimerProc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TIMERPROC callback function


## -description


An application-defined callback function that processes <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-timer">WM_TIMER</a> messages. The 
			<b>TIMERPROC</b> type defines a pointer to this callback function. <i>TimerProc</i> is a placeholder for the application-defined function name. 


## -parameters




### -param Arg1

Type: <b>HWND</b>

A handle to the window associated with the timer. 

### -param Arg2

Type: <b>UINT</b>

The <a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-timer">WM_TIMER</a> message. 

### -param Arg3

Type: <b>UINT_PTR</b>

The timer's identifier. 


### -param Arg4

Type: <b>DWORD</b>

The number of milliseconds that have elapsed since the system was started. This is the value returned by the <a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-gettickcount">GetTickCount</a> function. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-killtimer">KillTimer</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/timers">Timers</a>



<a href="https://docs.microsoft.com/windows/desktop/winmsg/wm-timer">WM_TIMER</a>
 

 

