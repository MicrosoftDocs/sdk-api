---
UID: NF:processthreadsapi.SetThreadToken
title: SetThreadToken function (processthreadsapi.h)
description: Assigns an impersonation token to a thread. The function can also cause a thread to stop using an impersonation token.
helpviewer_keywords: ["SetThreadToken","SetThreadToken function [Security]","_win32_setthreadtoken","processthreadsapi/SetThreadToken","security.setthreadtoken"]
old-location: security\setthreadtoken.htm
tech.root: security
ms.assetid: ba1a4fce-b3cc-423d-b213-5dfca3dea708
ms.date: 12/05/2018
ms.keywords: SetThreadToken, SetThreadToken function [Security], _win32_setthreadtoken, processthreadsapi/SetThreadToken, security.setthreadtoken
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadToken
 - processthreadsapi/SetThreadToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Advapi32.dll
 - API-MS-Win-Core-Processsecurity-l1-1-0.dll
 - Kernel32.dll
 - KernelBase.dll
 - API-MS-Win-Core-Processthreads-l1-1-0.dll
 - API-MS-Win-Core-Processthreads-l1-1-1.dll
 - API-MS-Win-Core-Processthreads-l1-1-2.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - SetThreadToken
---

# SetThreadToken function


## -description

The <b>SetThreadToken</b> function assigns an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a> to a thread. The function can also cause a thread to stop using an impersonation token.

## -parameters

### -param Thread [in, optional]

A pointer to a handle to the thread to which the function assigns the impersonation token. 




If <i>Thread</i> is <b>NULL</b>, the function assigns the impersonation token to the calling thread.

### -param Token [in, optional]

A handle to the impersonation token to assign to the thread. This handle must have been opened with TOKEN_IMPERSONATE access rights. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>. 




If <i>Token</i> is <b>NULL</b>, the function causes the thread to stop using an impersonation token.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When using the <b>SetThreadToken</b> function to impersonate, you must have the impersonate  privileges and make sure that the <b>SetThreadToken</b> function succeeds before calling the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a> function.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>