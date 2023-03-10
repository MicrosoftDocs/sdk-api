---
UID: NF:authz.AuthzRegisterSecurityEventSource
title: AuthzRegisterSecurityEventSource function (authz.h)
description: Registers a security event source with the Local Security Authority (LSA).
helpviewer_keywords: ["AuthzRegisterSecurityEventSource","AuthzRegisterSecurityEventSource function [Security]","authz/AuthzRegisterSecurityEventSource","security.authzregistersecurityeventsource"]
old-location: security\authzregistersecurityeventsource.htm
tech.root: security
ms.assetid: 726e480d-1a34-4fd6-ac2d-876fa08f4eae
ms.date: 12/05/2018
ms.keywords: AuthzRegisterSecurityEventSource, AuthzRegisterSecurityEventSource function [Security], authz/AuthzRegisterSecurityEventSource, security.authzregistersecurityeventsource
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
 - AuthzRegisterSecurityEventSource
 - authz/AuthzRegisterSecurityEventSource
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
 - AuthzRegisterSecurityEventSource
---

# AuthzRegisterSecurityEventSource function


## -description

The <b>AuthzRegisterSecurityEventSource</b> function registers a security event source with the <a href="/windows/desktop/SecGloss/l-gly">Local Security Authority</a> (LSA).

## -parameters

### -param dwFlags [in]

This parameter is reserved for future use. Set this parameter to zero.

### -param szEventSourceName [in]

A pointer to the name of the security event source to register.

### -param phEventProvider [out]

A pointer to a handle to the registered security event source.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function  validates the <i>szEventSourceName</i> parameter  and sets up the appropriate structures and RPC connections to log events with that source name.  The validation is handled by an underlying call to an LSA API.  

The LSA API  verifies the following:

<ul>
<li>The caller has the  SeAuditPrivilege access right.</li>
<li>The event source is not already in use.</li>
<li>The event source is registered.</li>
<li>The calling application matches the executable image path in the event source registration, if one exists.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzunregistersecurityeventsource">AuthzUnregisterSecurityEventSource</a>