---
UID: NF:securitybaseapi.ImpersonateLoggedOnUser
title: ImpersonateLoggedOnUser function (securitybaseapi.h)
description: Lets the calling thread impersonate the security context of a logged-on user. The user is represented by a token handle.
helpviewer_keywords: ["ImpersonateLoggedOnUser","ImpersonateLoggedOnUser function [Security]","_win32_impersonateloggedonuser","security.impersonateloggedonuser","securitybaseapi/ImpersonateLoggedOnUser"]
old-location: security\impersonateloggedonuser.htm
tech.root: security
ms.assetid: cf5c31ae-6749-45c2-888f-697060cc8c75
ms.date: 12/05/2018
ms.keywords: ImpersonateLoggedOnUser, ImpersonateLoggedOnUser function [Security], _win32_impersonateloggedonuser, security.impersonateloggedonuser, securitybaseapi/ImpersonateLoggedOnUser
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ImpersonateLoggedOnUser
 - securitybaseapi/ImpersonateLoggedOnUser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - ImpersonateLoggedOnUser
---

# ImpersonateLoggedOnUser function


## -description

The <b>ImpersonateLoggedOnUser</b> function lets the calling thread impersonate the <a href="/windows/desktop/SecGloss/s-gly">security context</a> of a logged-on user. The user is represented by a token handle.

## -parameters

### -param hToken [in]

A handle to a primary or impersonation <a href="/windows/desktop/SecGloss/a-gly">access token</a> that represents a logged-on user. This can be a token handle returned by a call to 
<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> functions. If <i>hToken</i> is a handle to a <a href="/windows/desktop/SecGloss/p-gly">primary token</a>, the token must have <b>TOKEN_QUERY</b> and <b>TOKEN_DUPLICATE</b> access. If <i>hToken</i> is a handle to an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>, the token must have <b>TOKEN_QUERY</b> and <b>TOKEN_IMPERSONATE</b> access.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The impersonation lasts until the thread exits or until it calls 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a>.

The calling thread does not need to have any particular <a href="/windows/desktop/SecGloss/p-gly">privileges</a> to call <b>ImpersonateLoggedOnUser</b>.

If the call to <b>ImpersonateLoggedOnUser</b> fails, the client connection is not impersonated and the client request is made in the security context of the process. If the process is running as a highly privileged account, such as LocalSystem, or as a member of an administrative group, the user may be able to perform actions they would otherwise be disallowed. Therefore, it is important to always check the return value of the call, and if it fails, raise an error; do not continue execution of the client request.

All impersonate functions, including <b>ImpersonateLoggedOnUser</b> allow the requested impersonation if one of the following is true: 



<ul>
<li>The requested impersonation level of the token is less than <b>SecurityImpersonation</b>, such as <b>SecurityIdentification</b> or <b>SecurityAnonymous</b>.</li>
<li>The caller has the <b>SeImpersonatePrivilege</b> privilege.</li>
<li>A process (or another process in the caller's logon session) created the token using explicit credentials through <a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a> or <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalogonuser">LsaLogonUser</a> function.</li>
<li>The authenticated identity is same as the caller.</li>
</ul>
<b>Windows XP with SP1 and earlier:  </b>The <b>SeImpersonatePrivilege</b> privilege is not supported.

For more information about impersonation, see 
<a href="/windows/desktop/SecAuthZ/client-impersonation">Client Impersonation</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a>