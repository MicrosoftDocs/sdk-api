---
UID: NF:sspi.QuerySecurityContextToken
title: QuerySecurityContextToken function (sspi.h)
description: Obtains the access token for a client security context and uses it directly.
helpviewer_keywords: ["QuerySecurityContextToken","QuerySecurityContextToken function [Security]","_ssp_querysecuritycontexttoken","security.querysecuritycontexttoken","sspi/QuerySecurityContextToken"]
old-location: security\querysecuritycontexttoken.htm
tech.root: security
ms.assetid: 5dc23608-9ce3-4fee-8161-2e409cef4063
ms.date: 12/05/2018
ms.keywords: QuerySecurityContextToken, QuerySecurityContextToken function [Security], _ssp_querysecuritycontexttoken, security.querysecuritycontexttoken, sspi/QuerySecurityContextToken
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QuerySecurityContextToken
 - sspi/QuerySecurityContextToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - QuerySecurityContextToken
---

# QuerySecurityContextToken function


## -description

Obtains the <a href="/windows/desktop/SecGloss/a-gly">access token</a> for a client <a href="/windows/desktop/SecGloss/s-gly">security context</a> and uses it directly.

## -parameters

### -param phContext [in]

Handle of the context to query.

### -param Token [out]

Returned handle to the access token.

## -returns

If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns a nonzero error code. One possible error code return is SEC_E_INVALID_HANDLE.

## -remarks

This function is called by a server application to control impersonation outside the SSPI layer, such as when launching a child process. The handle returned must be closed with <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> when the handle is no longer needed.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>