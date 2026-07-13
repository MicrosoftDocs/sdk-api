---
UID: NF:processtopologyapi.SetThreadGroupAffinity
title: SetThreadGroupAffinity function (processtopologyapi.h)
description: Sets the processor group affinity for the specified thread.
helpviewer_keywords: ["SetThreadGroupAffinity","SetThreadGroupAffinity function","base.setthreadgroupaffinity","processtopologyapi/SetThreadGroupAffinity","winbase/SetThreadGroupAffinity"]
old-location: base\setthreadgroupaffinity.htm
tech.root: backup
ms.assetid: 9f24f1bf-a63d-4318-af2a-eb3553f2b0f9
ms.date: 12/05/2018
ms.keywords: SetThreadGroupAffinity, SetThreadGroupAffinity function, base.setthreadgroupaffinity, processtopologyapi/SetThreadGroupAffinity, winbase/SetThreadGroupAffinity
req.header: processtopologyapi.h
req.include-header: 
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
 - SetThreadGroupAffinity
 - processtopologyapi/SetThreadGroupAffinity
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
 - SetThreadGroupAffinity
---

# SetThreadGroupAffinity function


## -description

Sets the processor group affinity for the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread. 

The handle must have the THREAD_SET_INFORMATION access right. For more information, see 
<a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

### -param GroupAffinity [in]

A <a href="/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a> structure that specifies the processor group affinity to be used for the specified thread.

### -param PreviousGroupAffinity [out, optional]

A pointer to a <a href="/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a> structure to receive the thread's previous group affinity. This parameter can be NULL.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use <a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">GetLastError</a>.

## -remarks

Starting with Windows 11 and Windows Server 2022, on a system with more than 64 processors, process and thread affinities span all processors in the system, across all <a href="/windows/desktop/ProcThread/processor-groups">processor groups</a>, by default. 
The <b>SetThreadGroupAffinity</b> function restricts a thread's affinity to the processors over the single processor group specified by the given <i>GroupAffinity</i>. This group will also become the thread's primary group.

To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-group_affinity">GROUP_AFFINITY</a>
