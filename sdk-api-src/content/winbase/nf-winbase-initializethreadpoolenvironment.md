---
UID: NF:winbase.InitializeThreadpoolEnvironment
title: InitializeThreadpoolEnvironment function
author: windows-sdk-content
description: Initializes a callback environment.
old-location: base\initializethreadpoolenvironment.htm
tech.root: procthread
ms.assetid: ad610b7a-9865-4feb-81d2-491f9f87ef3e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InitializeThreadpoolEnvironment, InitializeThreadpoolEnvironment function, base.initializethreadpoolenvironment, winbase/InitializeThreadpoolEnvironment
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
 - InitializeThreadpoolEnvironment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitializeThreadpoolEnvironment function


## -description


Initializes a callback environment.


## -parameters




### -param pcbe [out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines a callback environment.


## -returns



This function does not return a value.




## -remarks



By default, a callback executes in the default thread pool for the process. No cleanup group is associated with the callback environment, the caller is responsible for keeping the callback's DLL loaded while there are outstanding callbacks, and the callback is expected to run in a reasonable amount of time for the application. 

Create a callback environment if you plan to call one of the following functions to modify the environment:

<ul>
<li>
<a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>
</li>
<li>
<a href="https://msdn.microsoft.com/41d5d8c5-4938-4274-bcfa-b122bbc70530">SetThreadpoolCallbackLibrary</a>
</li>
<li>
<a href="https://msdn.microsoft.com/022d83de-ff6c-4bc8-8213-42f403a323e8">SetThreadpoolCallbackPool</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c24d3e9b-5a4e-43e1-a903-b612d022aa97">SetThreadpoolCallbackPriority</a>
</li>
<li>
<a href="https://msdn.microsoft.com/19ca0501-02d8-4851-8015-65e53d6f8074">SetThreadpoolCallbackRunsLong</a>
</li>
</ul>
To use the default callback environment, set the optional callback environment parameter to NULL when calling one of the following functions: 

<ul>
<li>
<a href="https://msdn.microsoft.com/621f4747-50fa-4538-bd6a-dbe4dbb05dd1">CreateThreadpoolIo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1fa98b79-e646-4e48-9979-1817d2c1b713">CreateThreadpoolTimer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ba19f5f9-d4b0-4865-9609-95e7697d61c0">CreateThreadpoolWait</a>
</li>
<li>
<a href="https://msdn.microsoft.com/50647d87-1768-4918-8376-a6a04daca621">CreateThreadpoolWork</a>
</li>
<li>
<a href="https://msdn.microsoft.com/689d197e-195f-419c-9317-b30c614038c4">TrySubmitThreadpoolCallback</a>
</li>
</ul>
The <b>InitializeThreadpoolEnvironment</b> function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b6a635f3-a603-4c2f-9aa9-1baa51922394">DestroyThreadpoolEnvironment</a>



<a href="https://msdn.microsoft.com/395db7ba-ff39-46ee-917b-2896a0e99d43">SetThreadpoolCallbackCleanupGroup</a>



<a href="https://msdn.microsoft.com/41d5d8c5-4938-4274-bcfa-b122bbc70530">SetThreadpoolCallbackLibrary</a>



<a href="https://msdn.microsoft.com/022d83de-ff6c-4bc8-8213-42f403a323e8">SetThreadpoolCallbackPool</a>



<a href="https://msdn.microsoft.com/19ca0501-02d8-4851-8015-65e53d6f8074">SetThreadpoolCallbackRunsLong</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

