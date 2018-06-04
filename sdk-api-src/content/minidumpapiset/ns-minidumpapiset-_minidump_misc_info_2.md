---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _MINIDUMP_MISC_INFO_2 structure


## -description


Represents information in the miscellaneous information stream.


## -struct-fields




### -field SizeOfInfo

The size of the structure, in bytes.


### -field Flags1

The flags that indicate the valid members of this structure. This member can be one or more of the 
      following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_MISC1_PROCESS_ID"></a><a id="minidump_misc1_process_id"></a><dl>
<dt><b>MINIDUMP_MISC1_PROCESS_ID</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
<b>ProcessId</b> is used.

</td>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_MISC1_PROCESS_TIMES"></a><a id="minidump_misc1_process_times"></a><dl>
<dt><b>MINIDUMP_MISC1_PROCESS_TIMES</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
<b>ProcessCreateTime</b>, <b>ProcessKernelTime</b>, and 
        <b>ProcessUserTime</b> are used.

</td>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_MISC1_PROCESSOR_POWER_INFO"></a><a id="minidump_misc1_processor_power_info"></a><dl>
<dt><b>MINIDUMP_MISC1_PROCESSOR_POWER_INFO</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
<b>ProcessorMaxMhz</b>, <b>ProcessorCurrentMhz</b>, 
        <b>ProcessorMhzLimit</b>, <b>ProcessorMaxIdleState</b>, and 
        <b>ProcessorCurrentIdleState</b> are used.

</td>
</tr>
</table>
 


### -field ProcessId

The identifier of the process. If <b>Flags1</b> does not specify 
      <b>MINIDUMP_MISC1_PROCESS_ID</b>, this member is unused.


### -field ProcessCreateTime

The creation time of the process, in <b>time_t</b> format. If 
      <b>Flags1</b> does not specify <b>MINIDUMP_MISC1_PROCESS_TIMES</b>, this 
      member is unused.


### -field ProcessUserTime

The time the process has executed in user mode, in seconds. The time that each of the threads of the 
      process has executed in user mode is determined, then all these times are summed to obtain this value. If 
      <b>Flags1</b> does not specify <b>MINIDUMP_MISC1_PROCESS_TIMES</b>, this 
      member is unused.


### -field ProcessKernelTime

The time the process has executed in kernel mode, in seconds. The time that each of the threads of the 
      process has executed in kernel mode is determined, then all these times are summed to obtain this value. If 
      <b>Flags1</b> does not specify <b>MINIDUMP_MISC1_PROCESS_TIMES</b>, this 
      member is unused.


### -field ProcessorMaxMhz

The maximum specified clock frequency of the system processor, in MHz. If <b>Flags1</b> 
      does not specify <b>MINIDUMP_MISC1_PROCESSOR_POWER_INFO</b>, this member is unused.


### -field ProcessorCurrentMhz

The processor clock frequency, in MHz. This number is the maximum specified processor clock frequency 
      multiplied by the current processor throttle. If <b>Flags1</b> does not specify 
      <b>MINIDUMP_MISC1_PROCESSOR_POWER_INFO</b>, this member is unused.


### -field ProcessorMhzLimit

The limit on the processor clock frequency, in MHz. This number is the maximum specified processor clock 
      frequency multiplied by the current processor thermal throttle limit. If <b>Flags1</b> does 
      not specify <b>MINIDUMP_MISC1_PROCESSOR_POWER_INFO</b>, this member is unused.


### -field ProcessorMaxIdleState

The maximum idle state of the processor. If <b>Flags1</b> does not specify 
      <b>MINIDUMP_MISC1_PROCESSOR_POWER_INFO</b>, this member is unused.


### -field ProcessorCurrentIdleState

The current idle state of the processor. If <b>Flags1</b> does not specify 
      <b>MINIDUMP_MISC1_PROCESSOR_POWER_INFO</b>, this member is unused.


## -see-also




<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>
 

 

