---
UID: NF:processthreadsapi.GetCurrentThreadToken
title: GetCurrentThreadToken function
author: windows-sdk-content
description: Retrieves a pseudo-handle that you can use as a shorthand way to refer to the impersonation token that was assigned to the current thread.
old-location: security\getcurrentthreadtoken.htm
tech.root: secauthz
ms.assetid: D56FE64F-CFE0-4BE4-BBDA-DF0B79E3E86F
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetCurrentThreadToken, GetCurrentThreadToken function [Security], processthreadsapi/GetCurrentThreadToken, security.getcurrentthreadtoken
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - GetCurrentThreadToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCurrentThreadToken function


## -description


Retrieves a pseudo-handle that you can use as a shorthand way to refer to the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> that was assigned to the current thread. 


## -parameters






## -returns



A pseudo-handle that you can use as a shorthand way to refer to the <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> that was assigned to the current thread.




## -remarks



A pseudo-handle is a special constant that can function as the impersonation token for the current thread.  The calling thread can use a pseudo-handle to specify the impersonation token for that thread whenever a token handle is required.  Child processes do not inherit pseudo-handles.

Starting in Windows 8, this pseudo-handle has only TOKEN_QUERY and TOKEN_QUERY_SOURCE access rights. 


A thread can create a standard handle that is valid in the context of other processes and can be inherited by other processes. To create this standard handle, call the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function and specify the pseudo-handle as the source handle.

You do not need to close the pseudo-handle when you no longer need it. If you call the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function with a pseudo-handle, the function has no effect. If you call <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> to duplicate the pseudo-handle, however, you must close the duplicate handle .





## -see-also




<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>



<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a>



<a href="https://msdn.microsoft.com/ba1a4fce-b3cc-423d-b213-5dfca3dea708">SetThreadToken</a>
 

 

