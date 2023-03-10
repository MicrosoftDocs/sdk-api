---
UID: NF:ntsecapi.AuditSetSystemPolicy
title: AuditSetSystemPolicy function (ntsecapi.h)
description: Sets system audit policy for one or more audit-policy subcategories.
helpviewer_keywords: ["AuditSetSystemPolicy","AuditSetSystemPolicy function [Security]","ntsecapi/AuditSetSystemPolicy","security.auditsetsystempolicy_func"]
old-location: security\auditsetsystempolicy_func.htm
tech.root: security
ms.assetid: 9692ebe3-a676-45bb-a58d-b3fdbb1bbc2a
ms.date: 12/05/2018
ms.keywords: AuditSetSystemPolicy, AuditSetSystemPolicy function [Security], ntsecapi/AuditSetSystemPolicy, security.auditsetsystempolicy_func
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
 - AuditSetSystemPolicy
 - ntsecapi/AuditSetSystemPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-audit-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-audit-l1-1-1.dll
api_name:
 - AuditSetSystemPolicy
---

# AuditSetSystemPolicy function


## -description

The <b>AuditSetSystemPolicy</b> function sets system audit policy for one or more audit-policy subcategories.

## -parameters

### -param pAuditPolicy [in]

A pointer to an array of <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-audit_policy_information">AUDIT_POLICY_INFORMATION</a> structures. Each structure specifies system audit policy for one audit-policy subcategory.

The <b>AuditCategoryGuid</b> member of these structures is ignored.

### -param dwPolicyCount [in]

The number of elements in the <i>pAuditPolicy</i> array.

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

To successfully call this function, the caller must have <b>SeSecurityPrivilege</b> or have <b>AUDIT_SET_SYSTEM_POLICY</b> access on the <a href="/windows/desktop/SecGloss/a-gly">Audit security object</a>.

## -see-also

<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditquerysystempolicy">AuditQuerySystemPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetperuserpolicy">AuditSetPerUserPolicy</a>