---
UID: NF:winuser.KillTimer
title: KillTimer function (winuser.h)
description: Destroys the specified timer.
helpviewer_keywords: ["KillTimer","KillTimer function [Windows and Messages]","_win32_KillTimer","_win32_killtimer_cpp","winmsg.killtimer","winui._win32_killtimer","winuser/KillTimer"]
old-location: winmsg\killtimer.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\timers\timerreference\timerfunctions\killtimer.htm
ms.date: 12/05/2018
ms.keywords: KillTimer, KillTimer function [Windows and Messages], _win32_KillTimer, _win32_killtimer_cpp, winmsg.killtimer, winui._win32_killtimer, winuser/KillTimer
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
 - KillTimer
 - winuser/KillTimer
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
 - KillTimer
req.apiset: ext-ms-win-ntuser-window-l1-1-2 (introduced in Windows 10, version 10.0.10240)
---

# KillTimer function


## -description

Destroys the specified timer.

## -parameters

### -param hWnd [in, optional]

Type: <b>HWND</b>

A handle to the window associated with the specified timer. This value must be the same as the 
					<i>hWnd</i> value passed to the <a href="/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a> function that created the timer.

### -param uIDEvent [in]

Type: <b>UINT_PTR</b>

The timer to be destroyed. If the window handle passed to <a href="/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a> is valid, this parameter must be the same as the
					<i>nIDEvent</i> 

value passed to <b>SetTimer</b>. If the application calls <b>SetTimer</b> with 
					<i>hWnd</i> set to <b>NULL</b>, this parameter must be the timer identifier returned by <b>SetTimer</b>.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>KillTimer</b> function does not remove <a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a> messages already posted to the message queue.


#### Examples

For an example, see <a href="/windows/desktop/winmsg/using-timers">Destroying a Timer</a>.

<div class="code"></div>

## -see-also

<b>Conceptual</b>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-settimer">SetTimer</a>



<a href="/windows/desktop/winmsg/timers">Timers</a>



<a href="/windows/desktop/winmsg/wm-timer">WM_TIMER</a>
