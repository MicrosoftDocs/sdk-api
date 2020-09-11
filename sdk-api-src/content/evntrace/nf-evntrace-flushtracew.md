---
UID: NF:evntrace.FlushTraceW
title: FlushTraceW function (evntrace.h)
description: The FlushTrace function causes an event tracing session to immediately deliver buffered events for the specified session.
helpviewer_keywords: ["FlushTrace","FlushTrace function [ETW]","FlushTraceA","FlushTraceW","_evt_flushtrace","base.flushtrace","etw.flushtrace","evntrace/FlushTrace","evntrace/FlushTraceA","evntrace/FlushTraceW"]
old-location: etw\flushtrace.htm
tech.root: ETW
ms.assetid: bc7d0dac-93d9-4614-9cb6-fee99765eb39
ms.date: 12/05/2018
ms.keywords: FlushTrace, FlushTrace function [ETW], FlushTraceA, FlushTraceW, _evt_flushtrace, base.flushtrace, etw.flushtrace, evntrace/FlushTrace, evntrace/FlushTraceA, evntrace/FlushTraceW
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FlushTraceW (Unicode) and FlushTraceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FlushTraceW
 - evntrace/FlushTraceW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-eventing-Legacy-l1-1-0.dll
 - advapi32legacy.dll
api_name:
 - FlushTrace
 - FlushTraceA
 - FlushTraceW
---

# FlushTraceW function


## -description

The 
<b>FlushTrace</b> function causes an event tracing session to immediately deliver buffered events for the specified session. (An event tracing session does not deliver events until an active buffer is full.) 

The <a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a> function supersedes this function.

## -parameters

### -param TraceHandle [in]

Handle to the event tracing session for whose buffers you want to flush, or <b>NULL</b>. You must specify <i>SessionHandle</i> if <i>SessionName</i> is <b>NULL</b>. However, ETW ignores the handle if <i>SessionName</i> is not <b>NULL</b>. The handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a> function.

### -param InstanceName [in]

Pointer to a null-terminated string that specifies the name of the event tracing session whose buffers you want to flush, or <b>NULL</b>. You must specify <i>SessionName</i> if <i>SessionHandle</i> is <b>NULL</b>.

To specify the NT Kernel Logger session, set <i>SessionName</i> to <b>KERNEL_LOGGER_NAME</b>.

### -param Properties [in, out]

Pointer to an 
initialized <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> structure. 




If you are using a newly initialized structure, you only need to set the <b>Wnode.BufferSize</b>, <b>Wnode.Guid</b>,  <b>LoggerNameOffset</b>, and <b>LogFileNameOffset</b> members of the structure. You can use the maximum session name (1024 characters) and maximum log file name (1024 characters) lengths to calculate the buffer size and offsets if not known. 

On output, the structure receives the property settings and session statistics of the event tracing session, which  reflect the state of the session after the flush.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true: 




<ul>
<li><i>Properties</i> is <b>NULL</b>.</li>
<li><i>SessionName</i> and <i>SessionHandle</i> are both <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true:

<ul>
<li>The <b>Wnode.BufferSize</b> member of <i>Properties</i> specifies an incorrect size.</li>
<li><i>Properties</i> does not have sufficient space allocated to hold a copy of the session name and log file name (if used).</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Only users with administrative privileges, users in the Performance Log Users group, and services running as LocalSystem, LocalService, NetworkService can control event tracing sessions. To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.

<b>Windows XP and Windows 2000:  </b>Anyone can control a trace session.

</td>
</tr>
</table>

## -remarks

Controllers call this function.

Typically, you do not need to flush buffers yourself. However, you may want to flush buffers if the event rate is low and you are delivering events in real time.

Note that it is not safe to flush buffers from DllMain.





> [!NOTE]
> The evntrace.h header defines FlushTrace as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a>

