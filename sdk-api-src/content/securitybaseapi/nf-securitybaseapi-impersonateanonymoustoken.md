---
UID: NF:securitybaseapi.ImpersonateAnonymousToken
title: ImpersonateAnonymousToken function (securitybaseapi.h)
description: Enables the specified thread to impersonate the system's anonymous logon token.
helpviewer_keywords: ["ImpersonateAnonymousToken","ImpersonateAnonymousToken function [Security]","_win32_impersonateanonymoustoken","security.impersonateanonymoustoken","securitybaseapi/ImpersonateAnonymousToken"]
old-location: security\impersonateanonymoustoken.htm
tech.root: security
ms.assetid: 98d1072e-f569-4c8c-9254-fa558054c7ec
ms.date: 12/05/2018
ms.keywords: ImpersonateAnonymousToken, ImpersonateAnonymousToken function [Security], _win32_impersonateanonymoustoken, security.impersonateanonymoustoken, securitybaseapi/ImpersonateAnonymousToken
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
 - ImpersonateAnonymousToken
 - securitybaseapi/ImpersonateAnonymousToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - ImpersonateAnonymousToken
---

# ImpersonateAnonymousToken function


## -description

The <b>ImpersonateAnonymousToken</b> function enables the specified thread to impersonate the system's anonymous logon token. To ensure that a token matches the operating system's concept of anonymous access, this function should be called before attempting network access to generate an anonymous token on the remote server.

## -parameters

### -param ThreadHandle [in]

A handle to the thread to impersonate the system's anonymous logon token.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

An error of ACCESS_DENIED may indicate that the token is for a restricted process. Use OpenProcessToken and IsTokenRestricted to check if the process is restricted.

## -remarks

Anonymous tokens do not include the Everyone Group SID unless the system default has been overridden by setting the HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Lsa\EveryoneIncludesAnonymous registry value to DWORD=1.

To cancel the impersonation call 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a>