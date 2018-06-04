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



