---
UID: NF:memoryapi.GetProcessWorkingSetSizeEx
title: GetProcessWorkingSetSizeEx function (memoryapi.h)
description: Retrieves the minimum and maximum working set sizes of the specified process. (GetProcessWorkingSetSizeEx)
helpviewer_keywords: ["GetProcessWorkingSetSizeEx","GetProcessWorkingSetSizeEx function","QUOTA_LIMITS_HARDWS_MAX_DISABLE","QUOTA_LIMITS_HARDWS_MAX_ENABLE","QUOTA_LIMITS_HARDWS_MIN_DISABLE","QUOTA_LIMITS_HARDWS_MIN_ENABLE","base.getprocessworkingsetsizeex","memoryapi/GetProcessWorkingSetSizeEx","winbase/GetProcessWorkingSetSizeEx"]
old-location: base\getprocessworkingsetsizeex.htm
tech.root: backup
ms.assetid: d2de0bf2-012b-480c-a1a5-54e4d3928381
ms.date: 12/05/2018
ms.keywords: GetProcessWorkingSetSizeEx, GetProcessWorkingSetSizeEx function, QUOTA_LIMITS_HARDWS_MAX_DISABLE, QUOTA_LIMITS_HARDWS_MAX_ENABLE, QUOTA_LIMITS_HARDWS_MIN_DISABLE, QUOTA_LIMITS_HARDWS_MIN_ENABLE, base.getprocessworkingsetsizeex, memoryapi/GetProcessWorkingSetSizeEx, winbase/GetProcessWorkingSetSizeEx
req.header: memoryapi.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: onecore.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetProcessWorkingSetSizeEx
 - memoryapi/GetProcessWorkingSetSizeEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-memory-l1-1-9.dll
 - api-ms-win-core-memory-l1-1-8.dll
 - api-ms-win-core-memory-l1-1-7.dll
 - api-ms-win-core-memory-l1-1-6.dll
 - api-ms-win-core-memory-l1-1-5.dll
 - Kernel32.dll
 - API-MS-Win-Core-Memory-l1-1-1.dll
 - API-MS-Win-Core-Memory-l1-1-2.dll
 - API-MS-Win-Core-Memory-l1-1-3.dll
 - API-MS-Win-Core-Memory-L1-1-4.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - GetProcessWorkingSetSizeEx
---

# GetProcessWorkingSetSizeEx function


## -description

Retrieves the minimum and maximum working set sizes of the specified process.

## -parameters

### -param hProcess [in]

A handle to the process whose working set sizes will be obtained. The handle must have the <b>PROCESS_QUERY_INFORMATION</b> or <b>PROCESS_QUERY_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003:  </b>The handle must have the <b>PROCESS_QUERY_INFORMATION</b> access right.

### -param lpMinimumWorkingSetSize [out]

A pointer to a variable that receives the minimum working set size of the specified process, in bytes. The virtual memory manager attempts to keep at least this much memory resident in the process whenever the process is active.

### -param lpMaximumWorkingSetSize [out]

A pointer to a variable that receives the maximum working set size of the specified process, in bytes. The virtual memory manager attempts to keep no more than this much memory resident in the process whenever the process is active when memory is in short supply.

### -param Flags [out]

The flags that control the enforcement of the minimum and maximum working set sizes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MIN_DISABLE"></a><a id="quota_limits_hardws_min_disable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MIN_DISABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The working set may fall below the minimum working set limit if memory demands are high.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MIN_ENABLE"></a><a id="quota_limits_hardws_min_enable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MIN_ENABLE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The working set will not fall below the minimum working set limit.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MAX_DISABLE"></a><a id="quota_limits_hardws_max_disable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MAX_DISABLE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The working set may exceed the maximum working set limit if there is abundant memory.

</td>
</tr>
<tr>
<td width="40%"><a id="QUOTA_LIMITS_HARDWS_MAX_ENABLE"></a><a id="quota_limits_hardws_max_enable"></a><dl>
<dt><b>QUOTA_LIMITS_HARDWS_MAX_ENABLE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The working set will not exceed the maximum working set limit.

</td>
</tr>
</table>

## -remarks

The "working set" of a process is the set of memory pages currently visible to the process in physical RAM memory. These pages are resident and available for an application to use without triggering a page fault. The minimum and maximum working set sizes affect the virtual memory paging behavior of a process.

## -see-also

<a href="/windows/desktop/ProcThread/process-working-set">Process Working Set</a>



<a href="/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsizeex">SetProcessWorkingSetSizeEx</a>
