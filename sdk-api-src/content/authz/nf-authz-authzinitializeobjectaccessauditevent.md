---
UID: NF:authz.AuthzInitializeObjectAccessAuditEvent
title: AuthzInitializeObjectAccessAuditEvent function (authz.h)
description: Initializes auditing for an object.
helpviewer_keywords: ["AUTHZ_NO_ALLOC_STRINGS","AUTHZ_NO_FAILURE_AUDIT","AUTHZ_NO_SUCCESS_AUDIT","AuthzInitializeObjectAccessAuditEvent","AuthzInitializeObjectAccessAuditEvent function [Security]","_win32_authzinitializeobjectaccessauditevent","authz/AuthzInitializeObjectAccessAuditEvent","security.authzinitializeobjectaccessauditevent"]
old-location: security\authzinitializeobjectaccessauditevent.htm
tech.root: security
ms.assetid: cf79a92f-31e0-47cf-8990-4dbd46056a90
ms.date: 12/05/2018
ms.keywords: AUTHZ_NO_ALLOC_STRINGS, AUTHZ_NO_FAILURE_AUDIT, AUTHZ_NO_SUCCESS_AUDIT, AuthzInitializeObjectAccessAuditEvent, AuthzInitializeObjectAccessAuditEvent function [Security], _win32_authzinitializeobjectaccessauditevent, authz/AuthzInitializeObjectAccessAuditEvent, security.authzinitializeobjectaccessauditevent
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
 - AuthzInitializeObjectAccessAuditEvent
 - authz/AuthzInitializeObjectAccessAuditEvent
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
 - AuthzInitializeObjectAccessAuditEvent
---

# AuthzInitializeObjectAccessAuditEvent function


## -description

The <b>AuthzInitializeObjectAccessAuditEvent</b> function initializes auditing for an object.

## -parameters

### -param Flags [in]

Modifies the audit. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_SUCCESS_AUDIT"></a><a id="authz_no_success_audit"></a><dl>
<dt><b>AUTHZ_NO_SUCCESS_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
Disable generation of success audits.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_FAILURE_AUDIT"></a><a id="authz_no_failure_audit"></a><dl>
<dt><b>AUTHZ_NO_FAILURE_AUDIT</b></dt>
</dl>
</td>
<td width="60%">
Disable generation of failure audits.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_NO_ALLOC_STRINGS"></a><a id="authz_no_alloc_strings"></a><dl>
<dt><b>AUTHZ_NO_ALLOC_STRINGS</b></dt>
</dl>
</td>
<td width="60%">
Use pointers to the passed strings instead of allocating memory and copying the strings. The calling application must ensure that the passed memory stays valid during access checks.

</td>
</tr>
</table>

### -param hAuditEventType [in]

Reserved. This parameter should be set to <b>NULL</b>.

### -param szOperationType [in]

String that indicates the operation that is to be audited.

### -param szObjectType [in]

String that indicates the type of object being accessed.

### -param szObjectName [in]

String the indicates the name of the object being accessed.

### -param szAdditionalInfo [in]

String, defined by the Resource Manager, for additional audit information.

### -param phAuditEvent [out]

Pointer that receives an <b>AUTHZ_AUDIT_EVENT_HANDLE</b> structure.

### -param dwAdditionalParameterCount [in]

Must be set to zero.

### -param ...

Additional parameters.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>

