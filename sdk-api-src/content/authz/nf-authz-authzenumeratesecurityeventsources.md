---
UID: NF:authz.AuthzEnumerateSecurityEventSources
title: AuthzEnumerateSecurityEventSources function (authz.h)
description: Retrieves the registered security event sources that are not installed by default.
helpviewer_keywords: ["AuthzEnumerateSecurityEventSources","AuthzEnumerateSecurityEventSources function [Security]","authz/AuthzEnumerateSecurityEventSources","security.authzenumeratesecurityeventsources"]
old-location: security\authzenumeratesecurityeventsources.htm
tech.root: security
ms.assetid: 2a20ccc9-f2ac-41e4-9d86-745004775e67
ms.date: 12/05/2018
ms.keywords: AuthzEnumerateSecurityEventSources, AuthzEnumerateSecurityEventSources function [Security], authz/AuthzEnumerateSecurityEventSources, security.authzenumeratesecurityeventsources
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
 - AuthzEnumerateSecurityEventSources
 - authz/AuthzEnumerateSecurityEventSources
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
 - AuthzEnumerateSecurityEventSources
---

# AuthzEnumerateSecurityEventSources function


## -description

The <b>AuthzEnumerateSecurityEventSources</b> function retrieves the registered security event sources that are not installed by default.

## -parameters

### -param dwFlags [in]

Reserved for future use; set this parameter to zero.

### -param Buffer [out]

A pointer to an array of <a href="/windows/desktop/api/authz/ns-authz-authz_source_schema_registration">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a> structures that returns the registered security event sources.

### -param pdwCount [out]

A pointer to a  variable that receives the number of event sources found.

### -param pdwLength [in, out]

A pointer to a variable that specifies the length of the <i>Buffer</i> parameter in bytes. On output, this parameter receives the number of bytes used or required.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/authz/ns-authz-authz_source_schema_registration">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a>