---
UID: NF:winbase.SetThreadpoolCallbackLibrary
title: SetThreadpoolCallbackLibrary function
author: windows-sdk-content
description: Ensures that the specified DLL remains loaded as long as there are outstanding callbacks.
old-location: base\setthreadpoolcallbacklibrary.htm
old-project: ProcThread
ms.assetid: 41d5d8c5-4938-4274-bcfa-b122bbc70530
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SetThreadpoolCallbackLibrary, SetThreadpoolCallbackLibrary function, base.setthreadpoolcallbacklibrary, winbase/SetThreadpoolCallbackLibrary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinBase.h
api_name:
-	SetThreadpoolCallbackLibrary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# SetThreadpoolCallbackLibrary function


## -description


Ensures that the specified DLL remains loaded as long as there are outstanding callbacks.


## -parameters




### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.


### -param mod [in]

A handle to the DLL.


## -returns



This function does not return a value.




## -remarks



You should call this function if a callback might acquire the loader lock. This prevents a deadlock from occurring when one thread in DllMain is waiting for the callback to end, and another thread that is executing the callback attempts to acquire the loader lock.

If the DLL containing the callback might be unloaded, the cleanup code in DllMain must cancel outstanding callbacks before releasing the object.

Managing callbacks created with a TP_CALLBACK_ENVIRON that specifies a callback library is somewhat processing-intensive.  You should consider other options for ensuring that the library is not unloaded while callbacks are executing, or to guarantee that callbacks which may be executing do not acquire the loader lock.

The thread pool assumes ownership of the library reference supplied to this function.  The caller should not call <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> on a module handle after passing it to this function.

This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.




## -see-also




<a href="https://msdn.microsoft.com/b6a635f3-a603-4c2f-9aa9-1baa51922394">DestroyThreadpoolEnvironment</a>



<a href="https://msdn.microsoft.com/a29ba988-5d66-4914-9e37-a229bce75af2">FreeLibraryWhenCallbackReturns</a>



<a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>



<a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/022d83de-ff6c-4bc8-8213-42f403a323e8">SetThreadpoolCallbackPool</a>



<a href="https://msdn.microsoft.com/c24d3e9b-5a4e-43e1-a903-b612d022aa97">SetThreadpoolCallbackPriority</a>



<a href="https://msdn.microsoft.com/19ca0501-02d8-4851-8015-65e53d6f8074">SetThreadpoolCallbackRunsLong</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

