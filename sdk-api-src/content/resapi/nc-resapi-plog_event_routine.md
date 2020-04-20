---
UID: NC:resapi.PLOG_EVENT_ROUTINE
title: PLOG_EVENT_ROUTINE (resapi.h)
description: Records an event in the cluster log.helpviewer_keywords: ["LOG_ERROR","LOG_INFORMATION","LOG_SEVERE","LOG_WARNING","LogEvent","LogEvent callback","LogEvent callback function [Failover Cluster]","PLOG_EVENT_ROUTINE","PLOG_EVENT_ROUTINE callback function [Failover Cluster]","_wolf_logevent","mscs.logevent","resapi/LogEvent","resapi/PLOG_EVENT_ROUTINE"]
old-location: mscs\logevent.htm
tech.root: MsCS
ms.assetid: 91389083-e007-4d64-885f-e5188e74b9d8
ms.date: 12/05/2018
ms.keywords: LOG_ERROR, LOG_INFORMATION, LOG_SEVERE, LOG_WARNING, LogEvent, LogEvent callback, LogEvent callback function [Failover Cluster], PLOG_EVENT_ROUTINE, PLOG_EVENT_ROUTINE callback function [Failover Cluster], _wolf_logevent, mscs.logevent, resapi/LogEvent, resapi/PLOG_EVENT_ROUTINE
f1_keywords:
- resapi/LogEvent
dev_langs:
- c++
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- ResApi.h
api_name:
- LogEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PLOG_EVENT_ROUTINE callback function


## -description


Records an event in the 
    cluster log. The <b>PLOG_EVENT_ROUTINE</b> type defines a pointer to this function.


## -parameters




### -param ResourceHandle [in]

Handle identifying the resource recording the event. The value for <i>ResourceHandle</i> 
       should be the handle passed in during the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> call for this 
       resource.


### -param LogLevel [in]

Value enumerated by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/ne-resapi-log_level">LOG_LEVEL</a> enumeration that 
       represents the log level of the event and that is for information only. The following valid values are shown in 
       order from least to most severe.



#### LOG_INFORMATION (0)

The event is informational.



#### LOG_WARNING (1)

The event is reporting a failure that might have happened, but it is uncertain whether a failure really did 
         occur.



#### LOG_ERROR (2)

The event affects a single component, but other components are not affected and the integrity of the rest 
         of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/nodes">node</a> is not compromised.



#### LOG_SEVERE (3)

The event is reporting a severe failure that affects multiple components, or the integrity of the entire 
         system is compromised or believed to be compromised.


### -param FormatString [in]

Null-terminated Unicode string that includes the information to be recorded. This string must be in the same 
       format as that passed to the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> 
       function.


### -param Arg1








####### - ...

Arguments to be passed to <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> along with 
       <i>FormatString</i>. Any number of arguments may be specified as long as they work with 
       <i>FormatString</i> to satisfy the syntax requirements of 
       <b>FormatMessage</b>. Arguments must be separated by 
       commas.


## -remarks



The <i>LogEvent</i> callback function is implemented by the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-monitor">Resource Monitor</a> and is called by a 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a> to report events and errors to the cluster log. 
     Resource DLLs receive a pointer to the <i>LogEvent</i> callback 
     function in the <i>LogEvent</i> parameter to their 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a> entry-point function.

<i>LogEvent</i> does not write entries to the event log. To 
     report events in the event log, a resource DLL must call the 
     <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-reporteventa">ReportEvent</a> function.

The format of the logged message appears as follows:

<i>ResourceTypeName</i><b>
</b><i>ResourceName</i><b>: </b><i>message</i>

<i>ResourceTypeName</i> is the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-types">resource type</a>, such as 
     "Generic Application". The specific resource name is the user-friendly name for the specific 
     resource, and message is the message delivered by the resource DLL to the Resource Monitor.

The log entry size is limited to 500 characters.


#### Examples

The following example is based on code generated by the Cluster Resource Type Wizard. For additional 
     examples, see <a href="https://docs.microsoft.com/previous-versions/aa372246(v=vs.85)">Resource DLL Examples</a>.

<pre class="syntax" xml:space="preserve"><code>//  The following parameters are assumed to be already defined:
//  g_pfnLogEvent   Stores the address of the LogEvent callback
//                  function passed to the DLL in the
//                  Startup entry point.
//  pResourceEntry  Stores resource instance data.
//  MY_SVCNAME      Stores the name of a service.
//  nStatus         Result

//  Log the fact that an attempt to start a service has failed.

//  Basic message
    (g_pfnLogEvent)( pResourceEntry-&gt;hResourceHandle,
                     LOG_ERROR,
                     L"Failed to start the specified service.\n" );

//  Message w/string argument
    (g_pfnLogEvent)( pResourceEntry-&gt;hResourceHandle,
                     LOG_ERROR,
                     L"OnlineThread: Failed to start the '%1' service.\n",
                     MY_SVCNAME );

//  Message w/multiple arguments
    (g_pfnLogEvent)( pResourceEntry-&gt;hResourceHandle,
                     LOG_ERROR,
                     L"OnlineThread: Failed to start the '%1' service. Error: %2!u!.\n",
                     MY_SVCNAME,
                     nStatus );</code></pre>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/ne-resapi-log_level">LOG_LEVEL</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-reporteventa">ReportEvent</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-dll-callback-functions">Resource DLL Callback Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pstartup_routine">Startup</a>
 

 

