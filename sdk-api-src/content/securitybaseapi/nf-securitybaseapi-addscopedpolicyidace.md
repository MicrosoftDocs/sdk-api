---
UID: NF:securitybaseapi.AddScopedPolicyIDAce
title: AddScopedPolicyIDAce function (securitybaseapi.h)
description: Adds a SYSTEM_SCOPED_POLICY_ID_ACEaccess control entry (ACE) to the end of a system access control list (SACL).
helpviewer_keywords: ["AddScopedPolicyIDAce","AddScopedPolicyIDAce function [Security]","CONTAINER_INHERIT_ACE","INHERITED_ACE","INHERIT_ONLY_ACE","NO_PROPAGATE_INHERIT_ACE","OBJECT_INHERIT_ACE","security.addscopedpolicyidace","securitybaseapi/AddScopedPolicyIDAce"]
old-location: security\addscopedpolicyidace.htm
tech.root: security
ms.assetid: 30AA5730-566C-4B02-A904-5A38237EE8E3
ms.date: 12/05/2018
ms.keywords: AddScopedPolicyIDAce, AddScopedPolicyIDAce function [Security], CONTAINER_INHERIT_ACE, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, security.addscopedpolicyidace, securitybaseapi/AddScopedPolicyIDAce
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddScopedPolicyIDAce
 - securitybaseapi/AddScopedPolicyIDAce
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Kernel32.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - AddScopedPolicyIDAce
---

# AddScopedPolicyIDAce function


## -description

The <b>AddScopedPolicyIDAce</b> function adds a <a href="/windows/desktop/api/winnt/ns-winnt-system_scoped_policy_id_ace">SYSTEM_SCOPED_POLICY_ID_ACE</a> <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) to the end of a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL). A <b>SYSTEM_SCOPED_POLICY_ID_ACE</b> structure specifies a central access policy (CAP) to be associated with the resource and can be  used during access checks. The set of standard access rights are defined in the <a href="/windows/desktop/SecAuthZ/standard-access-rights">Standard Access Rights</a> topic.

## -parameters

### -param pAcl [in, out]

A pointer to an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL). This function adds an ACE to this ACL. The value of this parameter cannot be <b>NULL</b>.

### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the ACL contains object-specific ACEs.

### -param AceFlags [in]

A set of bit flags that control ACE inheritance. The function sets these flags in the <b>AceFlags</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure of the new ACE.

For consistency with the Windows 8 Advanced File Permissions UI, applications should specify the CONTAINER_INHERIT_ACE and OBJECT_INHERIT_ACE flags in the <i>AceFlags</i> parameter.


This parameter can be a combination of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONTAINER_INHERIT_ACE"></a><a id="container_inherit_ace"></a><dl>
<dt><b>CONTAINER_INHERIT_ACE</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by the container objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
<dt>8 (0x8)</dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object the ACE is assigned to, but it can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
Indicates an inherited ACE. This flag allows operations that change the security on a tree of objects to modify inherited ACEs while not changing ACEs that were directly applied to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
The OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE bits are not propagated to an inherited ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by non-container objects.

</td>
</tr>
</table>

### -param AccessMask [in]

Must be zero for Windows 8 and Windows Server 2012.

### -param pSid [in]

A pointer to the SID (S-1-17-*) that identifies the Central Access Policy to be associated with the resource.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecAuthZ/standard-access-rights">Standard Access Rights</a>