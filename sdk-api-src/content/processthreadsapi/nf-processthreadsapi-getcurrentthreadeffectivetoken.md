---
UID: NF:processthreadsapi.GetCurrentThreadEffectiveToken
title: GetCurrentThreadEffectiveToken function (processthreadsapi.h)
description: Retrieves a pseudo-handle that you can use as a shorthand way to refer to the token that is currently in effect for the thread, which is the thread token if one exists and the process token otherwise.
helpviewer_keywords: ["GetCurrentThreadEffectiveToken","GetCurrentThreadEffectiveToken function [Security]","processthreadsapi/GetCurrentThreadEffectiveToken","security.getcurrentthreadeffectivetoken"]
old-location: security\getcurrentthreadeffectivetoken.htm
tech.root: processthreadsapi
ms.assetid: 794E9086-17E7-4520-AB30-63DF00FF7AA4
ms.date: 12/05/2018
ms.keywords: GetCurrentThreadEffectiveToken, GetCurrentThreadEffectiveToken function [Security], processthreadsapi/GetCurrentThreadEffectiveToken, security.getcurrentthreadeffectivetoken
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
 - GetCurrentThreadEffectiveToken
 - processthreadsapi/GetCurrentThreadEffectiveToken
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
 - GetCurrentThreadEffectiveToken
---

# GetCurrentThreadEffectiveToken function


## -description

Retrieves a pseudo-handle that you can use as a shorthand way to refer to the token that is currently in effect for the thread, which is the thread token if one exists and the process token otherwise.



## -returns

A pseudo-handle that you can use as a shorthand way to refer to the token that is currently in effect for the thread.

## -remarks

A pseudo-handle is a special constant that can function as the effective token for the current thread.  The calling thread can use a pseudo-handle to specify the effective token for that thread whenever a token handle is required.  Child processes do not inherit pseudo-handles.

Starting in Windows 8, this pseudo-handle has only TOKEN_QUERY and TOKEN_QUERY_SOURCE access rights. 

The pseudo-handle cannot be duplicated by the <a href="/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function or the <a href="/windows/win32/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a> function.

You do not need to close the pseudo-handle when you no longer need it. If you call the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function with a pseudo-handle, the function has no effect.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocesstoken">GetCurrentProcessToken</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadtoken">GetCurrentThreadToken</a>
