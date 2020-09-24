---
UID: NF:authz.AuthzInitializeContextFromAuthzContext
title: AuthzInitializeContextFromAuthzContext function (authz.h)
description: Creates a new client context based on an existing client context.
helpviewer_keywords: ["AuthzInitializeContextFromAuthzContext","AuthzInitializeContextFromAuthzContext function [Security]","_win32_authzinitializecontextfromauthzcontext","authz/AuthzInitializeContextFromAuthzContext","security.authzinitializecontextfromauthzcontext"]
old-location: security\authzinitializecontextfromauthzcontext.htm
tech.root: security
ms.assetid: dac5e354-ee31-45e3-9eb8-8f3263161ad2
ms.date: 12/05/2018
ms.keywords: AuthzInitializeContextFromAuthzContext, AuthzInitializeContextFromAuthzContext function [Security], _win32_authzinitializecontextfromauthzcontext, authz/AuthzInitializeContextFromAuthzContext, security.authzinitializecontextfromauthzcontext
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
 - AuthzInitializeContextFromAuthzContext
 - authz/AuthzInitializeContextFromAuthzContext
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
 - AuthzInitializeContextFromAuthzContext
---

# AuthzInitializeContextFromAuthzContext function


## -description

The <b>AuthzInitializeContextFromAuthzContext</b> function creates a new client context based on an existing client context. 

Starting with Windows Server 2012 and Windows 8, this function also duplicates device groups, user claims, and device claims.

## -parameters

### -param Flags [in]

Reserved for future use.

### -param hAuthzClientContext [in]

The handle to an existing client context.

### -param pExpirationTime [in, optional]

Sets the time limit for how long the returned context structure is valid. If no value is passed, then the token never expires. Expiration time is not currently enforced.

### -param Identifier [in]

The specific identifier for the resource manager.

### -param DynamicGroupArgs [in]

A pointer to parameters to be passed to the callback function that computes dynamic groups. If the value is <b>NULL</b>, then the callback function is not called.

### -param phNewAuthzClientContext [out]

A pointer to the duplicated AUTHZ_CLIENT_CONTEXT_HANDLE handle. When you have finished using the handle, release it by calling the <a href="/windows/desktop/api/authz/nf-authz-authzfreecontext">AuthzFreeContext</a> function.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function calls the  <a href="/windows/desktop/SecAuthZ/authzcomputegroupscallback">AuthzComputeGroupsCallback</a> callback function to add <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> to the newly created context.

## -see-also

<a href="/windows/desktop/api/authz/ns-authz-authz_access_reply">AUTHZ_ACCESS_REPLY</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>