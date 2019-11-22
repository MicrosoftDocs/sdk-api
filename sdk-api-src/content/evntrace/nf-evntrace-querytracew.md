---
UID: NF:evntrace.QueryTraceW
title: QueryTraceW function (evntrace.h)

description: The QueryTrace function retrieves the property settings and session statistics for the specified event tracing session. The ControlTrace function supersedes this function.
old-location: etw\querytrace.htm
tech.root: ETW
ms.assetid: 8ad0f4f6-902c-490e-b26e-7499dd99fc95

ms.date: 12/05/2018
ms.keywords: QueryTrace, QueryTrace function [ETW], QueryTraceA, QueryTraceW, _evt_querytrace, base.querytrace, etw.querytrace, evntrace/QueryTrace, evntrace/QueryTraceA, evntrace/QueryTraceW
ms.topic: function
f1_keywords: 
 - "evntrace/QueryTrace"
dev_langs:
 - c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QueryTraceW (Unicode) and QueryTraceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
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
 - QueryTrace
 - QueryTraceA
 - QueryTraceW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryTraceW function


## -description


The 
<b>QueryTrace</b> function retrieves the property settings and session statistics for the specified event tracing session. 
			

The 
<a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a> function supersedes this function.


## -parameters




### -param TraceHandle

Handle to the event tracing session for whose properties and statistics you want to query, or <b>NULL</b>. You must specify <i>SessionHandle</i> if <i>SessionName</i> is <b>NULL</b>. However, ETW ignores the handle if <i>SessionName</i> is not <b>NULL</b>. The handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a> function.


### -param InstanceName


Pointer to a null-terminated string that specifies the name of the event tracing session whose properties and statistics you want to query, or <b>NULL</b>. You must specify <i>SessionName</i> if <i>SessionHandle</i> is <b>NULL</b>.

To specify the NT Kernel Logger session, set <i>SessionName</i> to <b>KERNEL_LOGGER_NAME</b>.


### -param Properties

Pointer to an 
initialized <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> structure. 




You only need to set the <b>Wnode.BufferSize</b> member of the <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> structure. You can use the maximum session name (1024 characters) and maximum log file name (1024 characters) lengths to calculate the buffer size and offsets if not known. 

On output, the structure members contain the property settings and session statistics for the event tracing session. 

<b>Starting with Windows 10, version 1703:  </b>For better performance in cross process scenarios, you can now pass filtering in to <b>QueryTrace</b> for  system wide private loggers. You will need to pass in the new <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties-v2">EVENT_TRACE_PROPERTIES_V2</a> structure to include filtering information. See <a href="https://docs.microsoft.com/windows/desktop/ETW/configuring-and-starting-a-private-logger-session">Configuring and Starting a Private Logger Session</a> for more details.



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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Only users running with elevated administrative privileges, users in the Performance Log Users group, and services running as LocalSystem, LocalService, NetworkService can query event tracing sessions. To grant a restricted user the ability to query trace sessions, add them to the Performance Log Users group or see <a href="https://docs.microsoft.com/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a>.

<b>Windows XP and Windows 2000:  </b>Anyone can control a trace session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_INSTANCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The given session is not running.

</td>
</tr>
</table>
 




## -remarks



Controllers call this function.

To update the property settings and session statistics for an event tracing session, call the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/updatetrace">UpdateTrace</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/queryalltraces">QueryAllTraces</a>
 

 

