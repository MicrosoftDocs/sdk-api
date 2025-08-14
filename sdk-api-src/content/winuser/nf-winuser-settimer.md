---
UID: NF:winuser.SetTimer
title: SetTimer function (winuser.h)
description: Creates a timer with the specified time-out value.
helpviewer_keywords: ["SetTimer","SetTimer function [Windows and Messages]","_win32_SetTimer","_win32_settimer_cpp","winmsg.settimer","winui._win32_settimer","winuser/SetTimer"]
old-location: winmsg\settimer.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\settimer.htm
ms.date: 12/05/2018
ms.keywords: SetTimer, SetTimer function [Windows and Messages], _win32_SetTimer, _win32_settimer_cpp, winmsg.settimer, winui._win32_settimer, winuser/SetTimer
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
 - SetTimer
 - winuser/SetTimer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-rtcore-ntuser-window-ext-l1-1-1.dll
 - ext-ms-win-rtcore-ntuser-message-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-6.dll
 - ext-ms-win-ntuser-window-l1-1-5.dll
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetTimer
req.apiset: ext-ms-win-ntuser-window-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# SetTimer function


## -description

Creates a timer with the specified time-out value.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window to be associated with the timer. This window must be owned by the calling thread. If a <b>NULL</b> value for <i>hWnd</i> is passed in along with an <i>nIDEvent</i> of an existing timer, that timer will be replaced in the same way that an existing non-NULL <i>hWnd</i> timer will be.

### -param nIDEvent [in]

Type: <b>UINT_PTR</b>

A nonzero timer identifier. If the <i>hWnd</i> parameter is <b>NULL</b>, and the <i>nIDEvent</i> does not match an existing timer then it is ignored and a new timer ID is generated. If the <i>hWnd</i> parameter is not <b>NULL</b> and the window specified by <i>hWnd</i> already has a timer with the value <i>nIDEvent</i>, then the existing timer is replaced by the new timer. When <b>SetTimer</b> replaces a timer, the timer is reset. Therefore, a message will be sent after the current time-out value elapses, but the previously set time-out value is ignored. If the call is not intended to replace an existing timer, <i>nIDEvent</i> should be 0 if the <i>hWnd</i> is <b>NULL</b>.

### -param uElapse [in]

Type: <b>UINT</b>

The time-out value, in milliseconds.

 If <i>uElapse</i> is less than <b>USER_TIMER_MINIMUM</b> (0x0000000A), the timeout is set to <b>USER_TIMER_MINIMUM</b>. If <i>uElapse</i> is greater than <b>USER_TIMER_MAXIMUM</b> (0x7FFFFFFF), the timeout is set to <b>USER_TIMER_MAXIMUM</b>.

### -param lpTimerFunc [in, optional]

Type: <b>TIMERPROC</b>

A pointer to the function to be notified when the time-out value elapses. For more information about the function, see <a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a>. If <i>lpTimerFunc</i> is <b>NULL</b>, the system posts a <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> message to the application queue. The <b>hwnd</b> member of the message's <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure contains the value of the <i>hWnd</i> parameter.

## -returns

Type: <b>UINT_PTR</b>

If the function succeeds and the <i>hWnd</i> parameter is <b>NULL</b>, the return value is an integer identifying the new timer. An application can pass this value to the <a href="/windows/desktop/api/winuser/nf-winuser-killtimer">KillTimer</a> function to destroy the timer.

If the function succeeds and the <i>hWnd</i> parameter is not <b>NULL</b>, then the return value is a nonzero integer. An application can pass the value of the <i>nIDEvent</i> parameter to the <a href="/windows/desktop/api/winuser/nf-winuser-killtimer">KillTimer</a> function to destroy the timer.

If the function fails to create a timer, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application can process <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> messages by including a <b>WM_TIMER</b> case statement in the window procedure or by specifying a <a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a> callback function when creating the timer. When you specify a <b>TimerProc</b> callback function, the DispatchMessage calls the callback function instead of calling the window procedure when it processes <b>WM_TIMER</b> with a non-NULL lParam. Therefore, you need to dispatch messages in the calling thread, even when you use <b>TimerProc</b> instead of processing <b>WM_TIMER</b>.

The <i>wParam</i> parameter of the <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> message contains the value of the <i>nIDEvent</i> parameter. 

The timer identifier, <i>nIDEvent</i>, is specific to the associated window. Another window can have its own timer which has the same identifier as a timer owned by another window. The timers are distinct. 

<b>SetTimer</b> can reuse timer IDs in the case where <i>hWnd</i> is <b>NULL</b>. 
	
Before using **SetTimer** or other timer-related functions, it is recommended to set the **UOI_TIMERPROC_EXCEPTION_SUPPRESSION** flag to **false** through the **SetUserObjectInformationW** function, otherwise the application could behave unpredictably and could be vulnerable to security exploits. For more info, see <a href="/windows/win32/api/winuser/nf-winuser-setuserobjectinformationw">SetUserObjectInformationW</a>.

#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-timers">Creating a Timer</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-killtimer">KillTimer</a>



<a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>



<b>Reference</b>



<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a>



<a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a>



<a href="/windows/desktop/winmsg/timers">Timers</a>



<a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a>



<a href="/windows/win32/api/winuser/nf-winuser-setcoalescabletimer">SetCoalescableTimer</a>
