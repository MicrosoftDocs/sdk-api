---
UID: NF:securitybaseapi.AddAuditAccessObjectAce
title: AddAuditAccessObjectAce function (securitybaseapi.h)
description: Adds a system-audit access control entry (ACE) to the end of a system access control list (SACL). (AddAuditAccessObjectAce)
helpviewer_keywords: ["AddAuditAccessObjectAce","AddAuditAccessObjectAce function [Security]","CONTAINER_INHERIT_ACE","FAILED_ACCESS_ACE_FLAG","INHERITED_ACE","INHERIT_ONLY_ACE","NO_PROPAGATE_INHERIT_ACE","OBJECT_INHERIT_ACE","SUCCESSFUL_ACCESS_ACE_FLAG","_win32_addauditaccessobjectace","security.addauditaccessobjectace","securitybaseapi/AddAuditAccessObjectAce"]
old-location: security\addauditaccessobjectace.htm
tech.root: security
ms.assetid: be852a0c-9d96-4b29-b5f9-d9c41d838c12
ms.date: 12/05/2018
ms.keywords: AddAuditAccessObjectAce, AddAuditAccessObjectAce function [Security], CONTAINER_INHERIT_ACE, FAILED_ACCESS_ACE_FLAG, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, SUCCESSFUL_ACCESS_ACE_FLAG, _win32_addauditaccessobjectace, security.addauditaccessobjectace, securitybaseapi/AddAuditAccessObjectAce
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
 - AddAuditAccessObjectAce
 - securitybaseapi/AddAuditAccessObjectAce
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
 - AddAuditAccessObjectAce
---

# AddAuditAccessObjectAce function


## -description

The <b>AddAuditAccessObjectAce</b> function adds a system-audit <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) to the end of a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL). The new ACE can audit access to an object, or to a property set or property on an object. You can also use <b>AddAuditAccessObjectAce</b> to add an ACE that only a specified type of child object can inherit.

## -parameters

### -param pAcl [in, out]

A pointer to a SACL. The <b>AddAuditAccessObjectAce</b> function adds a system-audit ACE to the end of this SACL. The ACE is in the form of a 
<a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace">SYSTEM_AUDIT_OBJECT_ACE</a> structure.

### -param dwAceRevision [in]

Specifies the revision level of the SACL being modified. This value must be ACL_REVISION_DS. If the SACL's revision level is lower than ACL_REVISION_DS, the function changes it to ACL_REVISION_DS.

### -param AceFlags [in]

A set of bit flags that control ACE inheritance and the type of access attempts to audit. The function sets these flags in the <b>AceFlags</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure of the new ACE. This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONTAINER_INHERIT_ACE"></a><a id="container_inherit_ace"></a><dl>
<dt><b>CONTAINER_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by container objects.

</td>
</tr>
<tr>
<td width="40%"><a id="FAILED_ACCESS_ACE_FLAG"></a><a id="failed_access_ace_flag"></a><dl>
<dt><b>FAILED_ACCESS_ACE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If you set this flag or specify <b>TRUE</b> for the <i>bAuditFailure</i> parameter, failed attempts to use the specified access rights cause the system to generate an audit record in the security event log.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object to which the <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) is assigned, but it can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an inherited ACE. This flag allows operations that change the security on a tree of objects to modify inherited ACEs, while not changing ACEs that were directly applied to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE bits are not propagated to an inherited ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by noncontainer objects.

</td>
</tr>
<tr>
<td width="40%"><a id="SUCCESSFUL_ACCESS_ACE_FLAG"></a><a id="successful_access_ace_flag"></a><dl>
<dt><b>SUCCESSFUL_ACCESS_ACE_FLAG</b></dt>
</dl>
</td>
<td width="60%">
If you set this flag or specify <b>TRUE</b> for the <i>bAuditSuccess</i> parameter, successful uses of the specified access rights cause the system to generate an audit record in the security event log.

</td>
</tr>
</table>

### -param AccessMask [in]

An 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> that specifies the access rights that the new ACE audits for the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

### -param ObjectTypeGuid [in, optional]

A pointer to a 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of object, property set, or property protected by the new ACE. If this parameter is <b>NULL</b>, the new ACE protects the object to which the ACL is assigned.

### -param InheritedObjectTypeGuid [in, optional]

A pointer to a <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of object that can inherit the new ACE. If this parameter is non-<b>NULL</b>, only the specified object type can inherit the ACE. If <b>NULL</b>, any type of child object can inherit the ACE. In either case, inheritance is also controlled by the value of the <i>AceFlags</i> parameter, as well as by any protection against inheritance placed on the child objects.

### -param pSid [in]

A pointer to a 
SID that identifies the user, group, or <a href="/windows/desktop/SecGloss/l-gly">logon session</a> for which the new ACE audits access.

### -param bAuditSuccess [in]

Specifies whether successful uses of the specified access rights cause the system to generate an audit record in the security event log. If this flag is <b>TRUE</b> or if the <i>AceFlags</i> parameter specifies the SUCCESSFUL_ACCESS_ACE_FLAG flag, the system records successful access attempts; otherwise, it does not.

### -param bAuditFailure [in]

Specifies whether failed attempts to use the specified access rights cause the system to generate an audit record in the security event log. If this flag is <b>TRUE</b> or if the <i>AceFlags</i> parameter specifies the FAILED_ACCESS_ACE_FLAG flag, the system records failed access attempts; otherwise, it does not.

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
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <i>AceFlags</i> parameter is not valid.

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

If both <i>ObjectTypeGuid</i> and <i>InheritedObjectTypeGuid</i> are <b>NULL</b>, use the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessaceex">AddAuditAccessAceEx</a> function rather than <b>AddAuditAccessObjectAce</b>. This is suggested because a 
<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a> is smaller and more efficient than a 
<a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace">SYSTEM_AUDIT_OBJECT_ACE</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>



<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace">AddAccessAllowedObjectAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace">AddAccessDeniedObjectAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessaceex">AddAuditAccessAceEx</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_ace">SYSTEM_AUDIT_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace">SYSTEM_AUDIT_OBJECT_ACE</a>
