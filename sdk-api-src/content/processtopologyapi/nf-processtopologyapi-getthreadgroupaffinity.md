---
UID: NF:processtopologyapi.GetThreadGroupAffinity
title: GetThreadGroupAffinity function (processtopologyapi.h)
description: Retrieves the processor group affinity of the specified thread.
helpviewer_keywords: ["GetThreadGroupAffinity","GetThreadGroupAffinity function","base.getthreadgroupaffinity","processtopologyapi/GetThreadGroupAffinity","winbase/GetThreadGroupAffinity"]
old-location: base\getthreadgroupaffinity.htm
tech.root: backup
ms.assetid: effc75be-60da-43cc-bfb3-5fb905e1404d
ms.date: 12/05/2018
ms.keywords: GetThreadGroupAffinity, GetThreadGroupAffinity function, base.getthreadgroupaffinity, processtopologyapi/GetThreadGroupAffinity, winbase/GetThreadGroupAffinity
req.header: processtopologyapi.h
req.include-header: Windows.h
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
 - GetThreadGroupAffinity
 - processtopologyapi/GetThreadGroupAffinity
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
 - GetThreadGroupAffinity
---

# GetThreadGroupAffinity function


## -description

Retrieves the processor group affinity of the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread for which the processor group affinity is desired. 

The handle must have the THREAD_QUERY_INFORMATION or THREAD_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param GroupAffinity [out]

A pointer to a [GROUP_AFFINITY](../winnt/ns-winnt-group_affinity.md) structure that receives the group affinity of the thread.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use <a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">GetLastError</a>.

## -remarks

Starting with Windows 11 and Windows Server 2022, on a system with more than 64 processors, process and thread affinities span all processors in the system, across all <a href="/windows/desktop/ProcThread/processor-groups">processor groups</a>, by default. The <b>GetThreadGroupAffinity</b> function retrieves the group affinity over the thread's primary group.

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity">GetProcessGroupAffinity</a>



<a href="/windows/desktop/ProcThread/processor-groups">Processor Groups</a>
