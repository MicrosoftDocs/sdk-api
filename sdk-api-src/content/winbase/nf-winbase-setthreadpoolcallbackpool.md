---
UID: NF:winbase.SetThreadpoolCallbackPool
title: SetThreadpoolCallbackPool function
author: windows-sdk-content
description: Sets the thread pool to be used when generating callbacks.
old-location: base\setthreadpoolcallbackpool.htm
old-project: procthread
ms.assetid: 022d83de-ff6c-4bc8-8213-42f403a323e8
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: SetThreadpoolCallbackPool, SetThreadpoolCallbackPool function, base.setthreadpoolcallbackpool, winbase/SetThreadpoolCallbackPool
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - SetThreadpoolCallbackPool
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# SetThreadpoolCallbackPool function


## -description


Sets the thread pool to be used when generating callbacks.


## -parameters




### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.


### -param ptpp [in]

A <b>TP_POOL</b> structure that defines the thread pool. The <a href="https://msdn.microsoft.com/cc00d7bf-ac52-44ff-a6a8-76c8eaace5e6">CreateThreadpool</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



If you do not specify a thread pool, the global thread pool is used.

This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b6a635f3-a603-4c2f-9aa9-1baa51922394">DestroyThreadpoolEnvironment</a>



<a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>



<a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/41d5d8c5-4938-4274-bcfa-b122bbc70530">SetThreadpoolCallbackLibrary</a>



<a href="https://msdn.microsoft.com/c24d3e9b-5a4e-43e1-a903-b612d022aa97">SetThreadpoolCallbackPriority</a>



<a href="https://msdn.microsoft.com/19ca0501-02d8-4851-8015-65e53d6f8074">SetThreadpoolCallbackRunsLong</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

