---
UID: NF:winbase.AddConditionalAce
title: AddConditionalAce function (winbase.h)
description: Adds a conditional access control entry (ACE) to the specified access control list (ACL).
helpviewer_keywords: ["ACCESS_ALLOWED_CALLBACK_ACE_TYPE","ACCESS_DENIED_CALLBACK_ACE_TYPE","AddConditionalAce","AddConditionalAce function [Security]","CONTAINER_INHERIT_ACE","INHERITED_ACE","INHERIT_ONLY_ACE","NO_PROPAGATE_INHERIT_ACE","OBJECT_INHERIT_ACE","SYSTEM_AUDIT_CALLBACK_ACE_TYPE","security.addconditionalace","winbase/AddConditionalAce"]
old-location: security\addconditionalace.htm
tech.root: security
ms.assetid: 89f038be-d15c-4c0b-8145-ba531bdf87ce
ms.date: 12/05/2018
ms.keywords: ACCESS_ALLOWED_CALLBACK_ACE_TYPE, ACCESS_DENIED_CALLBACK_ACE_TYPE, AddConditionalAce, AddConditionalAce function [Security], CONTAINER_INHERIT_ACE, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, SYSTEM_AUDIT_CALLBACK_ACE_TYPE, security.addconditionalace, winbase/AddConditionalAce
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - AddConditionalAce
 - winbase/AddConditionalAce
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - AddConditionalAce
---

# AddConditionalAce function


## -description

The <b>AddConditionalAce</b> function adds a conditional  <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) to the specified <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL). A conditional ACE specifies a logical condition that is evaluated during access checks.

## -parameters

### -param pAcl [in, out]

A pointer to an 
ACL. This function adds an ACE to this ACL.

The value of this parameter cannot be <b>NULL</b>.

### -param dwAceRevision [in]

Specifies the revision level of the ACL being modified. This value can be ACL_REVISION or ACL_REVISION_DS. 
      Use ACL_REVISION_DS if the ACL contains object-specific ACEs.

### -param AceFlags [in]

A set of bit flags that control ACE inheritance. The function sets these flags in the <b>AceFlags</b> member of the 
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
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object to which the ACL is assigned, but it can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
</dl>
</td>
<td width="60%">
Indicates an inherited ACE. This flag allows operations that change the security on a tree of objects to modify inherited ACEs while not changing ACEs that were directly applied to the object.

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
</table>

### -param AceType [in]

The type of the ACE.

This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_ALLOWED_CALLBACK_ACE_TYPE"></a><a id="access_allowed_callback_ace_type"></a><dl>
<dt><b>ACCESS_ALLOWED_CALLBACK_ACE_TYPE</b></dt>
<dt>0x9</dt>
</dl>
</td>
<td width="60%">
Access-allowed callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_callback_ace">ACCESS_ALLOWED_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_DENIED_CALLBACK_ACE_TYPE"></a><a id="access_denied_callback_ace_type"></a><dl>
<dt><b>ACCESS_DENIED_CALLBACK_ACE_TYPE</b></dt>
<dt>0xA</dt>
</dl>
</td>
<td width="60%">
Access-denied callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_callback_ace">ACCESS_DENIED_CALLBACK_ACE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_AUDIT_CALLBACK_ACE_TYPE"></a><a id="system_audit_callback_ace_type"></a><dl>
<dt><b>SYSTEM_AUDIT_CALLBACK_ACE_TYPE</b></dt>
<dt>0xD</dt>
</dl>
</td>
<td width="60%">
System audit callback ACE that uses the 
<a href="/windows/desktop/api/winnt/ns-winnt-system_audit_callback_ace">SYSTEM_AUDIT_CALLBACK_ACE</a> structure.

</td>
</tr>
</table>

### -param AccessMask [in]

Specifies the mask of access rights to be granted to the specified SID.

### -param pSid [in]

A pointer to the 
SID  that represents a user, group, or logon account being granted access.

### -param ConditionStr [in]

A string that specifies the conditional statement to be evaluated for the ACE.

### -param ReturnLength [out]

The size, in bytes, of the ACL. If the buffer specified by the <i>pACL</i> parameter is not of sufficient size, the value of this parameter is the required size.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the <i>pAcl</i> buffer.

</td>
</tr>
</table>