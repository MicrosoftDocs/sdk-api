---
UID: NF:processthreadsapi.GetCurrentProcessToken
title: GetCurrentProcessToken function
author: windows-sdk-content
description: Retrieves a pseudo-handle that you can use as a shorthand way to refer to the access token associated with a process.
old-location: security\getcurrentprocesstoken.htm
old-project: SecAuthZ
ms.assetid: 9DD1781A-4C77-4E22-9FCF-579FC90F3028
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetCurrentProcessToken, GetCurrentProcessToken function [Security], processthreadsapi/GetCurrentProcessToken, security.getcurrentprocesstoken
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PSS_VA_SPACE_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processthreadsapi.h
api_name:
-	GetCurrentProcessToken
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetCurrentProcessToken function


## -description


Retrieves a pseudo-handle that you can use as a shorthand way to refer to the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> associated with a process.


## -parameters






## -returns



A pseudo-handle that you can use as a shorthand way to refer to the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> associated with a process.




## -remarks



A pseudo-handle is a special constant that can function as the access token for the current process.  The calling process can use a pseudo-handle to specify the access token for that process whenever a token handle is required.  Child processes do not inherit pseudo-handles.

Starting in Windows 8, this pseudo-handle has only TOKEN_QUERY and TOKEN_QUERY_SOURCE access rights. 


A process can create a standard handle that is valid in the context of other processes and can be inherited by other processes. To create this standard handle, call the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function and specify the pseudo-handle as the source handle.

You do not need to close the pseudo-handle when you no longer need it. If you call the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function with a pseudo-handle, the function has no effect. If you call <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> to duplicate the pseudo-handle, however, you must close the duplicate handle .





## -see-also




<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>



<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>
 

 

