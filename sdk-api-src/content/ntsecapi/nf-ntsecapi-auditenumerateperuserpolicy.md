---
UID: NF:ntsecapi.AuditEnumeratePerUserPolicy
title: AuditEnumeratePerUserPolicy function (ntsecapi.h)
description: Enumerates users for whom per-user auditing policy is specified.
helpviewer_keywords: ["AuditEnumeratePerUserPolicy","AuditEnumeratePerUserPolicy function [Security]","ntsecapi/AuditEnumeratePerUserPolicy","security.auditenumerateperuserpolicy_func"]
old-location: security\auditenumerateperuserpolicy_func.htm
tech.root: security
ms.assetid: 4b13f021-ba08-4eb8-9c7a-0512992ef272
ms.date: 12/05/2018
ms.keywords: AuditEnumeratePerUserPolicy, AuditEnumeratePerUserPolicy function [Security], ntsecapi/AuditEnumeratePerUserPolicy, security.auditenumerateperuserpolicy_func
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AuditEnumeratePerUserPolicy
 - ntsecapi/AuditEnumeratePerUserPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-audit-l1-1-1.dll
 - sechost.dll
api_name:
 - AuditEnumeratePerUserPolicy
---

# AuditEnumeratePerUserPolicy function


## -description

The <b>AuditEnumeratePerUserPolicy</b> function enumerates users for whom per-user auditing policy is specified.

## -parameters

### -param ppAuditSidArray [out]

A pointer to a single buffer that contains both an array of pointers to <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-policy_audit_sid_array">POLICY_AUDIT_SID_ARRAY</a> structures and the structures themselves. The <b>POLICY_AUDIT_SID_ARRAY</b> structures specify the users for whom per-user audit policy is specified. 

When you have finished using this buffer, free it by calling the <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditfree">AuditFree</a> function.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> may return one of the following error codes defined in WinError.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The caller does not have the privilege or access rights necessary to call this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87</dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>

## -remarks

To successfully call this function, the caller must have <b>SeSecurityPrivilege</b> or have <b>AUDIT_ENUMERATE_USERS</b> access on the <a href="/windows/desktop/SecGloss/a-gly">Audit security object</a>.