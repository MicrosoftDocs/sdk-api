---
UID: NS:minidumpapiset._MINIDUMP_THREAD_INFO
title: MINIDUMP_THREAD_INFO (minidumpapiset.h)
description: Contains thread state information.
helpviewer_keywords: ["*PMINIDUMP_THREAD_INFO","MINIDUMP_THREAD_INFO","MINIDUMP_THREAD_INFO structure","MINIDUMP_THREAD_INFO_ERROR_THREAD","MINIDUMP_THREAD_INFO_EXITED_THREAD","MINIDUMP_THREAD_INFO_INVALID_CONTEXT","MINIDUMP_THREAD_INFO_INVALID_INFO","MINIDUMP_THREAD_INFO_INVALID_TEB","MINIDUMP_THREAD_INFO_WRITING_THREAD","PMINIDUMP_THREAD_INFO","PMINIDUMP_THREAD_INFO structure pointer","_MINIDUMP_THREAD_INFO","base.minidump_thread_info_str","minidumpapiset/MINIDUMP_THREAD_INFO","minidumpapiset/PMINIDUMP_THREAD_INFO"]
old-location: base\minidump_thread_info_str.htm
tech.root: Debug
ms.assetid: 855bbccb-a7c8-4744-b314-8692f785b1c0
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_THREAD_INFO, MINIDUMP_THREAD_INFO, MINIDUMP_THREAD_INFO structure, MINIDUMP_THREAD_INFO_ERROR_THREAD, MINIDUMP_THREAD_INFO_EXITED_THREAD, MINIDUMP_THREAD_INFO_INVALID_CONTEXT, MINIDUMP_THREAD_INFO_INVALID_INFO, MINIDUMP_THREAD_INFO_INVALID_TEB, MINIDUMP_THREAD_INFO_WRITING_THREAD, PMINIDUMP_THREAD_INFO, PMINIDUMP_THREAD_INFO structure pointer, _MINIDUMP_THREAD_INFO, base.minidump_thread_info_str, minidumpapiset/MINIDUMP_THREAD_INFO, minidumpapiset/PMINIDUMP_THREAD_INFO'
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
req.typenames: MINIDUMP_THREAD_INFO, *PMINIDUMP_THREAD_INFO
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_THREAD_INFO
 - minidumpapiset/_MINIDUMP_THREAD_INFO
 - PMINIDUMP_THREAD_INFO
 - minidumpapiset/PMINIDUMP_THREAD_INFO
 - MINIDUMP_THREAD_INFO
 - minidumpapiset/MINIDUMP_THREAD_INFO
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
 - MINIDUMP_THREAD_INFO
---

# MINIDUMP_THREAD_INFO structure


## -description

Contains thread state information.

## -struct-fields

### -field ThreadId

The identifier of the thread.

### -field DumpFlags

The flags that indicate the thread state. This member can be 0 or one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_THREAD_INFO_ERROR_THREAD"></a><a id="minidump_thread_info_error_thread"></a><dl>
<dt><b>MINIDUMP_THREAD_INFO_ERROR_THREAD</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
A placeholder thread due to an error accessing the thread. No thread information exists beyond the thread identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_THREAD_INFO_EXITED_THREAD"></a><a id="minidump_thread_info_exited_thread"></a><dl>
<dt><b>MINIDUMP_THREAD_INFO_EXITED_THREAD</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The thread has exited (not running any code) at the time of the dump.

</td>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_THREAD_INFO_INVALID_CONTEXT"></a><a id="minidump_thread_info_invalid_context"></a><dl>
<dt><b>MINIDUMP_THREAD_INFO_INVALID_CONTEXT</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Thread context could not be retrieved.

</td>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_THREAD_INFO_INVALID_INFO"></a><a id="minidump_thread_info_invalid_info"></a><dl>
<dt><b>MINIDUMP_THREAD_INFO_INVALID_INFO</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Thread information could not be retrieved.

</td>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_THREAD_INFO_INVALID_TEB"></a><a id="minidump_thread_info_invalid_teb"></a><dl>
<dt><b>MINIDUMP_THREAD_INFO_INVALID_TEB</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
TEB information could not be retrieved.

</td>
</tr>
<tr>
<td width="40%"><a id="MINIDUMP_THREAD_INFO_WRITING_THREAD"></a><a id="minidump_thread_info_writing_thread"></a><dl>
<dt><b>MINIDUMP_THREAD_INFO_WRITING_THREAD</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
This is the thread that called <b>MiniDumpWriteDump</b>.

</td>
</tr>
</table>

### -field DumpError

An <b>HRESULT</b> value that indicates the dump status.

### -field ExitStatus

The thread termination status code.

### -field CreateTime

The time when the thread was created, in 100-nanosecond intervals since January 1, 1601 (UTC).

### -field ExitTime

The time when the thread exited, in 100-nanosecond intervals since January 1, 1601 (UTC).

### -field KernelTime

The time executed in kernel mode, in 100-nanosecond intervals.

### -field UserTime

The time executed in user mode, in 100-nanosecond intervals.

### -field StartAddress

The starting address of the thread.

### -field Affinity

The processor affinity mask.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_thread_info_list">MINIDUMP_THREAD_INFO_LIST</a>

