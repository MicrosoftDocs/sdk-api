---
UID: NF:winbase.SetThreadExecutionState
title: SetThreadExecutionState function (winbase.h)
description: Enables an application to inform the system that it is in use, thereby preventing the system from entering sleep or turning off the display while the application is running.
helpviewer_keywords: ["ES_AWAYMODE_REQUIRED","ES_CONTINUOUS","ES_DISPLAY_REQUIRED","ES_SYSTEM_REQUIRED","ES_USER_PRESENT","SetThreadExecutionState","SetThreadExecutionState function","_win32_setthreadexecutionstate","base.setthreadexecutionstate","winbase/SetThreadExecutionState"]
old-location: base\setthreadexecutionstate.htm
tech.root: base
ms.assetid: 9214ea84-7636-4a78-91fd-a5a5da8199a1
ms.date: 12/05/2018
ms.keywords: ES_AWAYMODE_REQUIRED, ES_CONTINUOUS, ES_DISPLAY_REQUIRED, ES_SYSTEM_REQUIRED, ES_USER_PRESENT, SetThreadExecutionState, SetThreadExecutionState function, _win32_setthreadexecutionstate, base.setthreadexecutionstate, winbase/SetThreadExecutionState
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadExecutionState
 - winbase/SetThreadExecutionState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - Kernel32Legacy.dll
api_name:
 - SetThreadExecutionState
---

# SetThreadExecutionState function


## -description

Enables an application to inform the system that it is in use, thereby preventing the system from entering sleep or turning off the display while the application is running.

## -parameters

### -param esFlags [in]

The thread's execution requirements. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ES_AWAYMODE_REQUIRED"></a><a id="es_awaymode_required"></a><dl>
<dt><b>ES_AWAYMODE_REQUIRED</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Enables away mode. This value must be specified with <b>ES_CONTINUOUS</b>.

Away mode should be used only by media-recording and media-distribution applications that must perform critical background processing on desktop computers while the computer appears to be sleeping. See Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_CONTINUOUS"></a><a id="es_continuous"></a><dl>
<dt><b>ES_CONTINUOUS</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Informs the system that the state being set should remain in effect until the next call that uses <b>ES_CONTINUOUS</b> and one of the other state flags is cleared.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_DISPLAY_REQUIRED"></a><a id="es_display_required"></a><dl>
<dt><b>ES_DISPLAY_REQUIRED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Forces the display to be on by resetting the display idle timer.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_SYSTEM_REQUIRED"></a><a id="es_system_required"></a><dl>
<dt><b>ES_SYSTEM_REQUIRED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Forces the system to be in the working state by resetting the system idle timer.

</td>
</tr>
<tr>
<td width="40%"><a id="ES_USER_PRESENT"></a><a id="es_user_present"></a><dl>
<dt><b>ES_USER_PRESENT</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
This value is not supported. If <b>ES_USER_PRESENT</b> is combined with other <i>esFlags</i> values, the call will fail and  none of the specified states will be set.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is the previous thread execution state.

If the function fails, the return value is <b>NULL</b>.

## -remarks

The system automatically detects activities such as local keyboard or mouse input, server activity, and changing window focus. Activities that are not automatically detected include disk or CPU activity and video display.

Calling 
<b>SetThreadExecutionState</b> without <b>ES_CONTINUOUS</b> simply resets the idle timer; to keep the display or system in the working state, the thread must call 
<b>SetThreadExecutionState</b> periodically.

To run properly on a power-managed computer, applications such as fax servers, answering machines, backup agents, and network management applications must use both <b>ES_SYSTEM_REQUIRED</b> and <b>ES_CONTINUOUS</b> when they process events. Multimedia applications, such as video players and presentation applications, must use <b>ES_DISPLAY_REQUIRED</b> when they display video for long periods of time without user input. Applications such as word processors, spreadsheets, browsers, and games do not need to call 
<b>SetThreadExecutionState</b>.

The <b>ES_AWAYMODE_REQUIRED</b> value should be used only when absolutely necessary by media applications that require the system to perform background tasks such as recording television content or streaming media to other devices while the system appears to be sleeping. Applications that do not require critical background processing or that run on portable computers should not enable away mode because it prevents the system from conserving power by entering true sleep. 

To enable away mode, an application uses both <b>ES_AWAYMODE_REQUIRED</b> and <b>ES_CONTINUOUS</b>; to disable away mode, an application calls <b>SetThreadExecutionState</b> with <b>ES_CONTINUOUS</b> and clears <b>ES_AWAYMODE_REQUIRED</b>. When away mode is enabled, any operation that would put the computer to sleep puts it in away mode instead. The computer appears to be sleeping while the system continues to perform tasks that do not require user input.  Away mode does not affect the sleep idle timer; to prevent the system from entering sleep when the timer expires, an application must also set the <b>ES_SYSTEM_REQUIRED</b> value. 

The 
<b>SetThreadExecutionState</b> function cannot be used to prevent the user from putting the computer to sleep. Applications should respect that the user expects a certain behavior when they close the lid on their laptop or press the power button.

This function does not  stop the screen saver from executing. 


#### Examples


```cpp
// Television recording is beginning. Enable away mode and prevent
// the sleep idle time-out.
//
SetThreadExecutionState(ES_CONTINUOUS | ES_SYSTEM_REQUIRED | ES_AWAYMODE_REQUIRED);

//
// Wait until recording is complete...
//

//
// Clear EXECUTION_STATE flags to disable away mode and allow the system to idle to sleep normally.
//
SetThreadExecutionState(ES_CONTINUOUS);

```

## -see-also

<a href="/windows/desktop/Power/power-management-functions">Power Management Functions</a>



<a href="/windows/desktop/api/powrprof/nf-powrprof-setsuspendstate">SetSuspendState</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setsystempowerstate">SetSystemPowerState</a>



<a href="/windows/desktop/Power/wm-powerbroadcast">WM_POWERBROADCAST</a>