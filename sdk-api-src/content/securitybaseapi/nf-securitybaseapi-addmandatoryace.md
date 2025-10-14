---
UID: NF:securitybaseapi.AddMandatoryAce
title: AddMandatoryAce function (securitybaseapi.h)
description: Adds a SYSTEM_MANDATORY_LABEL_ACE access control entry (ACE) to the specified system access control list (SACL).
helpviewer_keywords: ["ACL_REVISION","ACL_REVISION_DS","AddMandatoryAce","AddMandatoryAce function [Security]","CONTAINER_INHERIT_ACE","INHERITED_ACE","INHERIT_ONLY_ACE","NO_PROPAGATE_INHERIT_ACE","OBJECT_INHERIT_ACE","SYSTEM_MANDATORY_LABEL_NO_EXECUTE_UP","SYSTEM_MANDATORY_LABEL_NO_READ_UP","SYSTEM_MANDATORY_LABEL_NO_WRITE_UP","security.addmandatoryace","securitybaseapi/AddMandatoryAce","winbase/AddMandatoryAce"]
old-location: security\addmandatoryace.htm
tech.root: security
ms.assetid: 22c8f384-fdb7-4d5a-8854-d9fd25cd351e
ms.date: 12/05/2018
ms.keywords: ACL_REVISION, ACL_REVISION_DS, AddMandatoryAce, AddMandatoryAce function [Security], CONTAINER_INHERIT_ACE, INHERITED_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, SYSTEM_MANDATORY_LABEL_NO_EXECUTE_UP, SYSTEM_MANDATORY_LABEL_NO_READ_UP, SYSTEM_MANDATORY_LABEL_NO_WRITE_UP, security.addmandatoryace, securitybaseapi/AddMandatoryAce, winbase/AddMandatoryAce
req.header: securitybaseapi.h
req.include-header: WinBase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - AddMandatoryAce
 - securitybaseapi/AddMandatoryAce
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
 - AddMandatoryAce
---

# AddMandatoryAce function


## -description

 The <b>AddMandatoryAce</b> function adds a <a href="/windows/desktop/api/winnt/ns-winnt-system_mandatory_label_ace">SYSTEM_MANDATORY_LABEL_ACE</a> <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) to the specified <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL).

## -parameters

### -param pAcl [in, out]

A pointer to an 
 SACL. This function adds a mandatory ACE to the end of this SACL. The ACE is in the form of a 
<a href="/windows/desktop/api/winnt/ns-winnt-system_mandatory_label_ace">SYSTEM_MANDATORY_LABEL_ACE</a> structure.

### -param dwAceRevision [in]

The revision level of the SACL being modified. 
This value can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACL_REVISION"></a><a id="acl_revision"></a><dl>
<dt><b>ACL_REVISION</b></dt>
</dl>
</td>
<td width="60%">
The SACL does not contain object-specific ACEs.

</td>
</tr>
<tr>
<td width="40%"><a id="ACL_REVISION_DS"></a><a id="acl_revision_ds"></a><dl>
<dt><b>ACL_REVISION_DS</b></dt>
</dl>
</td>
<td width="60%">
The SACL contains object-specified ACEs.

</td>
</tr>
</table>

### -param AceFlags [in]

A set of bit flags that control ACE inheritance. This function sets these flags in the <b>AceFlags</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure of the new ACE.

This parameter can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by noncontainer objects.

</td>
</tr>
<tr>
<td width="40%"><a id="CONTAINER_INHERIT_ACE"></a><a id="container_inherit_ace"></a><dl>
<dt><b>CONTAINER_INHERIT_ACE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The ACE is inherited by container objects.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The <b>OBJECT_INHERIT_ACE</b> and <b>CONTAINER_INHERIT_ACE</b> bits are not propagated to an inherited ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the object to which the SACL is assigned, but the ACE can be inherited by child objects.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERITED_ACE"></a><a id="inherited_ace"></a><dl>
<dt><b>INHERITED_ACE</b></dt>
<dt>0x10</dt>
</dl>
</td>
<td width="60%">
The ACE is inherited. Operations that change the security on a tree of objects may modify inherited ACEs without changing ACEs that were directly applied to the object.

</td>
</tr>
</table>

### -param MandatoryPolicy [in]

The access policy for principals with a mandatory integrity level lower than the object associated with the SACL that contains this ACE.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_MANDATORY_LABEL_NO_WRITE_UP"></a><a id="system_mandatory_label_no_write_up"></a><dl>
<dt><b>SYSTEM_MANDATORY_LABEL_NO_WRITE_UP</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
A principal with a lower mandatory level than the object cannot write to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_MANDATORY_LABEL_NO_READ_UP"></a><a id="system_mandatory_label_no_read_up"></a><dl>
<dt><b>SYSTEM_MANDATORY_LABEL_NO_READ_UP</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
A principal with a lower mandatory level than the object cannot read the object.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_MANDATORY_LABEL_NO_EXECUTE_UP"></a><a id="system_mandatory_label_no_execute_up"></a><dl>
<dt><b>SYSTEM_MANDATORY_LABEL_NO_EXECUTE_UP</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
A principal with a lower mandatory level than the object cannot execute the object.

</td>
</tr>
</table>

### -param pLabelSid [in]

A pointer to an SID that specifies the mandatory integrity level of the object associated with the SACL being appended.

## -returns

If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following are possible error values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ALLOTTED_SPACE_EXCEEDED</b></dt>
<dt>0x540</dt>
</dl>
</td>
<td width="60%">
The new ACE does not fit into the <i>pAcl</i> buffer.

</td>
</tr>
</table>

## -remarks

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-system_mandatory_label_ace">SYSTEM_MANDATORY_LABEL_ACE</a>