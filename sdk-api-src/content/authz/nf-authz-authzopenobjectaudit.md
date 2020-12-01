---
UID: NF:authz.AuthzOpenObjectAudit
title: AuthzOpenObjectAudit function (authz.h)
description: Reads the system access control list (SACL) of the specified security descriptor and generates any appropriate audits specified by that SACL.
helpviewer_keywords: ["AuthzOpenObjectAudit","AuthzOpenObjectAudit function [Security]","_win32_authzopenobjectaudit","authz/AuthzOpenObjectAudit","security.authzopenobjectaudit"]
old-location: security\authzopenobjectaudit.htm
tech.root: security
ms.assetid: 39c6f0bc-72bf-4a82-b417-c0c5b2626344
ms.date: 12/05/2018
ms.keywords: AuthzOpenObjectAudit, AuthzOpenObjectAudit function [Security], _win32_authzopenobjectaudit, authz/AuthzOpenObjectAudit, security.authzopenobjectaudit
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
 - AuthzOpenObjectAudit
 - authz/AuthzOpenObjectAudit
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
 - AuthzOpenObjectAudit
---

# AuthzOpenObjectAudit function


## -description

The <b>AuthzOpenObjectAudit</b> function reads the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) of the specified security descriptor and generates any appropriate audits specified by that SACL.

## -parameters

### -param Flags [in]

Reserved for future use.

### -param hAuthzClientContext [in]

A handle to the client context of the object to open.

### -param pRequest [in]

A pointer to an 
<a href="/windows/desktop/api/authz/ns-authz-authz_access_request">AUTHZ_ACCESS_REQUEST</a> structure.

### -param hAuditEvent [in]

A handle to the audit event to use.

### -param pSecurityDescriptor [in]

A pointer to the 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure for the object.

### -param OptionalSecurityDescriptorArray [in]

A pointer to an array of <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structures.

### -param OptionalSecurityDescriptorCount [in]

The number of elements in <i>SecurityDescriptorArray</i>.

### -param pReply [in]

A pointer to an 
<a href="/windows/desktop/api/authz/ns-authz-authz_access_reply">AUTHZ_ACCESS_REPLY</a> structure.

## -returns

If the function succeeds, it returns a nonzero value. 

If the function fails, it returns a zero value. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>