---
UID: NF:winbase.GetUmsSystemThreadInformation
title: GetUmsSystemThreadInformation function (winbase.h)
author: windows-sdk-content
description: Queries whether the specified thread is a UMS scheduler thread, a UMS worker thread, or a non-UMS thread.
old-location: base\getumssystemthreadinformation.htm
tech.root: ProcThread
ms.assetid: 7c8347b6-6546-4ea9-9b2a-11794782f482
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetUmsSystemThreadInformation, GetUmsSystemThreadInformation function, base.getumssystemthreadinformation, winbase/GetUmsSystemThreadInformation
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1 [desktop apps only],Windows 7 (64-bit only) and Windows Server 2008 R2 with KB977165 installed
req.target-min-winversvr: Windows Server 2008 R2 with SP1 [desktop apps only]
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
 - Kernel32.dll
 - API-MS-Win-Core-ums-l1-1-0.dll
api_name:
 - GetUmsSystemThreadInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetUmsSystemThreadInformation function


## -description


Queries whether the specified thread is a UMS scheduler thread, a UMS worker thread, or a non-UMS thread.


## -parameters




### -param ThreadHandle [in]

A handle to a thread. The thread handle must have the THREAD_QUERY_INFORMATION access right. For more information, see <a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param SystemThreadInfo [in, out]

A pointer to an initialized <a href="https://msdn.microsoft.com/eecdc592-5046-47c3-a4c6-ecb10899db3c">UMS_SYSTEM_THREAD_INFORMATION</a> structure that specifies the kind of thread for the query.


## -returns



Returns TRUE if the specified thread matches the kind of thread specified by the <i>SystemThreadInfo</i> parameter. Otherwise, the function returns FALSE. 




## -remarks



The <b>GetUmsSystemThreadInformation</b> function is intended for use in debuggers, troubleshooting tools, and profiling applications. For example, thread-isolated tracing or single-stepping through instructions might involve suspending all other threads in the process. However, if the thread to be traced is a UMS worker thread, suspending UMS scheduler threads might cause a deadlock because a UMS worker thread requires the intervention of a UMS scheduler thread in order to run. A debugger can call <b>GetUmsSystemThreadInformation</b> for each thread that it might suspend to determine the kind of thread, and then suspend it or not as needed for the code being debugged. 



