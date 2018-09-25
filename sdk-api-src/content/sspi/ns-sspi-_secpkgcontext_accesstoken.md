---
UID: NS:sspi._SecPkgContext_AccessToken
title: "_SecPkgContext_AccessToken"
author: windows-sdk-content
description: Returns a handle to the access token for the current security context.
old-location: security\secpkgcontext_accesstoken.htm
tech.root: secauthn
ms.assetid: 4dc11cbd-7f28-4cb9-aaea-6e5a89ac91f0
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: "*PSecPkgContext_AccessToken, PSecPkgContext_AccessToken, PSecPkgContext_AccessToken structure pointer [Security], SecPkgContext_AccessToken, SecPkgContext_AccessToken structure [Security], _SecPkgContext_AccessToken, security.secpkgcontext_accesstoken, sspi/PSecPkgContext_AccessToken, sspi/SecPkgContext_AccessToken"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecPkgContext_AccessToken
product: Windows
targetos: Windows
req.typenames: SecPkgContext_AccessToken, *PSecPkgContext_AccessToken
req.redist: 
---

# _SecPkgContext_AccessToken structure


## -description


The <b>SecPkgContext_AccessToken</b> structure returns a handle to the access token for the current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. The returned handle can be used by the <a href="https://msdn.microsoft.com/cf5c31ae-6749-45c2-888f-697060cc8c75">ImpersonateLoggedOnUser</a> and <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> functions. This structure is returned by the <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function.


## -struct-fields




### -field AccessToken

Pointer to a <b>void</b> that receives the handle to the access token that represents the authenticated user.

The returned  handle is not duplicated, so the calling process must not call <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> on the returned handle.

If the security context is for a server or is incomplete, the returned  handle may be <b>NULL</b>. Depending on the security package, <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> may return SEC_E_NO_IMPERSONATION for these cases.

