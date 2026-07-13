---
UID: NF:winuser.WaitForInputIdle
title: WaitForInputIdle function (winuser.h)
description: Waits until the specified process has finished processing its initial input and is waiting for user input with no input pending, or until the time-out interval has elapsed.
helpviewer_keywords: ["WaitForInputIdle","WaitForInputIdle function","_win32_waitforinputidle","base.waitforinputidle","winuser/WaitForInputIdle"]
old-location: base\waitforinputidle.htm
tech.root: backup
ms.assetid: 2a684921-36f1-438c-895c-5bebc242635a
ms.date: 12/05/2018
ms.keywords: WaitForInputIdle, WaitForInputIdle function, _win32_waitforinputidle, base.waitforinputidle, winuser/WaitForInputIdle
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WaitForInputIdle
 - winuser/WaitForInputIdle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ntuser-misc-l1-7-0.dll
 - ext-ms-win-ntuser-misc-l1-6-0.dll
 - User32.dll
 - Ext-MS-Win-NTUser-Misc-l1-1-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-2-0.dll
 - Ext-MS-Win-NTUser-Misc-l1-3-0.dll
 - ext-ms-win-ntuser-misc-l1-3-1.dll
 - Ext-MS-Win-NTUser-Misc-L1-4-0.dll
 - Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
 - Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
 - WaitForInputIdle
req.apiset: ext-ms-win-ntuser-misc-l1-1-0 (introduced in Windows 8)
---

# WaitForInputIdle function


## -description

Waits until the specified process has finished processing its initial input and is waiting for user input with no input pending, or until the time-out interval has elapsed.

## -parameters

### -param hProcess [in]

A handle to the process. If this process is a console application or does not have a message queue, 
<b>WaitForInputIdle</b> returns immediately.

### -param dwMilliseconds [in]

The time-out interval, in milliseconds. If <i>dwMilliseconds</i> is INFINITE, the function does not return until the process is idle.

## -returns

The following table shows the possible return values for this function.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The wait was satisfied successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The wait was terminated because the time-out interval elapsed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAIT_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An error occurred.

</td>
</tr>
</table>

## -remarks

The 
<b>WaitForInputIdle</b> function enables a thread to suspend its execution until the specified process has finished its initialization and is waiting for user input with no input pending. If the process has multiple threads, the <b>WaitForInputIdle</b> function returns as soon as any thread becomes idle. 

<b>WaitForInputIdle</b>  can be used at any time, not just during application startup. However, <b>WaitForInputIdle</b> waits only once for a process to become idle; subsequent <b>WaitForInputIdle</b> calls return immediately, whether the process is idle or busy. 

<b>WaitForInputIdle</b> can be useful for synchronizing a parent process and a newly created child process. When a parent process creates a child process, the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function returns without waiting for the child process to finish its initialization. Before trying to communicate with the child process, the parent process can use 
the <b>WaitForInputIdle</b> function to determine when the child's initialization has been completed. For example, the parent process should use 
the <b>WaitForInputIdle</b> function before trying to find a window associated with the child process.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/synchronizing-execution-of-multiple-threads">Synchronizing Execution of Multiple Threads</a>
