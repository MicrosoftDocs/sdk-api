---
UID: NF:processthreadsapi.GetCurrentThreadToken
title: GetCurrentThreadToken function (processthreadsapi.h)
description: Retrieves a pseudo-handle that you can use as a shorthand way to refer to the impersonation token that was assigned to the current thread.
old-location: security\getcurrentthreadtoken.htm
tech.root: SecAuthZ
ms.assetid: D56FE64F-CFE0-4BE4-BBDA-DF0B79E3E86F
ms.date: 12/05/2018
ms.keywords: GetCurrentThreadToken, GetCurrentThreadToken function [Security], processthreadsapi/GetCurrentThreadToken, security.getcurrentthreadtoken
f1_keywords:
- processthreadsapi/GetCurrentThreadToken
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentThreadToken function


## -description


Retrieves a pseudo-handle that you can use as a shorthand way to refer to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/i-gly">impersonation token</a> that was assigned to the current thread. 


## -parameters






## -returns



A pseudo-handle that you can use as a shorthand way to refer to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/i-gly">impersonation token</a> that was assigned to the current thread.




## -remarks



A pseudo-handle is a special constant that can function as the impersonation token for the current thread.  The calling thread can use a pseudo-handle to specify the impersonation token for that thread whenever a token handle is required.  Child processes do not inherit pseudo-handles.

Starting in Windows 8, this pseudo-handle has only TOKEN_QUERY and TOKEN_QUERY_SOURCE access rights. 


A thread can create a standard handle that is valid in the context of other processes and can be inherited by other processes. To create this standard handle, call the <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function and specify the pseudo-handle as the source handle.

You do not need to close the pseudo-handle when you no longer need it. If you call the <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function with a pseudo-handle, the function has no effect. If you call <a href="https://docs.microsoft.com/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> to duplicate the pseudo-handle, however, you must close the duplicate handle .





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadtoken">SetThreadToken</a>
 

 

