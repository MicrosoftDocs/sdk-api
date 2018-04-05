---
UID: NS:evntrace._TRACE_LOGFILE_HEADER
title: "_TRACE_LOGFILE_HEADER"
author: windows-driver-content
description: The TRACE_LOGFILE_HEADER structure contains information about an event tracing session and its events.
old-location: etw\trace_logfile_header.htm
old-project: ETW
ms.assetid: 13fdabe6-c904-4546-b876-c145f6a6c345
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PTRACE_LOGFILE_HEADER, PTRACE_LOGFILE_HEADER, PTRACE_LOGFILE_HEADER structure pointer [ETW], TRACE_LOGFILE_HEADER, TRACE_LOGFILE_HEADER structure [ETW], _TRACE_LOGFILE_HEADER, _evt_trace_logfile_header, base.trace_logfile_header, etw.trace_logfile_header, evntrace/PTRACE_LOGFILE_HEADER, evntrace/TRACE_LOGFILE_HEADER"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACE_LOGFILE_HEADER, *PTRACE_LOGFILE_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Evntrace.h
api_name:
-	TRACE_LOGFILE_HEADER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _TRACE_LOGFILE_HEADER structure


## -description



			The 
TRACE_LOGFILE_HEADER structure contains information about an event tracing session and its events.
		



## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.VersionDetail


### -field DUMMYUNIONNAME.VersionDetail.MajorVersion

Major version number of the operating system.


### -field DUMMYUNIONNAME.VersionDetail.MinorVersion

Minor version number of the operating system.


### -field DUMMYUNIONNAME.VersionDetail.SubVersion

Reserved.


### -field DUMMYUNIONNAME.VersionDetail.SubMinorVersion

Reserved.


### -field DUMMYUNIONNAME2

 


### -field DUMMYUNIONNAME2.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME2.DUMMYSTRUCTNAME.StartBuffers

Reserved.


### -field DUMMYUNIONNAME2.DUMMYSTRUCTNAME.PointerSize

Size of a pointer data type, in bytes.


### -field DUMMYUNIONNAME2.DUMMYSTRUCTNAME.EventsLost

Number of events lost during the event tracing session. Events may be lost due to insufficient memory or a very high rate of incoming events.


### -field DUMMYUNIONNAME2.DUMMYSTRUCTNAME.CpuSpeedInMHz

 CPU speed, in megahertz.

<b>Windows 2000:  </b>This member is not supported.


### -field BufferSize

Size of the event tracing session's buffers, in bytes.


### -field ProviderVersion

Build number of the operating system.


### -field NumberOfProcessors

Number of processors on the system.


### -field EndTime

Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601. This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.


### -field TimerResolution

Resolution of the hardware timer, in units of 100 nanoseconds. For usage, see the Remarks for <a href="https://msdn.microsoft.com/library/windows/hardware/ff544329">EVENT_TRACE_HEADER</a>.


### -field MaximumFileSize

Maximum size of the log file, in megabytes.


### -field LogFileMode

Current logging mode for the event tracing session. For a list of values, see 
<a href="https://msdn.microsoft.com/d12aaecb-776a-4476-9ba4-16af30fde9c2">Logging Mode Constants</a>.


### -field BuffersWritten

Total number of buffers written by the event tracing session.


### -field LoggerName

Do not use.

The name of the event tracing session is the first null-terminated string following this structure in memory. 
					


### -field LogFileName

Do Not use.

The name of the event tracing log file is the second null-terminated string following this structure in memory. The first string is the name of the session. 
					


### -field TimeZone

A 
<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a> structure that contains the time zone for the <b>BootTime</b>, <b>EndTime</b> and <b>StartTime</b> members.


### -field BootTime

Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601. <b>BootTime</b> is  supported only for traces written to the Global Logger session.


### -field PerfFreq

Frequency of the high-resolution performance counter, if one exists.


### -field StartTime

Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.


### -field ReservedFlags

Specifies the clock type. For details, see the <b>ClientContext</b> member of <a href="https://msdn.microsoft.com/library/windows/hardware/ff566375">WNODE_HEADER</a>.


### -field BuffersLost

Total number of buffers lost during the event tracing session.


#### - LogInstanceGuid

Reserved.


#### - Version

Version number of the operating system. This is a roll-up of the members of <b>VersionDetail</b>. Starting with the low-order bytes, the first two bytes contain <b>MajorVersion</b>, the next two bytes contain <b>MinorVersion</b>, the next two bytes contain <b>SubVersion</b>, and the last two   bytes contain <b>SubMinorVersion</b>.


## -remarks



Be sure to initialize the memory for this structure to zero before setting any members.

The first event from any log file contains the data defined in this structure. You can use this structure to access the  event data or you can use the <a href="https://msdn.microsoft.com/3d0c4044-da06-4850-95c4-99b4ea28fcd9">EventTrace_Header</a> MOF class to decode the event data. Using this structure to read the event data may return unexpected results if the consumer is on a different computer from the one that generated the log file or the log file was written in a WOW (32-bit) session on a 64-bit computer. This is because the <b>LoggerName</b> and <b>LogFileName</b> members are pointers and can vary in size depending on the <b>PointerSize</b> member. 




## -see-also




<a href="https://msdn.microsoft.com/179451e9-7e3c-4d3a-bcc6-3ad9d382229a">EVENT_TRACE_LOGFILE</a>



<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>



<a href="https://msdn.microsoft.com/18c10ad6-8bc9-4a3b-a424-d17ee1d9e004">TIME_ZONE_INFORMATION</a>
 

 

