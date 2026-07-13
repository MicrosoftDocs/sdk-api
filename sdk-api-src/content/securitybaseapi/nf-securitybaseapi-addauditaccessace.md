---
UID: NF:securitybaseapi.AddAuditAccessAce
title: AddAuditAccessAce function (securitybaseapi.h)
description: Adds a system-audit access control entry (ACE) to a system access control list (ACL). The access of a specified security identifier (SID) is audited.
helpviewer_keywords: ["AddAuditAccessAce","AddAuditAccessAce function [Security]","_win32_addauditaccessace","security.addauditaccessace","securitybaseapi/AddAuditAccessAce"]
old-location: security\addauditaccessace.htm
tech.root: security
ms.assetid: 34f22aea-9cde-411e-b2d5-bfcd3bfe325d
ms.date: 12/05/2018
ms.keywords: AddAuditAccessAce, AddAuditAccessAce function [Security], _win32_addauditaccessace, security.addauditaccessace, securitybaseapi/AddAuditAccessAce
req.header: securitybaseapi.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddAuditAccessAce
 - securitybaseapi/AddAuditAccessAce
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AddAuditAccessAce
---

# AddAuditAccessAce function


## -description

The <b>AddAuditAccessAce</b> function adds a system-audit <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) to a system <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL). The access of a specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) is audited.

To control whether the new ACE can be inherited by child objects, use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessaceex">AddAuditAccessAceEx</a> function.

## -parameters

### -param pAcl [in, out]

A pointer to an 
ACL. This function adds a system-audit ACE to this ACL. The ACE is in the form of a 
<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a> structure.

### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. 


This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the ACL contains object-specific ACEs.

### -param dwAccessMask [in]

Specifies the mask of access rights to be audited for the specified SID.

### -param pSid [in]

A pointer to the 
SID representing the <a href="/windows/desktop/SecGloss/p-gly">process</a> whose access is being audited.

### -param bAuditSuccess [in]

Specifies whether successful access attempts are to be audited. Set this flag to <b>TRUE</b> to enable auditing; otherwise, set it to <b>FALSE</b>.

### -param bAuditFailure [in]

Specifies whether unsuccessful access attempts are to be audited. Set this flag to <b>TRUE</b> to enable auditing; otherwise, set it to <b>FALSE</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALLOTTED_SPACE_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the ACL. A larger ACL buffer is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ACL</b></dt>
</dl>
</td>
<td width="60%">
The specified ACL is not properly formed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The specified SID is not structurally valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_REVISION_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The specified revision is not known or is incompatible with that of the ACL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The ACE was successfully added.

</td>
</tr>
</table>

## -remarks

The 
<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure placed in the ACE by the <b>AddAuditAccessAce</b> function specifies a type and size, but provides no ACE flags.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addace">AddAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessaceex">AddAuditAccessAceEx</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-deleteace">DeleteAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getace">GetAce</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a>