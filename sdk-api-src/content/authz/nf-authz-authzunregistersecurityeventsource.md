---
UID: NF:authz.AuthzUnregisterSecurityEventSource
title: AuthzUnregisterSecurityEventSource function (authz.h)
description: Unregisters a security event source with the Local Security Authority (LSA).
helpviewer_keywords: ["AuthzUnregisterSecurityEventSource","AuthzUnregisterSecurityEventSource function [Security]","authz/AuthzUnregisterSecurityEventSource","security.authzunregistersecurityeventsource"]
old-location: security\authzunregistersecurityeventsource.htm
tech.root: security
ms.assetid: 3ca3086b-f9c9-4305-aaf3-c41b5dba30ad
ms.date: 12/05/2018
ms.keywords: AuthzUnregisterSecurityEventSource, AuthzUnregisterSecurityEventSource function [Security], authz/AuthzUnregisterSecurityEventSource, security.authzunregistersecurityeventsource
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - AuthzUnregisterSecurityEventSource
 - authz/AuthzUnregisterSecurityEventSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Authz.dll
api_name:
 - AuthzUnregisterSecurityEventSource
---

# AuthzUnregisterSecurityEventSource function


## -description

The <b>AuthzUnregisterSecurityEventSource</b> function unregisters a security event source with the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA).

## -parameters

### -param dwFlags [in]

This parameter is reserved for future use. Set this parameter to zero.

### -param phEventProvider [in, out]

A pointer to a handle to the security event source to unregister.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function deallocates any resources and closes any RPC connections associated with a previous call to the <a href="/windows/desktop/api/authz/nf-authz-authzregistersecurityeventsource">AuthzRegisterSecurityEventSource</a> function.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzregistersecurityeventsource">AuthzRegisterSecurityEventSource</a>