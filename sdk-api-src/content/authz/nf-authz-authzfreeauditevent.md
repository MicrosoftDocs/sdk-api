---
UID: NF:authz.AuthzFreeAuditEvent
title: AuthzFreeAuditEvent function (authz.h)
description: Frees the structure allocated by the AuthzInitializeObjectAccessAuditEvent function.
helpviewer_keywords: ["AuthzFreeAuditEvent","AuthzFreeAuditEvent function [Security]","_win32_authzfreeauditevent","authz/AuthzFreeAuditEvent","security.authzfreeauditevent"]
old-location: security\authzfreeauditevent.htm
tech.root: security
ms.assetid: e2980ef7-45dd-47c7-ba4d-f36b52bbd7dc
ms.date: 12/05/2018
ms.keywords: AuthzFreeAuditEvent, AuthzFreeAuditEvent function [Security], _win32_authzfreeauditevent, authz/AuthzFreeAuditEvent, security.authzfreeauditevent
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
 - AuthzFreeAuditEvent
 - authz/AuthzFreeAuditEvent
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
 - AuthzFreeAuditEvent
---

# AuthzFreeAuditEvent function


## -description

The <b>AuthzFreeAuditEvent</b> function frees the  structure allocated by the 
<a href="/windows/desktop/api/authz/nf-authz-authzinitializeobjectaccessauditevent">AuthzInitializeObjectAccessAuditEvent</a> function.

## -parameters

### -param hAuditEvent [in]

A pointer to the <b>AUTHZ_AUDIT_EVENT_HANDLE</b> structure to be freed.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzinitializeobjectaccessauditevent">AuthzInitializeObjectAccessAuditEvent</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>