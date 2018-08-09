---
UID: NF:processthreadsapi.QueryProcessAffinityUpdateMode
title: QueryProcessAffinityUpdateMode function
author: windows-sdk-content
description: Retrieves the affinity update mode of the specified process.
old-location: base\queryprocessaffinityupdatemode.htm
old-project: procthread
ms.assetid: e1c9fab2-45a0-4ea7-bafb-91fc0f22e658
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PROCESS_AFFINITY_ENABLE_AUTO_UPDATE, QueryProcessAffinityUpdateMode, QueryProcessAffinityUpdateMode function, base.queryprocessaffinityupdatemode, processthreadsapi/QueryProcessAffinityUpdateMode, winbase/QueryProcessAffinityUpdateMode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - QueryProcessAffinityUpdateMode
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# QueryProcessAffinityUpdateMode function


## -description


Retrieves the affinity update mode of the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param lpdwFlags [out, optional]

The affinity update mode. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Dynamic update of the process affinity by the system is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_AFFINITY_ENABLE_AUTO_UPDATE"></a><a id="process_affinity_enable_auto_update"></a><dl>
<dt><b>PROCESS_AFFINITY_ENABLE_AUTO_UPDATE</b></dt>
<dt>0x00000001UL</dt>
</dl>
</td>
<td width="60%">
Dynamic update of the process affinity by the system is enabled.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To compile an application that calls this function, define _WIN32_WINNT as 0x0600 or later. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/46e8f7d2-89b9-42cb-9171-d5ae2ec870da">SetProcessAffinityUpdateMode</a>
 

 

