---
UID: NF:evntrace.StartTraceA
title: StartTraceA function (evntrace.h)
description: The StartTrace function registers and starts an event tracing session.
old-location: etw\starttrace.htm
tech.root: ETW
ms.assetid: c040514a-733d-44b9-8300-a8341d2630b3
ms.date: 12/05/2018
ms.keywords: StartTrace, StartTrace function [ETW], StartTraceA, StartTraceW, _evt_starttrace, base.starttrace, etw.starttrace, evntrace/StartTrace, evntrace/StartTraceA, evntrace/StartTraceW
f1_keywords:
- evntrace/StartTrace
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
req.unicode-ansi: StartTraceW (Unicode) and StartTraceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista and Windows XP
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Sechost.dll
- Advapi32.dll
- AdvApi32Legacy.dll
- API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
- API-MS-Win-Eventing-Controller-l1-1-0.dll
- API-MS-Win-Eventing-Legacy-l1-1-0.dll
- KernelBase.dll
api_name:
- StartTrace
- StartTraceA
- StartTraceW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StartTraceA function


## -description


The <b>StartTrace</b> function registers and starts an event 
   tracing session.


## -parameters




### -param TraceHandle [out]

Handle to the event tracing session.

Do not use this handle if the function fails. Do not compare the session handle to INVALID_HANDLE_VALUE; the 
       session handle is 0 if the handle is not valid.


### -param InstanceName [in]

Null-terminated string that contains the name of the event tracing session. The session name is limited to 
       1,024 characters, is case-insensitive, and must be unique.

<b>Windows 2000:  </b>Session names are case-sensitive. As a result, duplicate session names are allowed. However, to reduce 
        confusion, you should make sure your session names are unique.

This function copies the session name that you provide to the offset that the 
       <b>LoggerNameOffset</b> member of <i>Properties</i> points to.


### -param Properties [in, out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> 
       structure that specifies the behavior of the session. The following are key members of the structure to set:

<ul>
<li><b>Wnode.BufferSize</b></li>
<li><b>Wnode.Guid</b></li>
<li><b>Wnode.ClientContext</b></li>
<li><b>Wnode.Flags</b></li>
<li><b>LogFileMode</b></li>
<li><b>LogFileNameOffset</b></li>
<li><b>LoggerNameOffset</b></li>
</ul>
Depending on the type of log file you choose to create, you may also need to specify a value for <b>MaximumFileSize</b>. See the Remarks section for more information on setting the <i>Properties</i> parameter and the behavior of the session.

<b>Starting with Windows 10, version 1703:  </b>For better performance in cross process scenarios, you can now pass filtering in to <b>StartTrace</b> when starting system wide private loggers. You will need to pass in the new <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties-v2">EVENT_TRACE_PROPERTIES_V2</a> structure to include filtering information. See <a href="https://docs.microsoft.com/windows/desktop/ETW/configuring-and-starting-a-private-logger-session">Configuring and Starting a Private Logger Session</a> for more details.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.
      

If the function fails, the return value is one of the 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some 
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
<li>The <b>Wnode.BufferSize</b> member of  <i>Properties</i> specifies an incorrect size.</li>
<li><i>Properties</i> does not have sufficient space allocated to hold a copy of <i>SessionName</i>.</li>
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
<li><i>SessionHandle</i> is <b>NULL</b>.</li>
<li>The <b>LogFileNameOffset</b> member of <i>Properties</i> is not valid.</li>
<li>The <b>LoggerNameOffset</b> member of <i>Properties</i> is not valid.</li>
<li>The <b>LogFileMode</b> member of <i>Properties</i> specifies a combination of flags that is not valid.</li>
<li>The <b>Wnode.Guid</b> member is <b>SystemTraceControlGuid</b>, but the <i>SessionName</i> parameter is not <b>KERNEL_LOGGER_NAME</b>.<b>Windows 2000:  </b>This case does not return an error.

</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALREADY_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
A session with the same name or GUID is already running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
You can receive this error for one of the following reasons:

<ul>
<li>Another session is already using the file name specified by the 
          <b>LogFileNameOffset</b> member of the <i>Properties</i> 
          structure.</li>
<li>Both <b>LogFileMode</b> and <b>LogFileNameOffset</b> are 
          zero.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DISK_FULL</b></dt>
</dl>
</td>
<td width="60%">
There is not enough free space on the drive for the log file. This occurs if:

<ul>
<li><b>MaximumFileSize</b> is nonzero and there is not <b>MaximumFileSize</b> bytes available for the log file</li>
<li>the drive is a system drive and there is not an additional 200 MB available</li>
<li><b>MaximumFileSize</b> is zero and there is not an additional 200 MB available</li>
</ul>
  Choose a drive with more space, or decrease the size specified in <b>MaximumFileSize</b> (if used).

<b>Windows 2000:  </b>Does not require an additional 200 MB available disk space. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Only users with administrative privileges, users in the Performance Log Users group, and services running 
         as LocalSystem, LocalService, NetworkService can control event tracing sessions. To grant a restricted user 
         the ability to control trace sessions, add them to the Performance Log Users group. Only users with 
         administrative privileges and services running as LocalSystem can control an NT Kernel Logger session.

<b>Windows XP and Windows 2000:  </b>Anyone can control a trace session.

If the user is a member of the  Performance Log Users group, they may not have permission to create the log 
         file in the specified folder.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
The maximum number of logging sessions on the system has been reached.  No new loggers can be created until a logging session has been stopped.  This value defaults to 64 on most systems.

  You can change this value by editing the <b>REG_DWORD</b> key at <b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\WMI\EtwMaxLoggers</b>. Permissible values are 32 through 256, inclusive.  A reboot is required for any change to take effect.  

Note that Loggers use system resources.  Increasing the number of loggers on the system will come at a performance cost if those slots are filled.  

Prior to Windows 10, version 1709, this is a fixed cap of 64 loggers for non-private loggers.

</td>
</tr>
</table>
 




## -remarks



Event trace controllers call this function.

The session remains active until you stop the session, the computer is restarted or the maximum file size is 
    reached for non-circular logs. To stop an event tracing session, call the 
    <a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a> function and set the 
    <i>ControlCode</i> parameter to <b>EVENT_TRACE_CONTROL_STOP</b>.

You cannot start  more than one session with the same session GUID.

<b>Windows Server 2003:  </b>You can start more than one session with the same session GUID.

For the logger to be a system logger and receive events from <a href="https://docs.microsoft.com/windows/desktop/ETW/configuring-and-starting-a-systemtraceprovider-session">SystemTraceProvider</a>, any of the following must be true:<ul>
<li>The <i>Properties</i> member <b>Wnode.Guid</b> is set to <b>SystemTraceControlGuid</b> or <b>GlobalLoggerGuid</b>.</li>
<li>The <i>Properties</i> member <b>LogFileMode</b> includes the <b>EVENT_TRACE_SYSTEM_LOGGER_MODE</b> flag.</li>
<li><i>SessionName</i> is set to <b>KERNEL_LOGGER_NAME</b>.</li>
</ul>
<div class="alert"><b>Note</b>  A system logger must set the <b>EnableFlags</b> member of the <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> structure to indicate which <a href="https://docs.microsoft.com/windows/desktop/ETW/configuring-and-starting-a-systemtraceprovider-session">SystemTraceProvider</a> events should be included in the trace.</div>
<div> </div>


Because system loggers receive special kernel events, they are subject to additional restrictions:<ul>
<li>There can be no more than 8 system loggers active on the same system.</li>
<li>System loggers cannot be created within a Windows Server container.</li>
<li>System loggers cannot use the <b>EVENT_TRACE_USE_PAGED_MEMORY</b> flag.</li>
<li>Prior to Windows 10, version 1703, no more than  2 distinct clock types can be used simultaneously by any system loggers. For example, if one active system logger is using the "CPU cycle counter" clock type, and another active system logger is using the "Query performance counter" clock type, then any attempt to start a system logger using the "System time" clock type will fail because it would require the activation of a third clock type. Because of this limitation, Microsoft  strongly recommends that system loggers do not use the "System time" clock type.</li>
<li>Starting with Windows 10, version 1703, the clock type restriction has been removed. All three clock types can now be used simultaneously by system loggers.</li>
</ul>


To specify an NT Kernel Logger session, set <i>SessionName</i> to 
     <b>KERNEL_LOGGER_NAME</b> and the <b>Wnode.Guid</b> member of 
     <i>Properties</i> to <b>SystemTraceControlGuid</b>. If you do not specify 
     the GUID as <b>SystemTraceControlGuid</b>, ETW will override the GUID value and set it to 
     <b>SystemTraceControlGuid</b>.

<b>Windows 2000:  </b>To start the kernel session, the session name must be <b>KERNEL_LOGGER_NAME</b> and the GUID must be <b>SystemTraceControlGuid</b>.

To specify a private logger session, set <b>Wnode.Guid</b> member of 
    <i>Properties</i> to the provider's control GUID, not the private logger session's control 
    GUID. The provider must have registered the GUID before you call 
    <b>StartTrace</b>.

You do not use this function to start a global logger session. For details on starting a global logger 
    session, see 
    <a href="https://docs.microsoft.com/windows/desktop/ETW/configuring-and-starting-the-global-logger-session">Configuring and Starting the Global Logger Session</a>.


#### Examples

For an example that uses <b>StartTrace</b>, see 
     <a href="https://docs.microsoft.com/windows/desktop/ETW/configuring-and-starting-an-event-tracing-session">Configuring and Starting an Event Tracing Session</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a>
 

 

