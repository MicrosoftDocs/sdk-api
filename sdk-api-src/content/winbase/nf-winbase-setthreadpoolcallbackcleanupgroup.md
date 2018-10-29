---
UID: NF:winbase.SetThreadpoolCallbackCleanupGroup
title: SetThreadpoolCallbackCleanupGroup function
author: windows-sdk-content
description: Associates the specified cleanup group with the specified callback environment.
old-location: base\setthreadpoolcallbackcleanupgroup.htm
tech.root: ProcThread
ms.assetid: 395db7ba-ff39-46ee-917b-2896a0e99d43
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SetThreadpoolCallbackCleanupGroup, SetThreadpoolCallbackCleanupGroup function, base.setthreadpoolcallbackcleanupgroup, winbase/SetThreadpoolCallbackCleanupGroup
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
 - SetThreadpoolCallbackCleanupGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadpoolCallbackCleanupGroup function


## -description


Associates the specified cleanup group with the specified callback environment.


## -parameters




### -param pcbe [in, out]

A <b>TP_CALLBACK_ENVIRON</b> structure that defines the callback environment. The <a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a> function returns this structure.


### -param ptpcg [in]

A <b>TP_CLEANUP_GROUP</b> structure that defines the cleanup group. The <a href="https://msdn.microsoft.com/668593fe-2ed1-418d-8cd5-5fac61826ea1">CreateThreadpoolCleanupGroup</a> function returns this structure.


### -param pfng [in, optional]

The cleanup callback to be called if the cleanup group is canceled before the associated object is released. The function is called when you call <a href="https://msdn.microsoft.com/9c78db13-d8dd-4eda-83d9-c9dbbfc6e822">CloseThreadpoolCleanupGroupMembers</a>.


## -returns



This function does not return a value.




## -remarks



This function is implemented as an inline function.

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or higher.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3d349c83-8b1a-4a5b-9625-be905d613b92">Using the Thread Pool Functions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/b6a635f3-a603-4c2f-9aa9-1baa51922394">DestroyThreadpoolEnvironment</a>



<a href="https://msdn.microsoft.com/ad610b7a-9865-4feb-81d2-491f9f87ef3e">InitializeThreadpoolEnvironment</a>



<a href="https://msdn.microsoft.com/41d5d8c5-4938-4274-bcfa-b122bbc70530">SetThreadpoolCallbackLibrary</a>



<a href="https://msdn.microsoft.com/022d83de-ff6c-4bc8-8213-42f403a323e8">SetThreadpoolCallbackPool</a>



<a href="https://msdn.microsoft.com/c24d3e9b-5a4e-43e1-a903-b612d022aa97">SetThreadpoolCallbackPriority</a>



<a href="https://msdn.microsoft.com/19ca0501-02d8-4851-8015-65e53d6f8074">SetThreadpoolCallbackRunsLong</a>



<a href="https://msdn.microsoft.com/abe0798a-0b60-4bdb-a61e-45393f1e958d">Thread Pools</a>
 

 

