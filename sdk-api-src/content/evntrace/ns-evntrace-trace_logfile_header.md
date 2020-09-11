---
UID: NS:evntrace._TRACE_LOGFILE_HEADER
title: TRACE_LOGFILE_HEADER (evntrace.h)
description: The TRACE_LOGFILE_HEADER structure contains information about an event tracing session and its events.
helpviewer_keywords: ["*PTRACE_LOGFILE_HEADER","PTRACE_LOGFILE_HEADER","PTRACE_LOGFILE_HEADER structure pointer [ETW]","TRACE_LOGFILE_HEADER","TRACE_LOGFILE_HEADER structure [ETW]","_TRACE_LOGFILE_HEADER","_evt_trace_logfile_header","base.trace_logfile_header","etw.trace_logfile_header","evntrace/PTRACE_LOGFILE_HEADER","evntrace/TRACE_LOGFILE_HEADER"]
old-location: etw\trace_logfile_header.htm
tech.root: ETW
ms.assetid: 13fdabe6-c904-4546-b876-c145f6a6c345
ms.date: 12/05/2018
ms.keywords: '*PTRACE_LOGFILE_HEADER, PTRACE_LOGFILE_HEADER, PTRACE_LOGFILE_HEADER structure pointer [ETW], TRACE_LOGFILE_HEADER, TRACE_LOGFILE_HEADER structure [ETW], _TRACE_LOGFILE_HEADER, _evt_trace_logfile_header, base.trace_logfile_header, etw.trace_logfile_header, evntrace/PTRACE_LOGFILE_HEADER, evntrace/TRACE_LOGFILE_HEADER'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TRACE_LOGFILE_HEADER, *PTRACE_LOGFILE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRACE_LOGFILE_HEADER
 - evntrace/_TRACE_LOGFILE_HEADER
 - PTRACE_LOGFILE_HEADER
 - evntrace/PTRACE_LOGFILE_HEADER
 - TRACE_LOGFILE_HEADER
 - evntrace/TRACE_LOGFILE_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - TRACE_LOGFILE_HEADER
---

# TRACE_LOGFILE_HEADER structure


## -description

The 
TRACE_LOGFILE_HEADER structure contains information about an event tracing session and its events.

## -struct-fields

### -field BufferSize

Size of the event tracing session's buffers, in bytes.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Version

Version number of the operating system. This is a roll-up of the members of <b>VersionDetail</b>. Starting with the low-order bytes, the first two bytes contain <b>MajorVersion</b>, the next two bytes contain <b>MinorVersion</b>, the next two bytes contain <b>SubVersion</b>, and the last two   bytes contain <b>SubMinorVersion</b>.

### -field DUMMYUNIONNAME.VersionDetail

### -field DUMMYUNIONNAME.VersionDetail.MajorVersion

Major version number of the operating system.

### -field DUMMYUNIONNAME.VersionDetail.MinorVersion

Minor version number of the operating system.

### -field DUMMYUNIONNAME.VersionDetail.SubVersion

Reserved.

### -field DUMMYUNIONNAME.VersionDetail.SubMinorVersion

Reserved.

### -field ProviderVersion

Build number of the operating system.

### -field NumberOfProcessors

Number of processors on the system.

### -field EndTime

Time at which the event tracing session stopped, in 100-nanosecond intervals since midnight, January 1, 1601. This value may be 0 if you are consuming events in real time or from a log file to which the provide is still logging events.

### -field TimerResolution

Resolution of the hardware timer, in units of 100 nanoseconds. For usage, see the Remarks for <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a>.

### -field MaximumFileSize

Maximum size of the log file, in megabytes.

### -field LogFileMode

Current logging mode for the event tracing session. For a list of values, see 
<a href="https://docs.microsoft.com/windows/desktop/ETW/logging-mode-constants">Logging Mode Constants</a>.

### -field BuffersWritten

Total number of buffers written by the event tracing session.

### -field DUMMYUNIONNAME2

### -field DUMMYUNIONNAME2.LogInstanceGuid

Reserved.

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

### -field LoggerName

Do not use.

The name of the event tracing session is the first null-terminated string following this structure in memory.

### -field LogFileName

Do Not use.

The name of the event tracing log file is the second null-terminated string following this structure in memory. The first string is the name of the session.

### -field TimeZone

A 
<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a> structure that contains the time zone for the <b>BootTime</b>, <b>EndTime</b> and <b>StartTime</b> members.

### -field BootTime

Time at which the system was started, in 100-nanosecond intervals since midnight, January 1, 1601. <b>BootTime</b> is  supported only for traces written to the Global Logger session.

### -field PerfFreq

Frequency of the high-resolution performance counter, if one exists.

### -field StartTime

Time at which the event tracing session started, in 100-nanosecond intervals since midnight, January 1, 1601.

### -field ReservedFlags

Specifies the clock type. For details, see the <b>ClientContext</b> member of <a href="https://docs.microsoft.com/windows/desktop/ETW/wnode-header">WNODE_HEADER</a>.

### -field BuffersLost

Total number of buffers lost during the event tracing session.

## -remarks

Be sure to initialize the memory for this structure to zero before setting any members.

The first event from any log file contains the data defined in this structure. You can use this structure to access the  event data or you can use the <a href="https://docs.microsoft.com/windows/desktop/ETW/eventtrace-header">EventTrace_Header</a> MOF class to decode the event data. Using this structure to read the event data may return unexpected results if the consumer is on a different computer from the one that generated the log file or the log file was written in a WOW (32-bit) session on a 64-bit computer. This is because the <b>LoggerName</b> and <b>LogFileName</b> members are pointers and can vary in size depending on the <b>PointerSize</b> member.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a>



<a href="/windows/win32/api/winnt/ns-winnt-large_integer~r1">LARGE_INTEGER</a>



<a href="https://docs.microsoft.com/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information">TIME_ZONE_INFORMATION</a>

