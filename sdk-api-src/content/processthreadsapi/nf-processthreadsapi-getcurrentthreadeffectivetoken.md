---
UID: NF:processthreadsapi.GetCurrentThreadEffectiveToken
title: GetCurrentThreadEffectiveToken function
author: windows-driver-content
description: Retrieves a pseudo-handle that you can use as a shorthand way to refer to the token that is currently in effect for the thread, which is the thread token if one exists and the process token otherwise.
old-location: security\getcurrentthreadeffectivetoken.htm
old-project: SecAuthZ
ms.assetid: 794E9086-17E7-4520-AB30-63DF00FF7AA4
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetCurrentThreadEffectiveToken, GetCurrentThreadEffectiveToken function [Security], processthreadsapi/GetCurrentThreadEffectiveToken, security.getcurrentthreadeffectivetoken
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
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processthreadsapi.h
api_name:
-	GetCurrentThreadEffectiveToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetCurrentThreadEffectiveToken function


## -description


Retrieves a pseudo-handle that you can use as a shorthand way to refer to the token that is currently in effect for the thread, which is the thread token if one exists and the process token otherwise. 


## -parameters






## -returns



A pseudo-handle that you can use as a shorthand way to refer to the token that is currently in effect for the thread.




## -remarks



A pseudo-handle is a special constant that can function as the effective token for the current thread.  The calling thread can use a pseudo-handle to specify the effective token for that thread whenever a token handle is required.  Child processes do not inherit pseudo-handles.

Starting in Windows 8, this pseudo-handle has only TOKEN_QUERY and TOKEN_QUERY_SOURCE access rights. 


A thread can create a standard handle that is valid in the context of other processes and can be inherited by other processes. To create this standard handle, call the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function and specify the pseudo-handle as the source handle.

You do not need to close the pseudo-handle when you no longer need it. If you call the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function with a pseudo-handle, the function has no effect. If you call <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> to duplicate the pseudo-handle, however, you must close the duplicate handle .





## -see-also




<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>



<a href="https://msdn.microsoft.com/9DD1781A-4C77-4E22-9FCF-579FC90F3028">GetCurrentProcessToken</a>



<a href="https://msdn.microsoft.com/D56FE64F-CFE0-4BE4-BBDA-DF0B79E3E86F">GetCurrentThreadToken</a>
 

 

