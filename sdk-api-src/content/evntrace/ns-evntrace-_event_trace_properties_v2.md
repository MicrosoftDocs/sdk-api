---
UID: NS:evntrace._EVENT_TRACE_PROPERTIES_V2
title: "_EVENT_TRACE_PROPERTIES_V2"
author: windows-driver-content
description: The EVENT_TRACE_PROPERTIES_V2 structure contains information about an event tracing session.
old-location: etw\event_trace_properties_v2.htm
old-project: ETW
ms.assetid: 2EEDB53B-75BC-48AC-A70D-9AEAED526C40
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PEVENT_TRACE_PROPERTIES_V2, EVENT_TRACE_FLAG_ALPC, EVENT_TRACE_FLAG_CSWITCH, EVENT_TRACE_FLAG_DBGPRINT, EVENT_TRACE_FLAG_DISK_FILE_IO, EVENT_TRACE_FLAG_DISK_IO, EVENT_TRACE_FLAG_DISK_IO_INIT, EVENT_TRACE_FLAG_DISPATCHER, EVENT_TRACE_FLAG_DPC, EVENT_TRACE_FLAG_DRIVER, EVENT_TRACE_FLAG_FILE_IO, EVENT_TRACE_FLAG_FILE_IO_INIT, EVENT_TRACE_FLAG_IMAGE_LOAD, EVENT_TRACE_FLAG_INTERRUPT, EVENT_TRACE_FLAG_JOB, EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS, EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS, EVENT_TRACE_FLAG_NETWORK_TCPIP, EVENT_TRACE_FLAG_NO_SYSCONFIG, EVENT_TRACE_FLAG_PROCESS, EVENT_TRACE_FLAG_PROCESS_COUNTERS, EVENT_TRACE_FLAG_PROFILE, EVENT_TRACE_FLAG_REGISTRY, EVENT_TRACE_FLAG_SPLIT_IO, EVENT_TRACE_FLAG_SYSTEMCALL, EVENT_TRACE_FLAG_THREAD, EVENT_TRACE_FLAG_VAMAP, EVENT_TRACE_FLAG_VIRTUAL_ALLOC, EVENT_TRACE_PROPERTIES_V2, EVENT_TRACE_PROPERTIES_V2 structure [ETW], PEVENT_TRACE_PROPERTIES_V2, PEVENT_TRACE_PROPERTIES_V2 structure pointer [ETW], _EVENT_TRACE_PROPERTIES_V2, etw.event_trace_properties_v2, evntrace/EVENT_TRACE_PROPERTIES_V2, evntrace/PEVENT_TRACE_PROPERTIES_V2"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EVENT_TRACE_PROPERTIES_V2, *PEVENT_TRACE_PROPERTIES_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Evntrace.h
api_name:
-	EVENT_TRACE_PROPERTIES_V2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _EVENT_TRACE_PROPERTIES_V2 structure


## -description


The 
<b>EVENT_TRACE_PROPERTIES_V2</b> structure contains information about an event tracing session. You use this structure when you define a session, change the properties of a session, or query for the properties of a session. This is  extended from the <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME2

 


### -field DUMMYUNIONNAME2.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME2.DUMMYSTRUCTNAME.VersionNumber

The version of the structure. This should be set to "2" for this version.


### -field DUMMYUNIONNAME3

 


### -field DUMMYUNIONNAME3.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME3.DUMMYSTRUCTNAME.Wow

 


### -field Wnode

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff566375">WNODE_HEADER</a> structure. You must specify the <b>BufferSize</b>, <b>Flags</b>, and <b>Guid</b> members, and optionally the  <b>ClientContext</b> member.


### -field BufferSize

Amount of memory allocated for each event tracing session buffer, in kilobytes. The maximum buffer size is 1 MB. ETW uses the size of physical memory to calculate this value. For more information, see Remarks.

If an application expects a relatively low event rate, the buffer size should be set to the memory page size. If the event rate is expected to be relatively high, the application should specify a larger buffer size, and should increase the maximum number of buffers. 

The buffer size affects the rate at which buffers fill and must be flushed. Although a small buffer size requires less memory, it increases the rate at which buffers must be flushed. 


### -field MinimumBuffers

Minimum number of buffers allocated for the event tracing session's buffer pool. The minimum number of buffers that you can specify is two buffers per processor. For example, on a single processor computer, the minimum number of buffers is two. Note that if you use the EVENT_TRACE_NO_PER_PROCESSOR_BUFFERING logging mode, the number of processors is assumed to be 1.


### -field MaximumBuffers

Maximum number of buffers allocated for the event tracing session's buffer pool. Typically, this value is the minimum number of buffers plus twenty. ETW uses the buffer size and the size of physical memory to calculate this value. This value must be greater than or equal to the value for <b>MinimumBuffers</b>. Note that  you do not need to set this value if <b>LogFileMode</b> contains <b>EVENT_TRACE_BUFFERING_MODE</b>; instead, the total memory buffer size is instead the product of  <b>MinimumBuffers</b> and <b>BufferSize</b>.


### -field MaximumFileSize

Maximum size of the file used to log events, in megabytes. Typically, you use this member to limit the size of a circular log file when you set <b>LogFileMode</b> to <b>EVENT_TRACE_FILE_MODE_CIRCULAR</b>. This member must be specified if <b>LogFileMode</b> contains <b>EVENT_TRACE_FILE_MODE_PREALLOCATE</b>, <b>EVENT_TRACE_FILE_MODE_CIRCULAR</b> or <b>EVENT_TRACE_FILE_MODE_NEWFILE</b>

If you are using the system drive (the drive that contains the operating system) for logging, ETW checks for an additional 200MB of disk space, regardless of whether you are using the maximum file size parameter. Therefore, if you specify 100MB as the maximum file size for the trace file in the system drive, you need to have 300MB of free space on the drive. 


### -field LogFileMode

Logging modes for the event tracing session. You use this member to specify that you want events written to a log file, a real-time consumer, or both. You can also use this member to specify that the session is a private logger session. You can specify one or more modes. For a list of possible modes, see 
<a href="https://msdn.microsoft.com/d12aaecb-776a-4476-9ba4-16af30fde9c2">Logging Mode Constants</a>.

Do not specify real-time logging unless there are real-time consumers ready to consume the events. If there are no real-time consumers, ETW writes the events to a playback file. However, the size of the playback file is limited. If the limit is reached, no new events are logged (to the log file or playback file) and the logging functions fail with STATUS_LOG_FILE_FULL.<b>Prior to Windows Vista:  </b>If there was no real-time consumer, the events were discarded and logging continues.</p>If a consumer begins processing real-time events, the events in the playback file are consumed first. After all events in the playback file are consumed, the session will begin logging new events.


### -field FlushTimer

How often, in seconds, the trace buffers are forcibly flushed. The minimum flush time is 1 second.
This forced flush is in addition to the automatic flush that occurs whenever a buffer is full and when the trace session stops.



If zero, ETW flushes buffers as soon as they become full. If nonzero, ETW flushes all buffers that contain events based on the timer value. Typically, you want to flush buffers only when they become full. Forcing the buffers to flush (either by setting this member to a nonzero value or by calling <a href="https://msdn.microsoft.com/bc7d0dac-93d9-4614-9cb6-fee99765eb39">FlushTrace</a>) can increase the file size of the log file with unfilled buffer space. 

If the consumer is consuming events in real time, you may want to set this member to a nonzero value if the event rate is low to force events to be delivered before the buffer is full.

For the case of a realtime logger,  a value of zero (the default value) means that the flush time will be set to 1 second. A realtime logger is when <b>LogFileMode</b> is set to <b>EVENT_TRACE_REAL_TIME_MODE</b>.


### -field EnableFlags

A system logger must set <b>EnableFlags</b> to indicate which SystemTraceProvider events should be included in the trace. This is also used for NT Kernel Logger sessions. 


This member can contain one or more of the following values.
					In addition to the events you specify, the kernel logger also logs hardware configuration events on Windows XP or system configuration events on Windows Server 2003.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_ALPC"></a><a id="event_trace_flag_alpc"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_ALPC</b></b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Enables the <a href="https://msdn.microsoft.com/5380fada-50e7-4eb2-8549-6d738a56d2cd">ALPC</a> event types.

This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_CSWITCH"></a><a id="event_trace_flag_cswitch"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_CSWITCH</b></b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/0bf14240-3b8d-4eb5-b751-7b2e23b55762">Thread</a> event type:<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938520">CSwitch</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_DBGPRINT"></a><a id="event_trace_flag_dbgprint"></a><dl>
<dt><b>EVENT_TRACE_FLAG_DBGPRINT</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
Enables the <b>DbgPrint</b> and <b>DbgPrintEx</b> calls to be converted to ETW events.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_DISK_FILE_IO"></a><a id="event_trace_flag_disk_file_io"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_DISK_FILE_IO</b></b></dt>
<dt>0x00000200</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/8e006a63-a061-4b62-8f90-b8c8823bb047">FileIo</a>  event type (you must also enable EVENT_TRACE_FLAG_DISK_IO):

<ul>
<li>
<a href="https://msdn.microsoft.com/ed72daa3-06c0-46f1-bb9d-c0b343228f28">FileIo_Name</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_DISK_IO"></a><a id="event_trace_flag_disk_io"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_DISK_IO</b></b></dt>
<dt>0x00000100</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/library/windows/hardware/dn938535">DiskIo</a>  event types:

<ul>
<li>
<a href="https://msdn.microsoft.com/fe7d4efa-3d39-4438-a1a6-af3f65ea3deb">DiskIo_TypeGroup1</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7f0c9bd4-e4d3-49c1-ae72-f6bdf938099f">DiskIo_TypeGroup3</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_DISK_IO_INIT"></a><a id="event_trace_flag_disk_io_init"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_DISK_IO_INIT</b></b></dt>
<dt>0x00000400</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/library/windows/hardware/dn938535">DiskIo</a>  event type:<ul>
<li>
<a href="https://msdn.microsoft.com/96543ef9-cc2b-4d9a-86a8-f2458439e4d8">DiskIo_TypeGroup2</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_DISPATCHER"></a><a id="event_trace_flag_dispatcher"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_DISPATCHER</b></b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/0bf14240-3b8d-4eb5-b751-7b2e23b55762">Thread</a>  event type:<ul>
<li>
<a href="https://msdn.microsoft.com/861ab070-5536-4897-b523-9b09a7d59b3e">ReadyThread</a>
</li>
</ul>


This value is supported on Windows 7, Windows Server 2008 R2, and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_DPC"></a><a id="event_trace_flag_dpc"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_DPC</b></b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/2606fea3-0651-4f7f-83a6-63021039eb95">PerfInfo</a> event type:<ul>
<li>
<a href="https://msdn.microsoft.com/46010179-7f0a-47dd-95fd-04d30fc597ba">DPC</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_DRIVER"></a><a id="event_trace_flag_driver"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_DRIVER</b></b></dt>
<dt>0x00800000</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/library/windows/hardware/dn938535">DiskIo</a> event types:<ul>
<li>
<a href="https://msdn.microsoft.com/c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7">DriverCompleteRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/04505f8c-a11e-4bf7-91c0-fca1b5846d80">DriverCompleteRequestReturn</a>
</li>
<li>
<a href="https://msdn.microsoft.com/deb4f0b2-d73f-4ccf-b39b-6e92b32489fb">DriverCompletionRoutine</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8c913145-ac50-4d40-8519-5fed79d977ba">DriverMajorFunctionCall</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b3358935-d6fb-49eb-bdf7-4366b4fd14c5">DriverMajorFunctionReturn</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_FILE_IO"></a><a id="event_trace_flag_file_io"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_FILE_IO</b></b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/8e006a63-a061-4b62-8f90-b8c8823bb047">FileIo</a>  event types:<ul>
<li>
<a href="https://msdn.microsoft.com/3925d5bf-f412-4248-a61f-e667efa9debd">FileIo_OpEnd</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_FILE_IO_INIT"></a><a id="event_trace_flag_file_io_init"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_FILE_IO_INIT</b></b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/8e006a63-a061-4b62-8f90-b8c8823bb047">FileIo</a> event type:<ul>
<li>
<a href="https://msdn.microsoft.com/83465072-3dae-4a39-8a36-1512025b79df">FileIo_Create</a>
</li>
<li>
<a href="https://msdn.microsoft.com/08458385-6066-4523-a053-aceb5e5d6f10">FileIo_DirEnum</a>
</li>
<li>
<a href="https://msdn.microsoft.com/41ae1f8a-a90f-43d0-a848-a2c095f046d4">FileIo_Info</a>
</li>
<li>
<a href="https://msdn.microsoft.com/88c380fb-e043-40ab-aa74-550bce43c52b">FileIo_ReadWrite</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b6374e0-b39a-4d5a-acbd-25b410f1ba52">FileIo_SimpleOp</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_IMAGE_LOAD"></a><a id="event_trace_flag_image_load"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_IMAGE_LOAD</b></b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/a719a34c-7e32-4758-9031-6ca2b2873e3e">Image</a>  event type:

<ul>
<li>
<a href="https://msdn.microsoft.com/70ec0542-16d3-4186-a346-7f3c44dedf67">Image_Load</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_INTERRUPT"></a><a id="event_trace_flag_interrupt"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_INTERRUPT</b></b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/2606fea3-0651-4f7f-83a6-63021039eb95">PerfInfo</a> event type:<ul>
<li>
<a href="https://msdn.microsoft.com/2c7ccace-3384-43f4-905e-e7eeeee6f87b">ISR</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_JOB"></a><a id="event_trace_flag_job"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_JOB</b></b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
This value is supported on Windows 10

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS"></a><a id="event_trace_flag_memory_hard_faults"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_MEMORY_HARD_FAULTS</b></b></dt>
<dt>0x00002000</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/cc349e75-fe81-427e-8cf9-15c76e8e4dad">PageFault_V2</a>  event type:

<ul>
<li>
<a href="https://msdn.microsoft.com/9837cc45-6485-46c3-a5d9-0d33e443cd32">PageFault_HardFault</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS"></a><a id="event_trace_flag_memory_page_faults"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_MEMORY_PAGE_FAULTS</b></b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/cc349e75-fe81-427e-8cf9-15c76e8e4dad">PageFault_V2</a>  event type:

<ul>
<li>
<a href="https://msdn.microsoft.com/59cb1091-af21-4fe6-87b8-17a262cc4467">PageFault_TypeGroup1</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_NETWORK_TCPIP"></a><a id="event_trace_flag_network_tcpip"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_NETWORK_TCPIP</b></b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Enables the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966084">TcpIp</a> and <a href="https://msdn.microsoft.com/0fbecad2-0221-408e-9f43-859547efa803">UdpIp</a> event types.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_NO_SYSCONFIG"></a><a id="event_trace_flag_no_sysconfig"></a><dl>
<dt><b>EVENT_TRACE_FLAG_NO_SYSCONFIG</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Do not do a system configuration rundown.

This value is supported on Windows 8,  Windows Server 2012, and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_PROCESS"></a><a id="event_trace_flag_process"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_PROCESS</b></b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">Process</a> event type:

<ul>
<li>
<a href="https://msdn.microsoft.com/4f06e1af-3f9a-4346-aa50-50f3ee82cd98">Process_TypeGroup1</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_PROCESS_COUNTERS"></a><a id="event_trace_flag_process_counters"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_PROCESS_COUNTERS</b></b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/75596278-43cc-4040-a43d-6958d0935b68">Process_V2</a> event type:<ul>
<li>
<a href="https://msdn.microsoft.com/7f1fa1c4-a2ff-4a1c-ac9d-e922a13c99a1">Process_V2_TypeGroup2</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_PROFILE"></a><a id="event_trace_flag_profile"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_PROFILE</b></b></dt>
<dt>0x01000000</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/2606fea3-0651-4f7f-83a6-63021039eb95">PerfInfo</a> event type:<ul>
<li>
<a href="https://msdn.microsoft.com/75ea1e5e-2554-40bb-aa9d-c6d4942c5801">SampledProfile</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_REGISTRY"></a><a id="event_trace_flag_registry"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_REGISTRY</b></b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
Enables the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926940">Registry</a> event types.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_SPLIT_IO"></a><a id="event_trace_flag_split_io"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_SPLIT_IO</b></b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
Enables the <a href="https://msdn.microsoft.com/d65c5180-6f1a-45cc-bca8-eac13857d383">SplitIo</a> event types.

This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_SYSTEMCALL"></a><a id="event_trace_flag_systemcall"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_SYSTEMCALL</b></b></dt>
<dt>0x00000080</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/2606fea3-0651-4f7f-83a6-63021039eb95">PerfInfo</a> event type:<ul>
<li>
<a href="https://msdn.microsoft.com/1ab32977-3f59-4816-b311-67142475dff2">SysCallEnter</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bb9a2770-f37b-4055-8811-59ba117adf82">SysCallExit</a>
</li>
</ul>


This value is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_THREAD"></a><a id="event_trace_flag_thread"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_THREAD</b></b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/0bf14240-3b8d-4eb5-b751-7b2e23b55762">Thread</a> event type:

<ul>
<li>
<a href="https://msdn.microsoft.com/d9e3e33a-0e59-4753-a8d8-5320cbae9d95">Thread_TypeGroup1</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_VAMAP"></a><a id="event_trace_flag_vamap"></a><dl>
<dt><b>EVENT_TRACE_FLAG_VAMAP</b></dt>
<dt>0x00008000</dt>
</dl>
</td>
<td width="60%">
Enables the map and unmap (excluding image files) event type.

This value is supported on Windows 8,  Windows Server 2012, and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_FLAG_VIRTUAL_ALLOC"></a><a id="event_trace_flag_virtual_alloc"></a><dl>
<dt><b><b>EVENT_TRACE_FLAG_VIRTUAL_ALLOC</b></b></dt>
<dt>0x00004000</dt>
</dl>
</td>
<td width="60%">
Enables the following <a href="https://msdn.microsoft.com/cc349e75-fe81-427e-8cf9-15c76e8e4dad">PageFault_V2</a>  event type:<ul>
<li>
<a href="https://msdn.microsoft.com/037d33e0-da94-4834-bc02-814c1cae1d8d">PageFault_VirtualAlloc</a>
</li>
</ul>


This value is supported on Windows 7,  Windows Server 2008 R2, and later.

</td>
</tr>
</table>
 


### -field NumberOfBuffers

On output, the number of buffers allocated for the event tracing session's buffer pool.


### -field FreeBuffers

On output, the number of buffers that are allocated but unused in the event tracing session's buffer pool.


### -field EventsLost

On output, the number of events that were not recorded.


### -field BuffersWritten

On output, the number of buffers written.


### -field LogBuffersLost

On output, the number of buffers that could not be written to the log file.


### -field RealTimeBuffersLost

On output, the number of buffers that could not be delivered in real-time to the consumer.


### -field LoggerThreadId

On output, the thread identifier for the event tracing session.


### -field LogFileNameOffset

Offset from the start of the structure's allocated memory to beginning of the null-terminated string that contains the log file name. 

The file name should use the .etl extension. All folders in the path must exist. The path can be relative, absolute, local, or remote. The path cannot contain environment variables (they are not expanded). The user must have permission to write to the folder.

The log file name is limited to 1,024 characters. If you set <b>LogFileMode</b> to  <b>EVENT_TRACE_PRIVATE_LOGGER_MODE</b> or <b>EVENT_TRACE_FILE_MODE_NEWFILE</b>, be sure to allocate enough memory to include the process identifier that is appended to the file name for private loggers sessions, and the sequential number that is added to log files created using the new file log mode. 
						
					

If you do not want to log events to a log file (for example, you specify <b>EVENT_TRACE_REAL_TIME_MODE</b> only), set <i>LogFileNameOffset</i> to 0. If you specify only real-time logging and also provide an offset with a valid log file name, ETW will use the log file name to create a sequential log file and log events to the log file. ETW also creates the sequential log file if <b>LogFileMode</b> is 0 and you provide an offset with a valid log file name.

If you want to log events to a log file, you must allocate enough memory for this structure to include the log file name and session name following the structure. The log file name must follow the session name in memory.

Trace files are created using the default security descriptor, meaning that the log file will have the same ACL as the parent directory. If you want access to the files restricted, create a parent directory with the appropriate ACLs.


### -field LoggerNameOffset

Offset from the start of the structure's allocated memory to beginning of the null-terminated string that contains the session name. 

The session name is limited to 1,024 characters. The session name is case-insensitive and must be unique.

<b>Windows 2000:  </b>Session names are case-sensitive. As a result, duplicate session names are allowed. However, to reduce confusion, you should make sure your session names are unique.

When you allocate the memory for this structure, you must allocate enough memory to include the session name and log file name following the structure. The session name must come before the log file name in memory. You must copy the log file name to the offset but you do not copy the session name to the offset—the <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> function copies the name for you.


### -field FilterDescCount

The number of filters that the <b>FilterDesc</b> points to. The only time this should not be zero is for system wide Private Loggers.


### -field FilterDesc

Supported <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> filter types for system wide private loggers: <b>EVENT_FILTER_TYPE_EXECUTABLE_NAME</b> and <b>EVENT_FILTER_TYPE_PID</b>

A pointer to an array of <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structures that points to the filter data. The number of elements in the array is specified in the <b>FilterDescCount</b> member. There can only be one filter for a specific filter type as specified by the <b>Type</b> member of the <b>EVENT_FILTER_DESCRIPTOR</b> structure. 

This is only applicable to Private Loggers. The only time this should not be null is when it is used for system wide Private Loggers.


#### - AgeLimit

 Not used.

<b>Windows 2000:  </b>Time delay before unused buffers are freed, in minutes. The default is 15 minutes.


## -remarks



This structure behaves similarly to <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> with a few exceptions.

The beginning of the structure is defined exactly as <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> to allow this new structure to be compatible with systems running versions of Windows before Windows 10, version 1703 and will be treated as <b>EVENT_TRACE_PROPERTIES</b>.

When using this structure, be sure to include WNODE_FLAG_VERSIONED_PROPERTIES in Wnode.Flags to indicate that this is the version two structure.

Note that the filters  passed into <a href="https://msdn.microsoft.com/c39f669c-ff40-40ed-ba47-798474ec2de4">ControlTrace</a>, <a href="https://msdn.microsoft.com/8ad0f4f6-902c-490e-b26e-7499dd99fc95">QueryTrace</a>, <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>, and <a href="https://msdn.microsoft.com/604274a1-c4ed-4746-b69a-e18969f969db">StopTrace</a> by this structure are the same format as filters consumed by the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function.




## -see-also




<a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566375">WNODE_HEADER</a>
 

 

