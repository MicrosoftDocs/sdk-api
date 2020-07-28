---
UID: NF:ntsecapi.AuditSetPerUserPolicy
title: AuditSetPerUserPolicy function (ntsecapi.h)
description: Sets per-user audit policy in one or more audit subcategories for the specified principal.
helpviewer_keywords: ["AuditSetPerUserPolicy","AuditSetPerUserPolicy function [Security]","ntsecapi/AuditSetPerUserPolicy","security.auditsetperuserpolicy_func"]
old-location: security\auditsetperuserpolicy_func.htm
tech.root: security
ms.assetid: a6cef640-5658-4c13-96fb-a664d2a61b57
ms.date: 12/05/2018
ms.keywords: AuditSetPerUserPolicy, AuditSetPerUserPolicy function [Security], ntsecapi/AuditSetPerUserPolicy, security.auditsetperuserpolicy_func
f1_keywords:
- ntsecapi/AuditSetPerUserPolicy
dev_langs:
- c++
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
- AuditSetPerUserPolicy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AuditSetPerUserPolicy function


## -description


The <b>AuditSetPerUserPolicy</b> function sets per-user audit policy in one or more audit subcategories for the specified principal. 


## -parameters




### -param pSid [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure associated with the principal for which to set  audit policy. Per-user policy for group SIDs is not currently supported.


### -param pAuditPolicy [in]

A pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ns-ntsecapi-audit_policy_information">AUDIT_POLICY_INFORMATION</a> structures. Each structure specifies per-user audit policy for one audit subcategory.

The <b>AuditCategoryGuid</b> member of these structures is ignored.


### -param dwPolicyCount [in]

The number of elements in the <i>pAuditPolicy</i> array.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. <b>GetLastError</b> may return one of the following error codes defined in WinError.h.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_USER</b></dt>
<dt>1317</dt>
</dl>
</td>
<td width="60%">
The <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure specified by the <i>pSID</i> parameter is not associated with an existing user.

</td>
</tr>
</table>
 




## -remarks



To successfully call this function, the caller must have <b>SeSecurityPrivilege</b> or have <b>AUDIT_SET_USER_POLICY</b> access on the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">Audit security object</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-auditqueryperuserpolicy">AuditQueryPerUserPolicy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-auditquerysystempolicy">AuditQuerySystemPolicy</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-auditsetsystempolicy">AuditSetSystemPolicy</a>
 

 

