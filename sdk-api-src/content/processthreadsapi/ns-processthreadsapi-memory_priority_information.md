---
UID: NS:processthreadsapi._MEMORY_PRIORITY_INFORMATION
title: MEMORY_PRIORITY_INFORMATION (processthreadsapi.h)
description: Specifies the memory priority for a thread or process.
helpviewer_keywords: ["*PMEMORY_PRIORITY_INFORMATION","MEMORY_PRIORITY_BELOW_NORMAL","MEMORY_PRIORITY_INFORMATION","MEMORY_PRIORITY_INFORMATION structure","MEMORY_PRIORITY_LOW","MEMORY_PRIORITY_MEDIUM","MEMORY_PRIORITY_NORMAL","MEMORY_PRIORITY_VERY_LOW","PMEMORY_PRIORITY_INFORMATION","PMEMORY_PRIORITY_INFORMATION structure pointer","_MEMORY_PRIORITY_INFORMATION","base.memory_priority_information","processthreadsapi/MEMORY_PRIORITY_INFORMATION","processthreadsapi/PMEMORY_PRIORITY_INFORMATION"]
old-location: base\memory_priority_information.htm
tech.root: processthreadsapi
ms.assetid: 03cacfdf-5c66-42e4-bfcf-afaacd3ad038
ms.date: 12/05/2018
ms.keywords: '*PMEMORY_PRIORITY_INFORMATION, MEMORY_PRIORITY_BELOW_NORMAL, MEMORY_PRIORITY_INFORMATION, MEMORY_PRIORITY_INFORMATION structure, MEMORY_PRIORITY_LOW, MEMORY_PRIORITY_MEDIUM, MEMORY_PRIORITY_NORMAL, MEMORY_PRIORITY_VERY_LOW, PMEMORY_PRIORITY_INFORMATION, PMEMORY_PRIORITY_INFORMATION structure pointer, _MEMORY_PRIORITY_INFORMATION, base.memory_priority_information, processthreadsapi/MEMORY_PRIORITY_INFORMATION, processthreadsapi/PMEMORY_PRIORITY_INFORMATION'
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MEMORY_PRIORITY_INFORMATION, *PMEMORY_PRIORITY_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MEMORY_PRIORITY_INFORMATION
 - processthreadsapi/_MEMORY_PRIORITY_INFORMATION
 - PMEMORY_PRIORITY_INFORMATION
 - processthreadsapi/PMEMORY_PRIORITY_INFORMATION
 - MEMORY_PRIORITY_INFORMATION
 - processthreadsapi/MEMORY_PRIORITY_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - MEMORY_PRIORITY_INFORMATION
---

# MEMORY_PRIORITY_INFORMATION structure


## -description

Specifies the memory priority for a thread or process. This structure is used by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessinformation">GetProcessInformation</a>, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation">SetProcessInformation</a>, <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadinformation">GetThreadInformation</a>, and <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadinformation">SetThreadInformation</a> functions.

## -struct-fields

### -field MemoryPriority

The memory priority for the thread or process.  This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_VERY_LOW"></a><a id="memory_priority_very_low"></a><dl>
<dt><b>MEMORY_PRIORITY_VERY_LOW</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Very low memory priority.

</td>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_LOW"></a><a id="memory_priority_low"></a><dl>
<dt><b>MEMORY_PRIORITY_LOW</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Low memory priority.

</td>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_MEDIUM"></a><a id="memory_priority_medium"></a><dl>
<dt><b>MEMORY_PRIORITY_MEDIUM</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Medium memory priority.

</td>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_BELOW_NORMAL"></a><a id="memory_priority_below_normal"></a><dl>
<dt><b>MEMORY_PRIORITY_BELOW_NORMAL</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Below normal memory priority.

</td>
</tr>
<tr>
<td width="40%"><a id="MEMORY_PRIORITY_NORMAL"></a><a id="memory_priority_normal"></a><dl>
<dt><b>MEMORY_PRIORITY_NORMAL</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Normal memory priority. This is the default priority for all threads and processes on the system.

</td>
</tr>
</table>

## -remarks

The memory priority of a thread or process serves as a hint to the memory manager when it trims pages from the working set. Other factors being equal, pages with lower memory priority are trimmed before pages with higher memory priority. For more information, see <a href="/windows/desktop/Memory/working-set">Working Set</a>.

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessinformation">GetProcessInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadinformation">GetThreadInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation">SetProcessInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadinformation">SetThreadInformation</a>