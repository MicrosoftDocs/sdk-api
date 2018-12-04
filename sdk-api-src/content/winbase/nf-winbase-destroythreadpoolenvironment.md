---
UID: NF:winbase.DestroyThreadpoolEnvironment
title: DestroyThreadpoolEnvironment function
author: windows-sdk-content
description: Deletes the specified callback environment. Call this function when the callback environment is no longer needed for creating new thread pool objects.
old-location: base\destroythreadpoolenvironment.htm
tech.root: procthread
ms.assetid: b6a635f3-a603-4c2f-9aa9-1baa51922394
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: DestroyThreadpoolEnvironment, DestroyThreadpoolEnvironment function, base.destroythreadpoolenvironment, winbase/DestroyThreadpoolEnvironment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - DestroyThreadpoolEnvironment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyThreadpoolEnvironment function


## -description


Deletes the specified callback environment. Call this function when the callback environment is no longer needed for creating new thread pool objects.


## -parameters




### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.


## -returns



This function does not return a value.




## -remarks



This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>



<a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/41d5d8c5-4938-4274-bcfa-b122bbc70530">SetThreadpoolCallbackLibrary</a>



<a href="https://msdn.microsoft.com/022d83de-ff6c-4bc8-8213-42f403a323e8">SetThreadpoolCallbackPool</a>



<a href="https://msdn.microsoft.com/c24d3e9b-5a4e-43e1-a903-b612d022aa97">SetThreadpoolCallbackPriority</a>



<a href="https://msdn.microsoft.com/19ca0501-02d8-4851-8015-65e53d6f8074">SetThreadpoolCallbackRunsLong</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

