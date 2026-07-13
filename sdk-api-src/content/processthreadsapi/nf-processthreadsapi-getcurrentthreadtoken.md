---
UID: NF:processthreadsapi.GetCurrentThreadToken
title: GetCurrentThreadToken function (processthreadsapi.h)
description: Retrieves a pseudo-handle that you can use as a shorthand way to refer to the impersonation token that was assigned to the current thread.
helpviewer_keywords: ["GetCurrentThreadToken","GetCurrentThreadToken function [Security]","processthreadsapi/GetCurrentThreadToken","security.getcurrentthreadtoken"]
old-location: security\getcurrentthreadtoken.htm
tech.root: processthreadsapi
ms.assetid: D56FE64F-CFE0-4BE4-BBDA-DF0B79E3E86F
ms.date: 12/05/2018
ms.keywords: GetCurrentThreadToken, GetCurrentThreadToken function [Security], processthreadsapi/GetCurrentThreadToken, security.getcurrentthreadtoken
req.header: processthreadsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentThreadToken
 - processthreadsapi/GetCurrentThreadToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - GetCurrentThreadToken
---

# GetCurrentThreadToken function


## -description

Retrieves a pseudo-handle that you can use as a shorthand way to refer to the <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> that was assigned to the current thread.



## -returns

A pseudo-handle that you can use as a shorthand way to refer to the <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> that was assigned to the current thread.

## -remarks

A pseudo-handle is a special constant that can function as the impersonation token for the current thread.  The calling thread can use a pseudo-handle to specify the impersonation token for that thread whenever a token handle is required.  Child processes do not inherit pseudo-handles.

Starting in Windows 8, this pseudo-handle has only TOKEN_QUERY and TOKEN_QUERY_SOURCE access rights. 

The pseudo-handle cannot be duplicated by the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function or the <a href="/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a> function.

You do not need to close the pseudo-handle when you no longer need it. If you call the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function with a pseudo-handle, the function has no effect.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadtoken">SetThreadToken</a>
