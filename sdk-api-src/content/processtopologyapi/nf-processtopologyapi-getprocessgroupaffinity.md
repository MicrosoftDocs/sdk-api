---
UID: NF:processtopologyapi.GetProcessGroupAffinity
title: GetProcessGroupAffinity function (processtopologyapi.h)
description: Retrieves the processor group affinity of the specified process.
helpviewer_keywords: ["GetProcessGroupAffinity","GetProcessGroupAffinity function","base.getprocessgroupaffinity","processtopologyapi/GetProcessGroupAffinity","winbase/GetProcessGroupAffinity"]
old-location: base\getprocessgroupaffinity.htm
tech.root: backup
ms.assetid: e22a4910-45dd-4eb6-9ed5-a8e0bcdfad7b
ms.date: 12/05/2018
ms.keywords: GetProcessGroupAffinity, GetProcessGroupAffinity function, base.getprocessgroupaffinity, processtopologyapi/GetProcessGroupAffinity, winbase/GetProcessGroupAffinity
req.header: processtopologyapi.h
req.include-header: Windows.h on Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetProcessGroupAffinity
 - processtopologyapi/GetProcessGroupAffinity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Processtopology-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-Processtopology-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
 - GetProcessGroupAffinity
---

# GetProcessGroupAffinity function


## -description

Retrieves the processor group affinity of the specified process.

## -parameters

### -param hProcess [in]

A handle to the process.

This handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param GroupCount [in, out]

On input, specifies the number of elements in <i>GroupArray</i> array. On output, specifies the number of processor groups written to the array. If the array is too small, the function fails with ERROR_INSUFFICIENT_BUFFER and sets the <i>GroupCount</i> parameter to the number of elements required.

### -param GroupArray [out]

An array of processor group numbers. A group number is included in the array if a thread in the process is assigned to a processor in the group.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use <a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">GetLastError</a>.

If the error value is ERROR_INSUFFICIENT_BUFFER, the <i>GroupCount</i> parameter contains the required buffer size in number of elements.

## -remarks

Starting with Windows 11 and Windows Server 2022, on a system with more than 64 processors, process and thread affinities span all processors in the system, across all <a href="/windows/desktop/ProcThread/processor-groups">processor groups</a>, by default.

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/processtopologyapi/nf-processtopologyapi-getthreadgroupaffinity">GetThreadGroupAffinity</a>



<a href="/windows/desktop/ProcThread/processor-groups">Processor Groups</a>
