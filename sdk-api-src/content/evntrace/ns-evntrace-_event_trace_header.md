---
UID: NS:evntrace._EVENT_TRACE_HEADER
title: "_EVENT_TRACE_HEADER"
author: windows-sdk-content
description: The EVENT_TRACE_HEADER structure is used to pass a WMI event to the WMI event logger.
old-location: kernel\event_trace_header.htm
tech.root: Kernel
ms.assetid: faddcf82-1025-458f-ab33-c96cd5699ca5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PEVENT_TRACE_HEADER, EVENT_TRACE_HEADER, EVENT_TRACE_HEADER structure [Kernel-Mode Driver Architecture], PEVENT_TRACE_HEADER, PEVENT_TRACE_HEADER structure pointer [Kernel-Mode Driver Architecture], _EVENT_TRACE_HEADER, evntrace/EVENT_TRACE_HEADER, evntrace/PEVENT_TRACE_HEADER, kernel.event_trace_header, kstruct_a_9a7cc863-6913-427c-8756-4c62c20f5b60.xml"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntrace.h
req.include-header: Wdm.h, Ntddk.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - EVENT_TRACE_HEADER
product: Windows
targetos: Windows
req.typenames: EVENT_TRACE_HEADER, *PEVENT_TRACE_HEADER
req.redist: 
---

# _EVENT_TRACE_HEADER structure


## -description


The <b>EVENT_TRACE_HEADER</b> structure is used to pass a WMI event to the WMI event logger. It is overlaid on the <a href="https://msdn.microsoft.com/a895f048-b111-4ccc-8466-fe9b169a2f95">WNODE_HEADER</a> portion of the <a href="https://msdn.microsoft.com/1805d174-ac10-4e76-9e3f-e9e156b769ec">WNODE_EVENT_ITEM</a> passed to <a href="https://msdn.microsoft.com/6b98861c-b108-4b07-b494-e3647d03de4c">IoWMIWriteEvent</a>. Information contained in the <b>EVENT_TRACE_HEADER</b> is written to the WMI log file.


## -struct-fields




### -field Size

Specifies the size, in bytes, of the buffer that is allocated to hold event tracing information. The value that is specified must include both the size of the <b>EVENT_TRACE_HEADER</b> structure and the size of any driver-specific data. (<b>EVENT_TRACE_HEADER</b> is overlaid on a <a href="https://msdn.microsoft.com/a895f048-b111-4ccc-8466-fe9b169a2f95">WNODE_HEADER</a> structure, but the <b>Size</b> member of <b>EVENT_TRACE_HEADER</b> and the <b>BufferSize</b> member of <b>WNODE_HEADER</b> do not specify the same size. Do not use the <b>BufferSize</b> member of <b>WNODE_HEADER</b> to set the <b>Size</b> member.) 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.FieldTypeFlags

Flags to indicate which fields in the <b>EVENT_TRACE_HEADER</b> structure are valid.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.HeaderType

Reserved for internal use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.MarkerFlags

Reserved for internal use.


### -field DUMMYUNIONNAME2

 


### -field DUMMYUNIONNAME2.Version

Drivers can use this member to store version information. This information is not interpreted by the event logger.


### -field DUMMYUNIONNAME2.Class

Event class information.


### -field DUMMYUNIONNAME2.Class.Type

Trace event type. This can be one of the predefined EVENT_TRACE_TYPE_<i>XXX</i> values contained in Evntrace.h or can be a driver-defined value. Callers are free to define private event types with values greater than the reserved values in Evntrace.h.


### -field DUMMYUNIONNAME2.Class.Level

Trace instrumentation level. A driver-defined value meant to represent the degree of detail of the trace instrumentation. Drivers are free to give this value meaning. This value should be 0 by default. More information about how consumers can request different levels of trace information will be provided in a future version of the documentation.


### -field DUMMYUNIONNAME2.Class.Version

Version of trace record. Version information that can be used by the driver to track different event formats.


### -field ThreadId

Thread identifier.


### -field ProcessId

Process identifier.


### -field TimeStamp

The time at which the driver event occurred. This time value is expressed in absolute system time format. Absolute system time is the number of 100-nanosecond intervals since the start of the year 1601 in the Gregorian calendar. If the WNODE_FLAG_USE_TIMESTAMP is set in <b>Flags,</b> the system logger will leave the value of <b>TimeStamp</b> unchanged. Otherwise, the system logger will set the value of <b>TimeStamp</b> at the time it receives the event. A driver can call <b>KeQuerySystemTime</b> to set the value of <b>TimeStamp</b>. 


### -field DUMMYUNIONNAME3

 


### -field DUMMYUNIONNAME3.Guid

The GUID that identifies the data block for the event. 


### -field DUMMYUNIONNAME3.GuidPtr

If the WNODE_FLAG_USE_GUID_PTR flag bit is set in <b>Flags</b>, <b>GuidPtr</b> points to the GUID that identifies the data block for the event.


### -field DUMMYUNIONNAME4

 


### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME.KernelTime

Reserved for internal use.


### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME.UserTime

Reserved for internal use.


### -field DUMMYUNIONNAME4.ProcessorTime

Reserved for internal use.


### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME2

 


### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME2.ClientContext

Reserved for internal use.


### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME2.Flags

Provides information about the contents of this structure. For information about <b>EVENT_TRACE_HEADER</b><b> Flags</b> values, see the <b>Flags</b> description in <a href="https://msdn.microsoft.com/a895f048-b111-4ccc-8466-fe9b169a2f95">WNODE_HEADER</a>.


## -remarks



A driver that supports trace events will use this structure to report events to the WMI event logger. Trace events should not be reported until the driver receives a request to enable events and the control GUID is one the driver supports. The driver should initialize an <b>EVENT_TRACE_HEADER</b> structure, fill in any user-defined event data at the end, and pass a pointer to the <b>EVENT_TRACE_HEADER</b> to <b>IoWMIWriteEvent</b>. The driver should continue reporting trace events until it receives a request to disable the control GUID for the trace events.

If the driver does not specify the WNODE_FLAG_USE_MOF_PTR flag in the <b>Flags</b> member of <b>EVENT_TRACE_HEADER</b>, the <b>EVENT_TRACE_HEADER</b> structure is followed in memory by event-specific data. In this case, the <b>Size</b> member must be <b>sizeof</b>(<b>EVENT_TRACE_HEADER</b>) plus the size of the event-specific data. 

If the driver does specify the WNODE_FLAG_USE_MOF_PTR flag, the <b>EVENT_TRACE_HEADER</b> structure is followed in memory by an array of <b>MOF_FIELD</b> structures (which are defined in Evntrace.h) that contain pointers to the data and sizes rather than the event tracing data itself. In this case, the <b>Size</b> member must be <b>sizeof</b>(<b>EVENT_TRACE_HEADER</b>) plus the size of the array of <b>MOF_FIELD</b> structures.




## -see-also




<a href="https://msdn.microsoft.com/6b98861c-b108-4b07-b494-e3647d03de4c">IoWMIWriteEvent</a>



<a href="https://msdn.microsoft.com/1805d174-ac10-4e76-9e3f-e9e156b769ec">WNODE_EVENT_ITEM</a>



<a href="https://msdn.microsoft.com/a895f048-b111-4ccc-8466-fe9b169a2f95">WNODE_HEADER</a>
 

 

