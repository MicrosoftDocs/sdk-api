---
UID: NF:securitybaseapi.ImpersonateLoggedOnUser
title: ImpersonateLoggedOnUser function (securitybaseapi.h)
description: Lets the calling thread impersonate the security context of a logged-on user. The user is represented by a token handle.
helpviewer_keywords: ["ImpersonateLoggedOnUser","ImpersonateLoggedOnUser function [Security]","_win32_impersonateloggedonuser","security.impersonateloggedonuser","securitybaseapi/ImpersonateLoggedOnUser"]
old-location: security\impersonateloggedonuser.htm
tech.root: security
ms.assetid: cf5c31ae-6749-45c2-888f-697060cc8c75
ms.date: 09/24/2025
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

The **ImpersonateLoggedOnUser** function lets the calling thread impersonate the [security context](/windows/win32/SecGloss/s-gly) of a logged-on user. The user is represented by a token handle.

## -parameters

### -param hToken [in]

A handle to a primary or impersonation [access token](/windows/win32/SecGloss/a-gly) that represents a logged-on user. This can be a token handle returned by a call to [LogonUser](/windows/win32/api/winbase/nf-winbase-logonusera), [CreateRestrictedToken](nf-securitybaseapi-createrestrictedtoken.md), [DuplicateToken](nf-securitybaseapi-duplicatetoken.md), [DuplicateTokenEx](nf-securitybaseapi-duplicatetokenex.md), [OpenProcessToken](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken), or [OpenThreadToken](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) functions. If *hToken* is a handle to a [primary token](/windows/win32/SecGloss/p-gly), the token must have **TOKEN_QUERY** and **TOKEN_DUPLICATE** access. If *hToken* is a handle to an [impersonation token](/windows/win32/SecGloss/i-gly), the token must have **TOKEN_QUERY** and **TOKEN_IMPERSONATE** access.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

The impersonation lasts until the thread exits or until it calls [RevertToSelf](nf-securitybaseapi-reverttoself.md).

The calling thread does not need to have any particular [privileges](/windows/win32/SecGloss/p-gly) to call **ImpersonateLoggedOnUser**.

If the call to **ImpersonateLoggedOnUser** fails, the client connection is not impersonated and the client request is made in the security context of the process. If the process is running as a highly privileged account, such as LocalSystem, or as a member of an administrative group, the user may be able to perform actions they would otherwise be disallowed. Therefore, it is important to always check the return value of the call, and if it fails, raise an error; do not continue execution of the client request.

All impersonate functions, including **ImpersonateLoggedOnUser** allow the requested impersonation if one of the following is true:

- The caller has the **SeImpersonatePrivilege** privilege.
- A process (or another process in the caller's logon session) created the token using explicit credentials through [LogonUser](/windows/win32/api/winbase/nf-winbase-logonusera) or [LsaLogonUser](/windows/win32/api/ntsecapi/nf-ntsecapi-lsalogonuser) function.
- The authenticated identity is same as the caller.

> [!IMPORTANT]
> The token must have an impersonation level of **SecurityImpersonation** or higher for impersonation to succeed. Tokens with **SecurityIdentification** or **SecurityAnonymous** levels cannot be used for impersonation, even if the caller has **SeImpersonatePrivilege**. **SecurityIdentification** tokens allow identity verification and ACL checks but do not permit impersonation.

#### Impersonation Level Requirements

The behavior varies based on the token's impersonation level:

- **SecurityAnonymous**: The server cannot obtain client identity information and cannot impersonate the client.
- **SecurityIdentification**: The server can obtain the client's identity and perform access validation, but cannot impersonate the client. This is the default level for many scenarios.
- **SecurityImpersonation**: The server can impersonate the client's security context on the local system. This is the minimum level required for **ImpersonateLoggedOnUser** to succeed.
- **SecurityDelegation**: The server can impersonate the client on remote systems as well as locally.

**Windows XP with SP1 and earlier:** The **SeImpersonatePrivilege** privilege is not supported.

For more information about impersonation, see [Client Impersonation](/windows/win32/SecAuthZ/client-impersonation).

## -see-also

[Client/Server Access Control Functions](/windows/win32/SecAuthZ/authorization-functions)

[Client/Server Access Control Overview](/windows/win32/SecAuthZ/client-server-access-control)

[CreateProcessAsUser](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)

[CreateRestrictedToken](nf-securitybaseapi-createrestrictedtoken.md)

[DuplicateToken](nf-securitybaseapi-duplicatetoken.md)

[DuplicateTokenEx](nf-securitybaseapi-duplicatetokenex.md)

[LogonUser](/windows/win32/api/winbase/nf-winbase-logonusera)

[OpenProcessToken](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)

[OpenThreadToken](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken)

[RevertToSelf](nf-securitybaseapi-reverttoself.md)