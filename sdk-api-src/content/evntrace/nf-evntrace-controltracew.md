---
UID: NF:evntrace.ControlTraceW
title: ControlTraceW function
author: windows-sdk-content
description: The ControlTrace function flushes, queries, updates, or stops the specified event tracing session.
old-location: etw\controltrace.htm
tech.root: ETW
ms.assetid: c39f669c-ff40-40ed-ba47-798474ec2de4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ControlTrace, ControlTrace function [ETW], ControlTraceA, ControlTraceW, EVENT_TRACE_CONTROL_FLUSH, EVENT_TRACE_CONTROL_QUERY, EVENT_TRACE_CONTROL_STOP, EVENT_TRACE_CONTROL_UPDATE, _evt_controltrace, base.controltrace, etw.controltrace, evntrace/ControlTrace, evntrace/ControlTraceA, evntrace/ControlTraceW
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
req.unicode-ansi: ControlTraceW (Unicode) and ControlTraceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - API-MS-Win-Eventing-Legacy-l1-1-0.dll
 - AdvApi32Legacy.dll
 - KernelBase.dll
api_name:
 - ControlTrace
 - ControlTraceA
 - ControlTraceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ControlTraceW
: 
---

# ControlTraceW function


## -description


The <b>ControlTrace</b> function flushes, queries, updates, or 
   stops the specified event tracing session.


## -parameters




### -param TraceHandle [in]

Handle to an event tracing session, or <b>NULL</b>. You must specify 
      <i>SessionHandle</i> if <i>SessionName</i> is 
      <b>NULL</b>. However, ETW ignores the handle if <i>SessionName</i> is not 
      <b>NULL</b>. The handle is returned by the 
      <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> function.


### -param InstanceName [in]

Name of an event tracing session, or <b>NULL</b>. You must specify 
      <i>SessionName</i> if <i>SessionHandle</i> is 
      <b>NULL</b>. 

To specify the NT Kernel Logger session, set <i>SessionName</i> to 
      <b>KERNEL_LOGGER_NAME</b>.


### -param Properties [in, out]

Pointer to an initialized 
       <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure. This structure 
       should be zeroed out before it is used.

If <i>ControlCode</i> specifies <b>EVENT_TRACE_CONTROL_STOP</b>, 
       <b>EVENT_TRACE_CONTROL_QUERY</b> or <b>EVENT_TRACE_CONTROL_FLUSH</b>, 
       you only need to set the <b>Wnode.BufferSize</b>, <b>Wnode.Guid</b>, 
       <b>LoggerNameOffset</b>, and <b>LogFileNameOffset</b> members of the 
       <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure. If the 
       session is a private session, you also need to set <b>LogFileMode</b>. You can use the 
       maximum session name (1024 characters) and maximum log file name (1024 characters) lengths to calculate the 
       buffer size and offsets if not known. 

If <i>ControlCode</i> specifies 
       <b>EVENT_TRACE_CONTROL_UPDATE</b>, on input, the members must specify the new values for the 
       properties to update. On output, <i>Properties</i> contains the properties and statistics 
       for the event tracing session. You can update the following properties.

<table>
<tr>
<th>Member</th>
<th>Use</th>
</tr>
<tr>
<td><b>EnableFlags</b></td>
<td>Set this member to 0 to disable all kernel providers. Otherwise, you must specify the kernel providers that you want to enable or keep enabled. Applies only to NT Kernel Logger sessions.</td>
</tr>
<tr>
<td><b>FlushTimer</b></td>
<td>Set this member if you want to change the time to wait before flushing buffers. If this member is 0, the member is not updated.</td>
</tr>
<tr>
<td><b>LogFileNameOffset</b></td>
<td>Set this member if you want to switch to another log file. If this member is 0, the file name is not updated. If the offset is not zero and you do not change the log file name, the function returns an error.</td>
</tr>
<tr>
<td><b>LogFileMode</b></td>
<td>Set this member if you want to turn <b>EVENT_TRACE_REAL_TIME_MODE</b> on and off. To turn real time consuming off, set this member to 0. To turn real time consuming on, set this member to <b>EVENT_TRACE_REAL_TIME_MODE</b> and it will be OR'd with the current modes.</td>
</tr>
<tr>
<td><b>MaximumBuffers</b></td>
<td>Set this member if you want to change the maximum number of buffers that ETW uses. If this member is 0, the member is not updated.</td>
</tr>
</table>
 

For private logger sessions, you can update only the <b>LogFileNameOffset</b> and 
       <b>FlushTimer</b> members.

If you are using a newly initialized 
       <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure, the only 
       members you need to specify, other than the members you are updating, are 
       <b>Wnode.BufferSize</b>, <b>Wnode.Guid</b>, and 
       <b>Wnode.Flags</b>.

If you use the property structure you passed to 
       <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>, make sure the 
       <b>LogFileNameOffset</b> member is 0 unless you are changing the log file name.

If you call the <b>ControlTrace</b> function to query the 
       current session properties and then update those properties to update the session, make sure you set 
       <b>LogFileNameOffset</b> to 0 (unless you are changing the log file name) and set 
       <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES.Wnode.Flags</a> to 
       <b>WNODE_FLAG_TRACED_GUID</b>.

<b>Starting with Windows 10, version 1703:  </b>For better performance in cross process scenarios, you can now pass filtering in to <b>ControlTrace</b> for  system wide private loggers. You will need to pass in the new <a href="https://msdn.microsoft.com/2EEDB53B-75BC-48AC-A70D-9AEAED526C40">EVENT_TRACE_PROPERTIES_V2</a> structure to include filtering information. See <a href="https://msdn.microsoft.com/fb6a3899-194e-4cb7-b9e5-a7ff85fb7891">Configuring and Starting a Private Logger Session</a> for more details.


### -param ControlCode [in]

Requested control function. You can specify one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_CONTROL_FLUSH"></a><a id="event_trace_control_flush"></a><dl>
<dt><b><b>EVENT_TRACE_CONTROL_FLUSH</b></b></dt>
</dl>
</td>
<td width="60%">
Flushes the session's active buffers. Typically, you do not need to flush buffers yourself. However, you may want to flush buffers if the event rate is low and you are delivering events in real time.

<b>Windows 2000:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_CONTROL_QUERY"></a><a id="event_trace_control_query"></a><dl>
<dt><b><b>EVENT_TRACE_CONTROL_QUERY</b></b></dt>
</dl>
</td>
<td width="60%">
Retrieves session properties and statistics.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_CONTROL_STOP"></a><a id="event_trace_control_stop"></a><dl>
<dt><b><b>EVENT_TRACE_CONTROL_STOP</b></b></dt>
</dl>
</td>
<td width="60%">
Stops the session. The session handle is no longer valid.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_CONTROL_UPDATE"></a><a id="event_trace_control_update"></a><dl>
<dt><b><b>EVENT_TRACE_CONTROL_UPDATE</b></b></dt>
</dl>
</td>
<td width="60%">
Updates the session properties.

</td>
</tr>
</table>
 

Note that it is not safe to flush buffers or stop a trace session from DllMain.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.
      

If the function fails, the return value is one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following table includes some 
       common errors and their causes.

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
<li>The <b>Wnode.BufferSize</b> member of <i>Properties</i> 
          specifies an incorrect size.</li>
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
<li>The <b>LogFileNameOffset</b> member of <i>Properties</i> is not valid.</li>
<li>The <b>LoggerNameOffset</b> member of <i>Properties</i> is not valid.</li>
<li>The <b>LogFileMode</b> member of <i>Properties</i> specifies a combination of flags that is not valid.</li>
<li>The <b>Wnode.Guid</b> member of <i>Properties</i> is <b>SystemTraceControlGuid</b>, but the <i>SessionName</i> parameter is not KERNEL_LOGGER_NAME.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
Another session is already using the file name specified by the 
        <b>LogFileNameOffset</b> member of the <i>Properties</i> structure.
       

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer for <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> is 
        too small to hold all the information for the session. If you do not need the session's property information, 
        you can ignore this error. If you receive this error when stopping the session, ETW will have already stopped 
        the session before generating this error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Only users running with elevated administrative privileges, users in the Performance Log Users group, and 
         services running as LocalSystem, LocalService, NetworkService can control event tracing sessions. To grant a 
         restricted user the ability to control trace sessions, add them to the Performance Log Users group. Only 
         users with administrative privileges and services running as LocalSystem can control an NT Kernel Logger 
         session.

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



Event trace controllers call this function.

This function supersedes the <a href="https://msdn.microsoft.com/bc7d0dac-93d9-4614-9cb6-fee99765eb39">FlushTrace</a>, 
    <a href="https://msdn.microsoft.com/8ad0f4f6-902c-490e-b26e-7499dd99fc95">QueryTrace</a>, 
    <a href="https://msdn.microsoft.com/604274a1-c4ed-4746-b69a-e18969f969db">StopTrace</a>, and 
    <a href="https://msdn.microsoft.com/40e6deaf-7363-45eb-80d0-bc3f33760875">UpdateTrace</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a>



<a href="https://msdn.microsoft.com/6b6144b0-9152-4b5e-863d-06e823fbe084">QueryAllTraces</a>



<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>
 

 

