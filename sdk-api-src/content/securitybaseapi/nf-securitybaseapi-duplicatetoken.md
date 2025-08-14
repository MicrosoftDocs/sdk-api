---
UID: NF:securitybaseapi.DuplicateToken
title: DuplicateToken function (securitybaseapi.h)
description: Creates a new access token that duplicates one already in existence.
helpviewer_keywords: ["DuplicateToken","DuplicateToken function [Security]","_win32_duplicatetoken","security.duplicatetoken","securitybaseapi/DuplicateToken"]
old-location: security\duplicatetoken.htm
tech.root: security
ms.assetid: 796ec60e-fcae-48a9-b471-de3dce831306
ms.date: 12/05/2018
ms.keywords: DuplicateToken, DuplicateToken function [Security], _win32_duplicatetoken, security.duplicatetoken, securitybaseapi/DuplicateToken
req.header: securitybaseapi.h
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
 - DuplicateToken
 - securitybaseapi/DuplicateToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - DuplicateToken
---

# DuplicateToken function


## -description

The <b>DuplicateToken</b> function creates a new <a href="/windows/desktop/SecGloss/a-gly">access token</a> that duplicates one already in existence.

## -parameters

### -param ExistingTokenHandle [in]

A handle to an access token opened with TOKEN_DUPLICATE access.

### -param ImpersonationLevel [in]

Specifies a 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> enumerated type that supplies the impersonation level of the new token.

### -param DuplicateTokenHandle [out]

A pointer to a variable that receives a handle to the duplicate token. This handle has TOKEN_IMPERSONATE and TOKEN_QUERY access to the new token.

When you have finished using the new token, call the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the token handle.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>DuplicateToken</b> function creates an <a href="/windows/desktop/SecGloss/i-gly">impersonation token</a>, which you can use in functions such as <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadtoken">SetThreadToken</a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a>. The token created by <b>DuplicateToken</b> cannot be used in the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> function, which requires a <a href="/windows/desktop/SecGloss/p-gly">primary token</a>. To create a token that you can pass to <b>CreateProcessAsUser</b>, use the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a> function.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetokenex">DuplicateTokenEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadtoken">SetThreadToken</a>