---
UID: NF:winuser.SetCoalescableTimer
title: SetCoalescableTimer function (winuser.h)
description: Creates a timer with the specified time-out value and coalescing tolerance delay.
helpviewer_keywords: ["Any other value","SetCoalescableTimer","SetCoalescableTimer function [Windows and Messages]","TIMERV_DEFAULT_COALESCING","TIMERV_NO_COALESCING","winmsg.setcoalescabletimer","winuser/SetCoalescableTimer"]
old-location: winmsg\setcoalescabletimer.htm
tech.root: winmsg
ms.assetid: 39303811-972f-4131-deea-cebf84c50867
ms.date: 10/23/2020
ms.keywords: Any other value, SetCoalescableTimer, SetCoalescableTimer function [Windows and Messages], TIMERV_DEFAULT_COALESCING, TIMERV_NO_COALESCING, winmsg.setcoalescabletimer, winuser/SetCoalescableTimer
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - SetCoalescableTimer
 - winuser/SetCoalescableTimer
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
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - SetCoalescableTimer
req.apiset: ext-ms-win-ntuser-window-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# SetCoalescableTimer function


## -description

Creates a timer with the specified time-out value and coalescing tolerance delay.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window to be associated with the timer. This window must be owned by the calling thread. If a <b>NULL</b> value for <i>hWnd</i> is passed in along with an <i>nIDEvent</i> of an existing timer, that timer will be replaced in the same way that an existing non-NULL <i>hWnd</i> timer will be.

### -param nIDEvent [in]

Type: <b>UINT_PTR</b>

A timer identifier. If the <i>hWnd</i> parameter is <b>NULL</b>, and the <i>nIDEvent</i> does not match an existing timer, then the <i>nIDEvent</i> is ignored and a new timer ID is generated. If the <i>hWnd</i> parameter is not <b>NULL</b> and the window specified by <i>hWnd</i> already has a timer with the value <i>nIDEvent</i>, then the existing timer is replaced by the new timer. When <b>SetCoalescableTimer</b> replaces a timer, the timer is reset. Therefore, a message will be sent after the current time-out value elapses, but the previously set time-out value is ignored. If the call is not intended to replace an existing timer, <i>nIDEvent</i> should be 0 if the <i>hWnd</i> is <b>NULL</b>.

### -param uElapse [in]

Type: <b>UINT</b>

The time-out value, in milliseconds.

 If <i>uElapse</i> is less than <b>USER_TIMER_MINIMUM</b> (0x0000000A), the timeout is set to <b>USER_TIMER_MINIMUM</b>. If <i>uElapse</i> is greater than <b>USER_TIMER_MAXIMUM</b> (0x7FFFFFFF), the timeout is set to <b>USER_TIMER_MAXIMUM</b>.

If the sum of <i>uElapse</i> and <i>uToleranceDelay</i> exceeds <b>USER_TIMER_MAXIMUM</b>, an ERROR_INVALID_PARAMETER exception occurs.

### -param lpTimerFunc [in, optional]

Type: <b>TIMERPROC</b>

A pointer to the function to be notified when the time-out value elapses. For more information about the function, see <a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a>. If <i>lpTimerFunc</i> is <b>NULL</b>, the system posts a <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> message to the application queue. The <b>hwnd</b> member of the message's <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure contains the value of the <i>hWnd</i> parameter.

### -param uToleranceDelay [in]

Type: <b>ULONG</b>

It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TIMERV_DEFAULT_COALESCING"></a><a id="timerv_default_coalescing"></a><dl>
<dt><b>TIMERV_DEFAULT_COALESCING</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Uses the system default timer coalescing. 

</td>
</tr>
<tr>
<td width="40%"><a id="TIMERV_NO_COALESCING"></a><a id="timerv_no_coalescing"></a><dl>
<dt><b>TIMERV_NO_COALESCING</b></dt>
<dt>0xFFFFFFFF</dt>
</dl>
</td>
<td width="60%">
Uses no timer coalescing.  When this value is used, the created timer is not coalesced, no matter what the system default timer coalescing is or the application compatibility flags are.


<div class="alert"><b>Note</b>  Do not use this value unless you are certain that the  timer requires no coalescing. </div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1 - 0x7FFFFFF5</dt>
</dl>
</td>
<td width="60%">
Specifies the coalescing tolerance delay, in milliseconds. 

Applications should set this value to the system default (<b>TIMERV_DEFAULT_COALESCING</b>) or the largest value possible. 

If the sum of <i>uElapse</i> and <i>uToleranceDelay</i> exceeds <b>USER_TIMER_MAXIMUM</b> (0x7FFFFFFF), an ERROR_INVALID_PARAMETER exception occurs.

See <a href="https://download.microsoft.com/download/9/C/5/9C5B2167-8017-4BAE-9FDE-D599BAC8184A/TimerCoal.docx">Windows Timer Coalescing</a> for more details and best practices.

</td>
</tr>
<tr>
<td width="40%"><a id="Any_other_value"></a><a id="any_other_value"></a><a id="ANY_OTHER_VALUE"></a><dl>
<dt><b>Any other value</b></dt>
</dl>
</td>
<td width="60%">
An invalid value. If <i>uToleranceDelay</i> is set to an invalid value, the function fails and returns zero.  

</td>
</tr>
</table>

## -returns

Type: <b>UINT_PTR</b>

If the function succeeds and the <i>hWnd</i> parameter is <b>NULL</b>, the return value is an integer identifying the new timer. An application can pass this value to the <a href="/windows/desktop/api/winuser/nf-winuser-killtimer">KillTimer</a> function to destroy the timer.

If the function succeeds and the <i>hWnd</i> parameter is not <b>NULL</b>, then the return value is a nonzero integer. An application can pass the value of the <i>nIDEvent</i> parameter to the <a href="/windows/desktop/api/winuser/nf-winuser-killtimer">KillTimer</a> function to destroy the timer.

If the function fails to create a timer, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application can process <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> messages by including a <b>WM_TIMER</b> case statement in the window procedure or by specifying a <a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a> callback function when creating the timer. When you specify a <b>TimerProc</b> callback function, the default window procedure calls the callback function when it processes <b>WM_TIMER</b>. Therefore, you need to dispatch messages in the calling thread, even when you use <b>TimerProc</b> instead of processing <b>WM_TIMER</b>.

The <i>wParam</i> parameter of the <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> message contains the value of the <i>nIDEvent</i> parameter. 

The timer identifier, <i>nIDEvent</i>, is specific to the associated window. Another window can have its own timer which has the same identifier as a timer owned by another window. The timers are distinct. 


<a href="/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a> can reuse timer IDs in the case where <i>hWnd</i> is <b>NULL</b>. 
            

When <i>uToleranceDelay</i> is set to 0, the system default timer coalescing is used and   <b>SetCoalescableTimer</b>  behaves the same as <a href="/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a>.

Before using **SetCoalescableTimer** or other timer-related functions, it is recommended to set the **UOI_TIMERPROC_EXCEPTION_SUPPRESSION** flag to **false** through the **SetUserObjectInformationW** function, otherwise the application could behave unpredictably and could be vulnerable to security exploits. For more info, see <a href="/windows/win32/api/winuser/nf-winuser-setuserobjectinformationw">SetUserObjectInformationW</a>.

## -see-also

<a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/99647-Windows%208.1%20desktop%20samples/Coalescing%20timers%20sample/C%2B%2B">Coalescing timers sample</a>



<b>Conceptual</b>



<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kesetcoalescabletimer">KeSetCoalescableTimer</a>



<a href="/windows-hardware/drivers/ddi/content/wdm/nf-wdm-kesettimerex">KeSetTimer</a>



<a href="/windows/desktop/api/winuser/nf-winuser-killtimer">KillTimer</a>



<a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>



<b>Reference</b>



<b>Sample</b>



<a href="/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a>



<a href="/windows/desktop/api/winuser/nc-winuser-timerproc">TimerProc</a>



<a href="/windows/desktop/winmsg/timers">Timers</a>



<a href="/windows/desktop/winmsg/using-timers">Using Timers</a>



<a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a>
