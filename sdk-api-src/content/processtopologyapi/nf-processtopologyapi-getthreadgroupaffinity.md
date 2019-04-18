---
UID: NF:processtopologyapi.GetThreadGroupAffinity
title: GetThreadGroupAffinity function (processtopologyapi.h)
author: windows-sdk-content
description: Retrieves the processor group affinity of the specified thread.
old-location: base\getthreadgroupaffinity.htm
tech.root: ProcThread
ms.assetid: effc75be-60da-43cc-bfb3-5fb905e1404d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetThreadGroupAffinity, GetThreadGroupAffinity function, base.getthreadgroupaffinity, processtopologyapi/GetThreadGroupAffinity, winbase/GetThreadGroupAffinity
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetThreadGroupAffinity function


## -description


Retrieves the processor group affinity of the specified thread.


## -parameters




### -param hThread [in]

A handle to the thread for which the processor group affinity is desired. 

The handle must have the THREAD_QUERY_INFORMATION or THREAD_QUERY_LIMITED_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param GroupAffinity [out]

A pointer to a GROUP_AFFINITY structure to receive the group affinity of the thread.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, use <a href="https://msdn.microsoft.com/5e9899e9-e51e-4785-812a-f86eac6e2006">GetLastError</a>.




## -remarks



To compile an application that uses this function, set _WIN32_WINNT &gt;= 0x0601. For more information, see <a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/e22a4910-45dd-4eb6-9ed5-a8e0bcdfad7b">GetProcessGroupAffinity</a>



<a href="https://msdn.microsoft.com/c627ac0f-96e8-48b5-9103-4316f487e173">Processor Groups</a>
 

 

