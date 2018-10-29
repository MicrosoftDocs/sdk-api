---
UID: NF:evntrace.QueryTraceW
title: QueryTraceW function
author: windows-sdk-content
description: The QueryTrace function retrieves the property settings and session statistics for the specified event tracing session. The ControlTrace function supersedes this function.
old-location: etw\querytrace.htm
tech.root: ETW
ms.assetid: 8ad0f4f6-902c-490e-b26e-7499dd99fc95
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: QueryTrace, QueryTrace function [ETW], QueryTraceA, QueryTraceW, _evt_querytrace, base.querytrace, etw.querytrace, evntrace/QueryTrace, evntrace/QueryTraceA, evntrace/QueryTraceW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryTraceW function


## -description


The 
<b>QueryTrace</b> function retrieves the property settings and session statistics for the specified event tracing session. 
			

The 
<a href="https://msdn.microsoft.com/c39f669c-ff40-40ed-ba47-798474ec2de4">ControlTrace</a> function supersedes this function.


## -parameters




### -param TraceHandle

TBD


### -param InstanceName

TBD


#### - Properties [in, out]

Pointer to an 
initialized <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure. 




You only need to set the <b>Wnode.BufferSize</b> member of the <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure. You can use the maximum session name (1024 characters) and maximum log file name (1024 characters) lengths to calculate the buffer size and offsets if not known. 

On output, the structure members contain the property settings and session statistics for the event tracing session. 

<b>Starting with Windows 10, version 1703:  </b>For better performance in cross process scenarios, you can now pass filtering in to <b>QueryTrace</b> for  system wide private loggers. You will need to pass in the new <a href="https://msdn.microsoft.com/2EEDB53B-75BC-48AC-A70D-9AEAED526C40">EVENT_TRACE_PROPERTIES_V2</a> structure to include filtering information. See <a href="https://msdn.microsoft.com/fb6a3899-194e-4cb7-b9e5-a7ff85fb7891">Configuring and Starting a Private Logger Session</a> for more details.


#### - SessionHandle [in]

Handle to the event tracing session for whose properties and statistics you want to query, or <b>NULL</b>. You must specify <i>SessionHandle</i> if <i>SessionName</i> is <b>NULL</b>. However, ETW ignores the handle if <i>SessionName</i> is not <b>NULL</b>. The handle is returned by the 
<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> function.


#### - SessionName [in]

Pointer to a null-terminated string that specifies the name of the event tracing session whose properties and statistics you want to query, or <b>NULL</b>. You must specify <i>SessionName</i> if <i>SessionHandle</i> is <b>NULL</b>.

To specify the NT Kernel Logger session, set <i>SessionName</i> to <b>KERNEL_LOGGER_NAME</b>.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following table includes some common errors and their causes.

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
Only users running with elevated administrative privileges, users in the Performance Log Users group, and services running as LocalSystem, LocalService, NetworkService can query event tracing sessions. To grant a restricted user the ability to query trace sessions, add them to the Performance Log Users group or see <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>.

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
<a href="https://msdn.microsoft.com/40e6deaf-7363-45eb-80d0-bc3f33760875">UpdateTrace</a> function.




## -see-also




<a href="https://msdn.microsoft.com/c39f669c-ff40-40ed-ba47-798474ec2de4">ControlTrace</a>



<a href="https://msdn.microsoft.com/6b6144b0-9152-4b5e-863d-06e823fbe084">QueryAllTraces</a>
 

 

