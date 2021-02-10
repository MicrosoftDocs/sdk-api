---
UID: NF:evntrace.StopTrace
title: StopTrace macro (evntrace.h)
description: The StopTrace function stops the specified event tracing session. The ControlTrace function supersedes this function.
helpviewer_keywords: ["StopTrace","StopTrace function [ETW]","StopTraceA","StopTraceW","_evt_stoptrace","base.stoptrace","etw.stoptrace","evntrace/StopTrace","evntrace/StopTraceA","evntrace/StopTraceW"]
old-location: etw\stoptrace.htm
tech.root: ETW
ms.assetid: 604274a1-c4ed-4746-b69a-e18969f969db
ms.date: 12/05/2018
ms.keywords: StopTrace, StopTrace function [ETW], StopTraceA, StopTraceW, _evt_stoptrace, base.stoptrace, etw.stoptrace, evntrace/StopTrace, evntrace/StopTraceA, evntrace/StopTraceW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StopTrace
 - evntrace/StopTrace
dev_langs:
 - c++
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
---

# StopTrace macro


## -description

The 
<b>StopTrace</b> function stops the specified event tracing session. 
   

The 
<a href="/windows/desktop/ETW/controltrace">ControlTrace</a> function supersedes this function.

## -parameters

### -param a [in]

Handle to the event tracing session that you want to stop, or <b>NULL</b>. You must 
      specify <i>SessionHandle</i> if <i>SessionName</i> is 
      <b>NULL</b>. However, ETW ignores the handle if <i>SessionName</i> is not 
      <b>NULL</b>. The handle is returned by the 
      <a href="/windows/desktop/ETW/starttrace">StartTrace</a> function.

### -param b [in]

Pointer to a null-terminated string that specifies the name of the event tracing session that you want to 
      stop, or <b>NULL</b>. You must specify <i>SessionName</i> if 
      <i>SessionHandle</i> is <b>NULL</b>.

To specify the NT Kernel Logger session, set <i>SessionName</i> to 
      <b>KERNEL_LOGGER_NAME</b>.

### -param c [out]

Pointer to an <a href="/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> 
      structure that receives the final properties and statistics for the session.

If you are using a newly 
      initialized structure, you only need to set the <b>Wnode.BufferSize</b>, 
      <b>Wnode.Guid</b>,  <b>LoggerNameOffset</b>, and 
      <b>LogFileNameOffset</b> members of the structure. You can use the maximum session name 
      (1024 characters) and maximum log file name (1024 characters) lengths to calculate the buffer size and offsets 
      if not known. 

<b>Starting with Windows 10, version 1703:  </b>For better performance in cross process scenarios, you can now pass filtering in to <b>StopTrace</b> for  system wide private loggers. You will need to pass in the new <a href="/windows/desktop/ETW/event-trace-properties-v2">EVENT_TRACE_PROPERTIES_V2</a> structure to include filtering information. See <a href="/windows/desktop/ETW/configuring-and-starting-a-private-logger-session">Configuring and Starting a Private Logger Session</a> for more details.

## -remarks

Controllers call this function.

If <b>LogFileMode</b> contains <b>EVENT_TRACE_FILE_MODE_PREALLOCATE</b>, 
    <a href="/windows/desktop/ETW/starttrace">StartTrace</a> extends the log file to 
    <b>MaximumFileSize</b> bytes. The file occupies the entire space during logging, for both 
    circular and sequential logs. When you stop the logger, the log file is reduced to the size needed.

Note that it is not safe to stop a trace session from DllMain.

## -see-also

<a href="/windows/desktop/ETW/controltrace">ControlTrace</a>



<a href="/windows/desktop/ETW/starttrace">StartTrace</a>

