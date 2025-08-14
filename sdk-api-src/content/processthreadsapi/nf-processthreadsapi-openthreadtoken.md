---
UID: NF:processthreadsapi.OpenThreadToken
title: OpenThreadToken function (processthreadsapi.h)
description: Opens the access token associated with a thread.
helpviewer_keywords: ["OpenThreadToken","OpenThreadToken function [Security]","_win32_openthreadtoken","processthreadsapi/OpenThreadToken","security.openthreadtoken"]
old-location: security\openthreadtoken.htm
tech.root: processthreadsapi
ms.assetid: 5003f0c4-41e9-4a14-b6a9-4f259c4af08b
ms.date: 12/05/2018
ms.keywords: OpenThreadToken, OpenThreadToken function [Security], _win32_openthreadtoken, processthreadsapi/OpenThreadToken, security.openthreadtoken
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
 - OpenThreadToken
 - processthreadsapi/OpenThreadToken
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
 - OpenThreadToken
---

# OpenThreadToken function


## -description

The <b>OpenThreadToken</b> function opens the <a href="/windows/desktop/SecGloss/a-gly">access token</a> associated with a thread.

## -parameters

### -param ThreadHandle [in]

A handle to the thread whose access token is opened.

### -param DesiredAccess [in]

Specifies an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> that specifies the requested types of access to the access token. These requested access types are reconciled against the token's <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) to determine which accesses are granted or denied. 




For a list of access rights for access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a>.

### -param OpenAsSelf [in]

TRUE if the access check is to be made against the  process-level <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

<b>FALSE</b> if the access check is to be made against the current security context of the thread calling the <b>OpenThreadToken</b> function.

The <i>OpenAsSelf</i> parameter allows the caller of this function to open the access token of a specified thread when the caller is impersonating a token at <b>SecurityIdentification</b> level. Without this parameter, the calling thread cannot open the access token on the specified thread because it is impossible to open executive-level objects by using the <b>SecurityIdentification</b> impersonation level.

### -param TokenHandle [out]

A pointer to a variable that receives the handle to the newly opened access token.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the token has the anonymous impersonation level, the token will not be opened and <b>OpenThreadToken</b> sets  ERROR_CANT_OPEN_ANONYMOUS as the error.

## -remarks

Tokens with the anonymous impersonation level cannot be opened.

Close the access token handle returned through the <i>TokenHandle</i> parameter by calling 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck">AccessCheck</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokengroups">AdjustTokenGroups</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges">AdjustTokenPrivileges</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getcurrentthreadtoken">GetCurrentThreadToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadtoken">SetThreadToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation">SetTokenInformation</a>