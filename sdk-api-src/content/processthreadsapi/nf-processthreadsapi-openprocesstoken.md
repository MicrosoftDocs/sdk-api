---
UID: NF:processthreadsapi.OpenProcessToken
title: OpenProcessToken function (processthreadsapi.h)
description: Opens the access token associated with a process.
helpviewer_keywords: ["OpenProcessToken","OpenProcessToken function [Security]","_win32_openprocesstoken","processthreadsapi/OpenProcessToken","security.openprocesstoken"]
old-location: security\openprocesstoken.htm
tech.root: processthreadsapi
ms.assetid: 1e760ad8-7e46-4748-8c45-36ad8efe936a
ms.date: 08/12/2022
ms.keywords: OpenProcessToken, OpenProcessToken function [Security], _win32_openprocesstoken, processthreadsapi/OpenProcessToken, security.openprocesstoken
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
 - OpenProcessToken
 - processthreadsapi/OpenProcessToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - OpenProcessToken
---

# OpenProcessToken function


## -description

The **OpenProcessToken** function opens the <a href="/windows/desktop/SecGloss/a-gly">access token</a> associated with a process.

## -parameters

### -param ProcessHandle [in]

A handle to the process whose access token is opened. The process must have the PROCESS_QUERY_LIMITED_INFORMATION access permission. See [Process Security and Access Rights](/windows/win32/procthread/process-security-and-access-rights) for more info.

### -param DesiredAccess [in]

Specifies an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> that specifies the requested types of access to the access token. These requested access types are compared with the <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) of the token to determine which accesses are granted or denied. 




For a list of access rights for access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.

### -param TokenHandle [out]

A pointer to a handle that identifies the newly opened access token when the function returns.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To get a handle to an elevated process from within a non-elevated process, both processes must be started from the same account.

If the process being checked was started by a different account, the checking process needs to have the SE_DEBUG_NAME privilege enabled. See [Privilege Constants (Authorization)](/windows/win32/secauthz/privilege-constants) for more info.

To close the access token handle returned through the <i>TokenHandle</i> parameter, call <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>

<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a>

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentprocesstoken">GetCurrentProcessToken</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadeffectivetoken">GetCurrentThreadEffectiveToken</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadtoken">GetCurrentThreadToken</a>

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>
