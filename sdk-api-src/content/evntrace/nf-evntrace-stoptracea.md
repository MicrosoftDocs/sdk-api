---
UID: NF:evntrace.StopTraceA
title: StopTraceA function
author: windows-sdk-content
description: The StopTrace function stops the specified event tracing session. The ControlTrace function supersedes this function.
old-location: etw\stoptrace.htm
tech.root: ETW
ms.assetid: 604274a1-c4ed-4746-b69a-e18969f969db
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: StopTrace, StopTrace function [ETW], StopTraceA, StopTraceW, _evt_stoptrace, base.stoptrace, etw.stoptrace, evntrace/StopTrace, evntrace/StopTraceA, evntrace/StopTraceW
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
req.unicode-ansi: StopTraceW (Unicode) and StopTraceA (ANSI)
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
 - StopTrace
 - StopTraceA
 - StopTraceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StopTraceA function


## -description


The 
<b>StopTrace</b> function stops the specified event tracing session. 
   

The 
<a href="https://msdn.microsoft.com/c39f669c-ff40-40ed-ba47-798474ec2de4">ControlTrace</a> function supersedes this function.


## -parameters




### -param TraceHandle

TBD


### -param InstanceName

TBD


#### - Properties [out]

Pointer to an <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> 
      structure that receives the final properties and statistics for the session.

If you are using a newly 
      initialized structure, you only need to set the <b>Wnode.BufferSize</b>, 
      <b>Wnode.Guid</b>,  <b>LoggerNameOffset</b>, and 
      <b>LogFileNameOffset</b> members of the structure. You can use the maximum session name 
      (1024 characters) and maximum log file name (1024 characters) lengths to calculate the buffer size and offsets 
      if not known. 

<b>Starting with Windows 10, version 1703:  </b>For better performance in cross process scenarios, you can now pass filtering in to <b>StopTrace</b> for  system wide private loggers. You will need to pass in the new <a href="https://msdn.microsoft.com/2EEDB53B-75BC-48AC-A70D-9AEAED526C40">EVENT_TRACE_PROPERTIES_V2</a> structure to include filtering information. See <a href="https://msdn.microsoft.com/fb6a3899-194e-4cb7-b9e5-a7ff85fb7891">Configuring and Starting a Private Logger Session</a> for more details.


#### - SessionHandle [in]

Handle to the event tracing session that you want to stop, or <b>NULL</b>. You must 
      specify <i>SessionHandle</i> if <i>SessionName</i> is 
      <b>NULL</b>. However, ETW ignores the handle if <i>SessionName</i> is not 
      <b>NULL</b>. The handle is returned by the 
      <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> function.


#### - SessionName [in]

Pointer to a null-terminated string that specifies the name of the event tracing session that you want to 
      stop, or <b>NULL</b>. You must specify <i>SessionName</i> if 
      <i>SessionHandle</i> is <b>NULL</b>.

To specify the NT Kernel Logger session, set <i>SessionName</i> to 
      <b>KERNEL_LOGGER_NAME</b>.


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
Only users with administrative privileges, users in the Performance Log Users group, and services running as LocalSystem, LocalService, NetworkService can control event tracing sessions. To grant a restricted user the ability to control trace sessions, add them to the Performance Log Users group.

<b>Windows XP and Windows 2000:  </b>Anyone can control a trace session.

</td>
</tr>
</table>
 




## -remarks



Controllers call this function.

If <b>LogFileMode</b> contains <b>EVENT_TRACE_FILE_MODE_PREALLOCATE</b>, 
    <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> extends the log file to 
    <b>MaximumFileSize</b> bytes. The file occupies the entire space during logging, for both 
    circular and sequential logs. When you stop the logger, the log file is reduced to the size needed.

Note that it is not safe to stop a trace session from DllMain.




## -see-also




<a href="https://msdn.microsoft.com/c39f669c-ff40-40ed-ba47-798474ec2de4">ControlTrace</a>



<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>
 

 

