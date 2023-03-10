---
UID: NF:authz.AuthzInitializeContextFromToken
title: AuthzInitializeContextFromToken function (authz.h)
description: Initializes a client authorization context from a kernel token. The kernel token must have been opened for TOKEN_QUERY.
helpviewer_keywords: ["AuthzInitializeContextFromToken","AuthzInitializeContextFromToken function [Security]","_win32_authzinitializecontextfromtoken","authz/AuthzInitializeContextFromToken","security.authzinitializecontextfromtoken"]
old-location: security\authzinitializecontextfromtoken.htm
tech.root: security
ms.assetid: 75a7fb3f-6b3a-42ca-b467-f57baf6c60c6
ms.date: 12/05/2018
ms.keywords: AuthzInitializeContextFromToken, AuthzInitializeContextFromToken function [Security], _win32_authzinitializecontextfromtoken, authz/AuthzInitializeContextFromToken, security.authzinitializecontextfromtoken
req.header: authz.h
req.include-header: 
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
req.lib: Authz.lib
req.dll: Authz.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - AuthzInitializeContextFromToken
 - authz/AuthzInitializeContextFromToken
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
 - Ext-MS-Win-authz-context-l1-1-0.dll
api_name:
 - AuthzInitializeContextFromToken
---

# AuthzInitializeContextFromToken function


## -description

The <b>AuthzInitializeContextFromToken</b> function initializes a client authorization context from a kernel token. The kernel token must have been opened for TOKEN_QUERY. 

Starting with Windows Server 2012 and Windows 8, this function can also copy device groups, user claims, and device claims.

## -parameters

### -param Flags [in]

Reserved for future use.

### -param TokenHandle [in]

A handle to the client token used to initialize the <i>pAuthzClientContext</i> parameter. The token must have been opened with TOKEN_QUERY access.

### -param hAuthzResourceManager [in]

A handle to the resource manager that created this client context. This handle is stored in the client context structure.

### -param pExpirationTime [in, optional]

Expiration date and time of the token. If no value is passed, the token never expires. Expiration time is not currently enforced.

### -param Identifier [in]

Identifier that is specific to the resource manager. This parameter is not currently used.

### -param DynamicGroupArgs [in, optional]

A pointer to parameters to be passed to the callback function that computes dynamic groups.

### -param phAuthzClientContext [out]

A pointer to the <i>AuthzClientContext</i> handle returned. Call 
<a href="/windows/desktop/api/authz/nf-authz-authzfreecontext">AuthzFreeContext</a> when done with the client context.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function calls the  <a href="/windows/desktop/SecAuthZ/authzcomputegroupscallback">AuthzComputeGroupsCallback</a> callback function to add <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> to the newly created context.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzfreecontext">AuthzFreeContext</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>