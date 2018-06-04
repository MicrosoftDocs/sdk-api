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

# _MINIDUMP_THREAD_INFO structure


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




<a href="https://msdn.microsoft.com/ee02a8fa-c81d-4b23-b8a2-6ff31cdaf3de">MINIDUMP_THREAD_INFO_LIST</a>
 

 

