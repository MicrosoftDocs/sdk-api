---
UID: NF:authz.AuthzReportSecurityEventFromParams
title: AuthzReportSecurityEventFromParams function (authz.h)
description: Generates a security audit for a registered security event source by using the specified array of audit parameters.
helpviewer_keywords: ["AuthzReportSecurityEventFromParams","AuthzReportSecurityEventFromParams function [Security]","authz/AuthzReportSecurityEventFromParams","security.authzreportsecurityeventfromparams"]
old-location: security\authzreportsecurityeventfromparams.htm
tech.root: security
ms.assetid: ee5b598a-0a89-4b32-a9bc-e9c811573b08
ms.date: 12/05/2018
ms.keywords: AuthzReportSecurityEventFromParams, AuthzReportSecurityEventFromParams function [Security], authz/AuthzReportSecurityEventFromParams, security.authzreportsecurityeventfromparams
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
 - AuthzReportSecurityEventFromParams
 - authz/AuthzReportSecurityEventFromParams
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
 - AuthzReportSecurityEventFromParams
---

# AuthzReportSecurityEventFromParams function


## -description

The <b>AuthzReportSecurityEventFromParams</b> function generates a security audit for a registered security event source by using the specified array of audit parameters.

## -parameters

### -param dwFlags [in]

Reserved for future use.

### -param hEventProvider [in]

A handle to the registered security event source to use for the audit.

### -param dwAuditId [in]

The identifier of the audit.

### -param pUserSid [in, optional]

A pointer to the <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that will be listed as the source of the audit in the event log.

### -param pParams [in]

An array of audit parameters.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzregistersecurityeventsource">AuthzRegisterSecurityEventSource</a>



<a href="/windows/desktop/api/authz/nf-authz-authzreportsecurityevent">AuthzReportSecurityEvent</a>