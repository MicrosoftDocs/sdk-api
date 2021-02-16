---
UID: NS:sspi._SecPkgContext_AccessToken
title: SecPkgContext_AccessToken (sspi.h)
description: Returns a handle to the access token for the current security context.
helpviewer_keywords: ["*PSecPkgContext_AccessToken","PSecPkgContext_AccessToken","PSecPkgContext_AccessToken structure pointer [Security]","SecPkgContext_AccessToken","SecPkgContext_AccessToken structure [Security]","security.secpkgcontext_accesstoken","sspi/PSecPkgContext_AccessToken","sspi/SecPkgContext_AccessToken"]
old-location: security\secpkgcontext_accesstoken.htm
tech.root: security
ms.assetid: 4dc11cbd-7f28-4cb9-aaea-6e5a89ac91f0
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_AccessToken, PSecPkgContext_AccessToken, PSecPkgContext_AccessToken structure pointer [Security], SecPkgContext_AccessToken, SecPkgContext_AccessToken structure [Security], security.secpkgcontext_accesstoken, sspi/PSecPkgContext_AccessToken, sspi/SecPkgContext_AccessToken'
req.header: sspi.h
req.include-header: Security.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SecPkgContext_AccessToken, *PSecPkgContext_AccessToken
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_AccessToken
 - sspi/_SecPkgContext_AccessToken
 - PSecPkgContext_AccessToken
 - sspi/PSecPkgContext_AccessToken
 - SecPkgContext_AccessToken
 - sspi/SecPkgContext_AccessToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_AccessToken
---

# SecPkgContext_AccessToken structure


## -description

The <b>SecPkgContext_AccessToken</b> structure returns a handle to the access token for the current <a href="/windows/desktop/SecGloss/s-gly">security context</a>. The returned handle can be used by the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser">ImpersonateLoggedOnUser</a> and <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> functions. This structure is returned by the <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function.

## -struct-fields

### -field AccessToken

Pointer to a <b>void</b> that receives the handle to the access token that represents the authenticated user.

The returned  handle is not duplicated, so the calling process must not call <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> on the returned handle.

If the security context is for a server or is incomplete, the returned  handle may be <b>NULL</b>. Depending on the security package, <a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> may return SEC_E_NO_IMPERSONATION for these cases.