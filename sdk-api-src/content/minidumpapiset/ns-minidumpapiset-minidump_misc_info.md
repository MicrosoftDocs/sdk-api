---
UID: NS:minidumpapiset._MINIDUMP_MISC_INFO
title: MINIDUMP_MISC_INFO (minidumpapiset.h)
description: Contains a variety of information.
helpviewer_keywords: ["*PMINIDUMP_MISC_INFO","MINIDUMP_MISC1_PROCESS_ID","MINIDUMP_MISC1_PROCESS_TIMES","MINIDUMP_MISC_INFO","MINIDUMP_MISC_INFO structure","PMINIDUMP_MISC_INFO","PMINIDUMP_MISC_INFO structure pointer","_MINIDUMP_MISC_INFO","_win32_minidump_misc_info_str","base.minidump_misc_info_str","minidumpapiset/MINIDUMP_MISC_INFO","minidumpapiset/PMINIDUMP_MISC_INFO"]
old-location: base\minidump_misc_info_str.htm
tech.root: Debug
ms.assetid: c80bb631-b26b-40d4-ae35-1cf38ce45d51
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_MISC_INFO, MINIDUMP_MISC1_PROCESS_ID, MINIDUMP_MISC1_PROCESS_TIMES, MINIDUMP_MISC_INFO, MINIDUMP_MISC_INFO structure, PMINIDUMP_MISC_INFO, PMINIDUMP_MISC_INFO structure pointer, _MINIDUMP_MISC_INFO, _win32_minidump_misc_info_str, base.minidump_misc_info_str, minidumpapiset/MINIDUMP_MISC_INFO, minidumpapiset/PMINIDUMP_MISC_INFO'
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
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
req.typenames: MINIDUMP_MISC_INFO, *PMINIDUMP_MISC_INFO
req.redist: DbgHelp.dll 6.0 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_MISC_INFO
 - minidumpapiset/_MINIDUMP_MISC_INFO
 - PMINIDUMP_MISC_INFO
 - minidumpapiset/PMINIDUMP_MISC_INFO
 - MINIDUMP_MISC_INFO
 - minidumpapiset/MINIDUMP_MISC_INFO
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
 - MINIDUMP_MISC_INFO
---

# MINIDUMP_MISC_INFO structure


## -description

Contains a variety of information.

## -struct-fields

### -field SizeOfInfo

The size of the structure, in bytes.

### -field Flags1

The flags that indicate the valid members of this structure. This member can be one or more of the following values. 



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
<b>ProcessCreateTime</b>, <b>ProcessKernelTime</b>, and <b>ProcessUserTime</b> are used.

</td>
</tr>
</table>

### -field ProcessId

The identifier of the process. If <b>Flags1</b> does not specify MINIDUMP_MISC1_PROCESS_ID, this member is unused.

### -field ProcessCreateTime

The creation time of the process, in <b>time_t</b> format. If <b>Flags1</b> does not specify MINIDUMP_MISC1_PROCESS_TIMES, this member is unused.

### -field ProcessUserTime

The time the process has executed in user mode, in seconds. The time that each of the threads of the process has executed in user mode is determined, then all these times are summed to obtain this value. If <b>Flags1</b> does not specify MINIDUMP_MISC1_PROCESS_TIMES, this member is unused.

### -field ProcessKernelTime

The time the process has executed in kernel mode, in seconds. The time that each of the threads of the process has executed in kernel mode is determined, then all these times are summed to obtain this value. If <b>Flags1</b> does not specify MINIDUMP_MISC1_PROCESS_TIMES, this member is unused.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>