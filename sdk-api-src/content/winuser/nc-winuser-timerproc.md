---
UID: NC:winuser.TIMERPROC
title: TIMERPROC
author: windows-sdk-content
description: An application-defined callback function that processes WM_TIMER messages. The TIMERPROC type defines a pointer to this callback function. TimerProc is a placeholder for the application-defined function name.
old-location: winmsg\timerproc.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\timerproc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: TimerProc, TimerProc callback, TimerProc callback function [Windows and Messages], _win32_TimerProc, _win32_timerproc_cpp, winmsg.timerproc, winui._win32_timerproc, winuser/TimerProc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TIMERPROC callback function


## -description


An application-defined callback function that processes <a href="https://msdn.microsoft.com/en-us/library/ms644902(v=VS.85).aspx">WM_TIMER</a> messages. The 
			<b>TIMERPROC</b> type defines a pointer to this callback function. <i>TimerProc</i> is a placeholder for the application-defined function name. 


## -parameters




### -param Arg1


### -param Arg2


### -param Arg3


### -param Arg4








#### - dwTime [in]

Type: <b>DWORD</b>

The number of milliseconds that have elapsed since the system was started. This is the value returned by the <a href="https://msdn.microsoft.com/22201c82-a49a-4972-9f49-6baf6d23a1ea">GetTickCount</a> function. 


#### - hwnd [in]

Type: <b>HWND</b>

A handle to the window associated with the timer. 


#### - idEvent [in]

Type: <b>UINT_PTR</b>

The timer's identifier. 


#### - uMsg [in]

Type: <b>UINT</b>

The <a href="https://msdn.microsoft.com/en-us/library/ms644902(v=VS.85).aspx">WM_TIMER</a> message. 


## -returns



This function does not return a value. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644903(v=VS.85).aspx">KillTimer</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms644906(v=VS.85).aspx">SetTimer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms632592(v=VS.85).aspx">Timers</a>



<a href="https://msdn.microsoft.com/en-us/library/ms644902(v=VS.85).aspx">WM_TIMER</a>
 

 

