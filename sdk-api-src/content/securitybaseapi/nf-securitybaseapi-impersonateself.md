---
UID: NF:securitybaseapi.ImpersonateSelf
title: ImpersonateSelf function (securitybaseapi.h)
description: Obtains an access token that impersonates the security context of the calling process. The token is assigned to the calling thread.
helpviewer_keywords: ["ImpersonateSelf","ImpersonateSelf function [Security]","_win32_impersonateself","security.impersonateself","securitybaseapi/ImpersonateSelf"]
old-location: security\impersonateself.htm
tech.root: security
ms.assetid: f909e3a7-6c7f-4c05-aa2e-e637113804c9
ms.date: 12/05/2018
ms.keywords: ImpersonateSelf, ImpersonateSelf function [Security], _win32_impersonateself, security.impersonateself, securitybaseapi/ImpersonateSelf
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
 - ImpersonateSelf
 - securitybaseapi/ImpersonateSelf
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
 - ImpersonateSelf
---

# ImpersonateSelf function


## -description

The <b>ImpersonateSelf</b> function obtains an <a href="/windows/desktop/SecGloss/a-gly">access token</a> that impersonates the <a href="/windows/desktop/SecGloss/s-gly">security context</a> of the calling <a href="/windows/desktop/SecGloss/p-gly">process</a>. The token is assigned to the calling thread.

## -parameters

### -param ImpersonationLevel [in]

Specifies a 
<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a> enumerated type that supplies the impersonation level of the new token.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>ImpersonateSelf</b> function is used for tasks such as enabling a <a href="/windows/desktop/SecGloss/p-gly">privilege</a> for a single thread rather than for the entire process or for changing the default <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL) for a single thread.

The server can call the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a> function when the impersonation is complete.

For this function to succeed, the DACL protecting the process token must grant the TOKEN_DUPLICATE right to itself.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Client/Server Access Control Functions</a>



<a href="/windows/desktop/SecAuthZ/client-server-access-control">Client/Server Access Control Overview</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient">ImpersonateNamedPipeClient</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself">RevertToSelf</a>



<a href="/windows/desktop/api/winnt/ne-winnt-security_impersonation_level">SECURITY_IMPERSONATION_LEVEL</a>