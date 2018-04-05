---
UID: NS:wmistr._WNODE_HEADER
title: "_WNODE_HEADER"
author: windows-driver-content
description: The WNODE_HEADER structure is a member of the EVENT_TRACE_PROPERTIES structure.
old-location: etw\wnode_header.htm
old-project: ETW
ms.assetid: 862a8f46-a326-48c6-92b7-8bb667837bb7
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PWNODE_HEADER, PWNODE_HEADER, PWNODE_HEADER structure pointer [ETW], WNODE_HEADER, WNODE_HEADER structure [ETW], _WNODE_HEADER, _evt_wnode_header, base.wnode_header, etw.wnode_header, wmistr/PWNODE_HEADER, wmistr/WNODE_HEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wmistr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WNODE_HEADER, *PWNODE_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wmistr.h
api_name:
-	WNODE_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WNODE_HEADER structure


## -description



			The 
<b>WNODE_HEADER</b> structure is a member of the 
<a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure. 
		


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Version

Reserved for internal use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Linkage

Reserved for internal use.


### -field DUMMYUNIONNAME2

 


### -field BufferSize

Total size of memory allocated, in bytes, for the event tracing session properties. The size of memory must include the room for the <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure plus the session name string and log file name string that follow the structure in memory.


### -field ProviderId

Reserved for internal use.


### -field Guid

The GUID that you define for the session.

For an NT Kernel Logger session, set this member to <b>SystemTraceControlGuid</b>.

If this member is set to <b>SystemTraceControlGuid</b> or <b>GlobalLoggerGuid</b>, the logger will be a system logger.

For a private logger session, set this member to the provider's GUID that you are going to enable for the session.

If you start a session that is not a kernel logger or private logger session, you do not have to specify a session GUID. If you do not specify a GUID, ETW creates one for you. You need to specify a session GUID only if you want to change the default permissions associated with a specific session. For details, see the EventAccessControl function.

You cannot start  more than one session with the same session GUID.

<b>Prior to Windows Vista:  </b>You can start more than one session with the same session GUID.


### -field ClientContext

Clock resolution to use when logging the time stamp for each event. The default is Query performance counter (QPC). 

<b>Prior to Windows Vista:  </b>The default is system time.

<b>Prior to Windows 10, version 1703:  </b>No more than 2 distinct clock types can be used simultaneously by any system loggers.

<b>Starting with Windows 10, version 1703:  </b>The clock type restriction has been removed. All three clock types can now be used simultaneously by system loggers.


You can specify one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Query performance counter (QPC). The QPC counter provides a high-resolution time stamp that is not affected by adjustments to the system clock. The time stamp stored in the event is equivalent to the value returned from the QueryPerformanceCounter API. For more information on the characteristics of this time stamp, see <a href=" http://go.microsoft.com/fwlink/?LinkId=733315">Acquiring high-resolution time stamps</a>.

You should use this resolution if you have high event rates or if the consumer merges events from different buffers. In these cases, the precision and stability of the QPC time stamp allows for better accuracy in ordering the events from different buffers. However, the QPC time stamp will not reflect updates to the system clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the QPC time stamps in the trace will continue to reflect time as if no update had occurred.

To determine the resolution, use the <b>PerfFreq</b> member of <a href="https://msdn.microsoft.com/13fdabe6-c904-4546-b876-c145f6a6c345">TRACE_LOGFILE_HEADER</a> when consuming the event.

To convert an event’s time stamp into 100-ns units, use the following conversion formula: 

scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart * 10000000.0 / logfileHeader.PerfFreq.QuadPart

Note that on older computers, the time stamp may not be accurate because the counter sometimes skips forward due to hardware errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
System time. The system time provides a time stamp that tracks changes to the system’s clock, e.g. if the system clock is adjusted forward due to synchronization with an NTP server while the trace is in progress, the System Time time stamps in the trace will also jump forward to match the new setting of the system clock. 

<ul>
<li>On systems prior to Windows 10, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimeAsFileTime API.</li>
<li>On Windows 10 or later, the time stamp stored in the event is equivalent to the value returned from the GetSystemTimePreciseAsFileTime API.</li>
</ul>
Prior to Windows 10, the resolution of this time stamp was the resolution of a system clock tick, as indicated by the TimerResolution member of TRACE_LOGFILE_HEADER. Starting with Windows 10, the resolution of this time stamp is the performance counter resolution, as indicated by the PerfFreq member of TRACE_LOGFILE_HEADER.

To convert an event’s time stamp into 100-ns units, use the following conversion formula: 

scaledTimestamp = eventRecord.EventHeader.TimeStamp.QuadPart

Note that when events are captured on a system running an OS prior to Windows 10, if the volume of events is high, the resolution for system time may not be fine enough to determine the sequence of events. In this case, a set of events will have the same time stamp, but the order in which ETW delivers the events may not be correct. Starting with Windows 10, the time stamp is captured with additional precision, though some instability may still occur in cases where the system clock was adjusted while the trace was being captured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
CPU cycle counter. The CPU counter provides the highest resolution time stamp and is the least resource-intensive to retrieve. However, the CPU counter is unreliable and should not be used in production. For example, on some computers, the timers will change frequency due to thermal and power changes, in addition to stopping in some states.

To determine the resolution, use the <b>CpuSpeedInMHz</b> member of <a href="https://msdn.microsoft.com/13fdabe6-c904-4546-b876-c145f6a6c345">TRACE_LOGFILE_HEADER</a> when consuming the event.

If your hardware does not support this clock type, ETW uses system time.

<b>Windows Server 2003, Windows XP with SP1 and Windows XP:  </b>This value is not supported, it was introduced in Windows Server 2003 with SP1 and Windows XP with SP2.

</td>
</tr>
</table>
 

<b>Windows 2000:  </b>The <b>ClientContext</b> member is not supported.


### -field Flags

Must contain <b>WNODE_FLAG_TRACED_GUID</b> to indicate that the structure contains event tracing information.


#### - HistoricalContext

On output, the handle to the event tracing session.


#### - KernelHandle

Reserved for internal use.


#### - TimeStamp

Time at which the information in this structure was updated, in 100-nanosecond intervals since midnight, January 1, 1601.


## -remarks



Be sure to initialize the memory for this structure to zero before setting any members.



To convert an ETW timestamp into a FILETIME, use the following procedure:

The following steps should only be used if the trace is being processed with the PROCESS_TRACE_MODE_RAW_TIMESTAMP flag set.


DOUBLE timeStampScale = 10000000.0 / logFile.LogfileHeader.PerfFreq.QuadPart;

DOUBLE timeStampScale = 1.0;


Note that the remaining steps are unnecessary for events using system time, since the events already provide their time stamps in FILETIME units. The remaining steps will work but are unnecessary and will introduce a small rounding error.

DOUBLE timeStampScale = 10.0 / logFile.LogfileHeader.CpuSpeedInMHz;

INT64 timeStampBase =  logFile.LogfileHeader.StartTime.QuadPart - (INT64)(timeStampScale * eventRecord.EventHeader.TimeStamp.QuadPart);


INT64 timeStampInFileTime = timeStampBase + (INT64)(timeStampScale * eventRecord.EventHeader.TimeStamp.QuadPart);




## -see-also




<a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a>



<a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a>



<a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>
 

 

