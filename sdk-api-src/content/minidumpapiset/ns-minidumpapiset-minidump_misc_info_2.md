---
UID: NS:minidumpapiset._MINIDUMP_MISC_INFO_2
title: MINIDUMP_MISC_INFO_2 (minidumpapiset.h)
description: Represents information in the miscellaneous information stream.
helpviewer_keywords: ["*PMINIDUMP_MISC_INFO_2","MINIDUMP_MISC1_PROCESSOR_POWER_INFO","MINIDUMP_MISC1_PROCESS_ID","MINIDUMP_MISC1_PROCESS_TIMES","MINIDUMP_MISC_INFO_2","MINIDUMP_MISC_INFO_2 structure","PMINIDUMP_MISC_INFO_2","PMINIDUMP_MISC_INFO_2 structure pointer","_MINIDUMP_MISC_INFO_2","base.minidump_misc_info_2","minidumpapiset/MINIDUMP_MISC_INFO_2","minidumpapiset/PMINIDUMP_MISC_INFO_2"]
old-location: base\minidump_misc_info_2.htm
tech.root: Debug
ms.assetid: 34f46a51-9e41-4550-a080-1c7c7a603b54
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_MISC_INFO_2, MINIDUMP_MISC1_PROCESSOR_POWER_INFO, MINIDUMP_MISC1_PROCESS_ID, MINIDUMP_MISC1_PROCESS_TIMES, MINIDUMP_MISC_INFO_2, MINIDUMP_MISC_INFO_2 structure, PMINIDUMP_MISC_INFO_2, PMINIDUMP_MISC_INFO_2 structure pointer, _MINIDUMP_MISC_INFO_2, base.minidump_misc_info_2, minidumpapiset/MINIDUMP_MISC_INFO_2, minidumpapiset/PMINIDUMP_MISC_INFO_2'
req.header: minidumpapiset.h
req.include-header: Dbghelp.h
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
targetos: Windows
req.typenames: MINIDUMP_MISC_INFO_2, *PMINIDUMP_MISC_INFO_2
req.redist: DbgHelp.dll 6.5 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_MISC_INFO_2
 - minidumpapiset/_MINIDUMP_MISC_INFO_2
 - PMINIDUMP_MISC_INFO_2
 - minidumpapiset/PMINIDUMP_MISC_INFO_2
 - MINIDUMP_MISC_INFO_2
 - minidumpapiset/MINIDUMP_MISC_INFO_2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_MISC_INFO_2
---

# MINIDUMP_MISC_INFO_2 structure


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

<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>