---
UID: NF:winbase.WaitCommEvent
title: WaitCommEvent function (winbase.h)
description: Waits for an event to occur for a specified communications device. The set of events that are monitored by this function is contained in the event mask associated with the device handle.
helpviewer_keywords: ["EV_BREAK","EV_CTS","EV_DSR","EV_ERR","EV_RING","EV_RLSD","EV_RXCHAR","EV_RXFLAG","EV_TXEMPTY","WaitCommEvent","WaitCommEvent function","_win32_waitcommevent","base.waitcommevent","winbase/WaitCommEvent"]
old-location: base\waitcommevent.htm
tech.root: base
ms.assetid: 79e955c0-8756-4d6f-bce6-49e8e44d0d3f
ms.date: 12/05/2018
ms.keywords: EV_BREAK, EV_CTS, EV_DSR, EV_ERR, EV_RING, EV_RLSD, EV_RXCHAR, EV_RXFLAG, EV_TXEMPTY, WaitCommEvent, WaitCommEvent function, _win32_waitcommevent, base.waitcommevent, winbase/WaitCommEvent
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - WaitCommEvent
 - winbase/WaitCommEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - api-ms-win-core-comm-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - WaitCommEvent
---

# WaitCommEvent function


## -description

Waits for an event to occur for a specified communications device. The set of events that are monitored by this function is contained in the event mask associated with the device handle.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

### -param lpEvtMask [out]

A pointer to a variable that receives a mask indicating the type of event that occurred. If an error occurs, the value is zero; otherwise, it is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EV_BREAK"></a><a id="ev_break"></a><dl>
<dt><b>EV_BREAK</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
A break was detected on input.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_CTS"></a><a id="ev_cts"></a><dl>
<dt><b>EV_CTS</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The CTS (clear-to-send) signal changed state.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_DSR"></a><a id="ev_dsr"></a><dl>
<dt><b>EV_DSR</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The DSR (data-set-ready) signal changed state.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_ERR"></a><a id="ev_err"></a><dl>
<dt><b>EV_ERR</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
A line-status error occurred. Line-status errors are <b>CE_FRAME</b>, <b>CE_OVERRUN</b>, and <b>CE_RXPARITY</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RING"></a><a id="ev_ring"></a><dl>
<dt><b>EV_RING</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
A ring indicator was detected.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RLSD"></a><a id="ev_rlsd"></a><dl>
<dt><b>EV_RLSD</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The RLSD (receive-line-signal-detect) signal changed state.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RXCHAR"></a><a id="ev_rxchar"></a><dl>
<dt><b>EV_RXCHAR</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
A character was received and placed in the input buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RXFLAG"></a><a id="ev_rxflag"></a><dl>
<dt><b>EV_RXFLAG</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The event character was received and placed in the input buffer. The event character is specified in the device's 
<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a> structure, which is applied to a serial port by using the 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_TXEMPTY"></a><a id="ev_txempty"></a><dl>
<dt><b>EV_TXEMPTY</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The last character in the output buffer was sent.

</td>
</tr>
</table>

### -param lpOverlapped [in]

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. This structure is required if <i>hFile</i> was opened with <b>FILE_FLAG_OVERLAPPED</b>. 




If <i>hFile</i> was opened with <b>FILE_FLAG_OVERLAPPED</b>, the <i>lpOverlapped</i> parameter must not be <b>NULL</b>. It must point to a valid <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. If <i>hFile</i> was opened with <b>FILE_FLAG_OVERLAPPED</b> and <i>lpOverlapped</i> is <b>NULL</b>, the function can incorrectly report that the operation is complete.

If <i>hFile</i> was opened with <b>FILE_FLAG_OVERLAPPED</b> and <i>lpOverlapped</i> is not <b>NULL</b>, 
<b>WaitCommEvent</b> is performed as an overlapped operation. In this case, the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure must contain a handle to a manual-reset event object (created by using the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function).

If <i>hFile</i> was not opened with <b>FILE_FLAG_OVERLAPPED</b>, 
<b>WaitCommEvent</b> does not return until one of the specified events or an error occurs.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>WaitCommEvent</b> function monitors a set of events for a specified communications resource. To set and query the current event mask of a communications resource, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommmask">SetCommMask</a> and 
<a href="/windows/desktop/api/winbase/nf-winbase-getcommmask">GetCommMask</a> functions.

If the overlapped operation cannot be completed immediately, the function returns <b>FALSE</b> and the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_IO_PENDING</b>, indicating that the operation is executing in the background. When this happens, the system sets the <b>hEvent</b> member of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure to the not-signaled state before 
<b>WaitCommEvent</b> returns, and then it sets it to the signaled state when one of the specified events or an error occurs. The calling process can use one of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a> to determine the event object's state and then use the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> function to determine the results of the 
<b>WaitCommEvent</b> operation. 
<b>GetOverlappedResult</b> reports the success or failure of the operation, and the variable pointed to by the <i>lpEvtMask</i> parameter is set to indicate the event that occurred.

If a process attempts to change the device handle's event mask by using the 
<a href="/windows/desktop/api/winbase/nf-winbase-setcommmask">SetCommMask</a> function while an overlapped 
<b>WaitCommEvent</b> operation is in progress, 
<b>WaitCommEvent</b> returns immediately. The variable pointed to by the <i>lpEvtMask</i> parameter is set to zero.


#### Examples

For an example, see 
<a href="/windows/desktop/DevIO/monitoring-communications-events">Monitoring Communications Events</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/ns-winbase-dcb">DCB</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcommmask">GetCommMask</a>



<a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommmask">SetCommMask</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setcommstate">SetCommState</a>