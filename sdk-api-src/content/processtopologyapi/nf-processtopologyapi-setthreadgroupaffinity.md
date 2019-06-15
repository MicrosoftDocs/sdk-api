---
UID: NF:processtopologyapi.SetThreadGroupAffinity
title: SetThreadGroupAffinity function (processtopologyapi.h)
author: windows-sdk-content
description: Sets the processor group affinity for the specified thread.
old-location: base\setthreadgroupaffinity.htm
tech.root: ProcThread
ms.assetid: 9f24f1bf-a63d-4318-af2a-eb3553f2b0f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetThreadGroupAffinity, SetThreadGroupAffinity function, base.setthreadgroupaffinity, processtopologyapi/SetThreadGroupAffinity, winbase/SetThreadGroupAffinity
ms.topic: function
f1_keywords: ["processtopologyapi/SetThreadGroupAffinity"]
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetThreadGroupAffinity function


## -description


Sets the processor group affinity for the specified thread.


## -parameters




### -param hThread [in]

A handle to the thread. 

The handle must have the THREAD_SET_INFORMATION access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.


### -param GroupAffinity [in]

A <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_group_affinity">GROUP_AFFINITY</a> structure that specifies the processor group affinity to be used for the specified thread.


### -param PreviousGroupAffinity [out, optional]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_group_affinity">GROUP_AFFINITY</a> structure to receive the thread's previous group affinity. This parameter can be NULL.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-adsgetlasterror">GetLastError</a>.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-_group_affinity">GROUP_AFFINITY</a>
 

 

