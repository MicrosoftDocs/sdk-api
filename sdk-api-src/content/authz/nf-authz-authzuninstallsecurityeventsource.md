---
UID: NF:authz.AuthzUninstallSecurityEventSource
title: AuthzUninstallSecurityEventSource function (authz.h)
description: Removes the specified source from the list of valid security event sources.
helpviewer_keywords: ["AuthzUninstallSecurityEventSource","AuthzUninstallSecurityEventSource function [Security]","authz/AuthzUninstallSecurityEventSource","security.authzuninstallsecurityeventsource"]
old-location: security\authzuninstallsecurityeventsource.htm
tech.root: security
ms.assetid: 495157da-d4ed-42ff-bcb4-5c07ab9ec0e6
ms.date: 12/05/2018
ms.keywords: AuthzUninstallSecurityEventSource, AuthzUninstallSecurityEventSource function [Security], authz/AuthzUninstallSecurityEventSource, security.authzuninstallsecurityeventsource
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
 - AuthzUninstallSecurityEventSource
 - authz/AuthzUninstallSecurityEventSource
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
 - AuthzUninstallSecurityEventSource
---

# AuthzUninstallSecurityEventSource function


## -description

The <b>AuthzUninstallSecurityEventSource</b> function removes the specified source from the list of valid security event sources.

## -parameters

### -param dwFlags [in]

Reserved for future use; set this parameter to zero.

### -param szEventSourceName [in]

Name of the source to remove from the list of valid security event sources. This corresponds to  the <b>szEventSourceName</b> member of the <a href="/windows/desktop/api/authz/ns-authz-authz_source_schema_registration">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a> structure that defines the source.

This function removes the source information from the registry. For more information about the registry keys and values affected, see the <a href="/windows/desktop/api/authz/nf-authz-authzinstallsecurityeventsource">AuthzInstallSecurityEventSource</a> function.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/authz/ns-authz-authz_source_schema_registration">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a>



<a href="/windows/desktop/api/authz/nf-authz-authzinstallsecurityeventsource">AuthzInstallSecurityEventSource</a>