---
UID: NS:accctrl._EXPLICIT_ACCESS_W
title: EXPLICIT_ACCESS_W (accctrl.h)
description: Defines access control information for a specified trustee. (Unicode)
helpviewer_keywords: ["*PEXPLICIT_ACCESSW","*PEXPLICIT_ACCESS_W","CONTAINER_INHERIT_ACE","EXPLICIT_ACCESS","EXPLICIT_ACCESS structure [Security]","EXPLICIT_ACCESSW","EXPLICIT_ACCESS_","EXPLICIT_ACCESS_A","EXPLICIT_ACCESS_W","INHERIT_NO_PROPAGATE","INHERIT_ONLY","INHERIT_ONLY_ACE","NO_INHERITANCE","NO_PROPAGATE_INHERIT_ACE","OBJECT_INHERIT_ACE","PEXPLICIT_ACCESS","PEXPLICIT_ACCESS structure pointer [Security]","SUB_CONTAINERS_AND_OBJECTS_INHERIT","SUB_CONTAINERS_ONLY_INHERIT","SUB_OBJECTS_ONLY_INHERIT","_EXPLICIT_ACCESS_A","_EXPLICIT_ACCESS_W","_win32_explicit_access_str","accctrl/EXPLICIT_ACCESS","accctrl/EXPLICIT_ACCESS_A","accctrl/EXPLICIT_ACCESS_W","accctrl/PEXPLICIT_ACCESS","security.explicit_access"]
old-location: security\explicit_access.htm
tech.root: security
ms.assetid: 6fe09542-10dd-439c-adf8-a4e06943ddb2
ms.date: 12/05/2018
ms.keywords: '*PEXPLICIT_ACCESSW, *PEXPLICIT_ACCESS_W, CONTAINER_INHERIT_ACE, EXPLICIT_ACCESS, EXPLICIT_ACCESS structure [Security], EXPLICIT_ACCESSW, EXPLICIT_ACCESS_, EXPLICIT_ACCESS_A, EXPLICIT_ACCESS_W, INHERIT_NO_PROPAGATE, INHERIT_ONLY, INHERIT_ONLY_ACE, NO_INHERITANCE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, PEXPLICIT_ACCESS, PEXPLICIT_ACCESS structure pointer [Security], SUB_CONTAINERS_AND_OBJECTS_INHERIT, SUB_CONTAINERS_ONLY_INHERIT, SUB_OBJECTS_ONLY_INHERIT, _EXPLICIT_ACCESS_A, _EXPLICIT_ACCESS_W, _win32_explicit_access_str, accctrl/EXPLICIT_ACCESS, accctrl/EXPLICIT_ACCESS_A, accctrl/EXPLICIT_ACCESS_W, accctrl/PEXPLICIT_ACCESS, security.explicit_access'
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EXPLICIT_ACCESS_W (Unicode) and EXPLICIT_ACCESS_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EXPLICIT_ACCESS_W, *PEXPLICIT_ACCESS_W, EXPLICIT_ACCESSW, *PEXPLICIT_ACCESSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EXPLICIT_ACCESS_W
 - accctrl/_EXPLICIT_ACCESS_W
 - PEXPLICIT_ACCESS_W
 - accctrl/PEXPLICIT_ACCESS_W
 - EXPLICIT_ACCESS_W
 - accctrl/EXPLICIT_ACCESS_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - EXPLICIT_ACCESS
 - EXPLICIT_ACCESS_A
 - EXPLICIT_ACCESS_W
---

# EXPLICIT_ACCESS_W structure


## -description

The <b>EXPLICIT_ACCESS</b> structure defines access control information for a specified trustee. Access control functions, such as 
<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a> and 
<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>, use this structure to describe the information in an <a href="/windows/desktop/SecGloss/a-gly">access control entry</a>(ACE) of an <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL).

## -struct-fields

### -field grfAccessPermissions

A set of bit flags that use the 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> format to specify the access rights that an ACE allows, denies, or audits for the trustee. The functions that use the <b>EXPLICIT_ACCESS</b> structure do not convert, interpret, or validate the bits in this mask.

### -field grfAccessMode

A value from the 
<a href="/windows/desktop/api/accctrl/ne-accctrl-access_mode">ACCESS_MODE</a> enumeration. For a <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL), this flag indicates whether the ACL allows or denies the specified access rights. For a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL), this flag indicates whether the ACL generates audit messages for successful attempts to use the specified access rights, or failed attempts, or both. When modifying an existing ACL, you can specify the REVOKE_ACCESS flag to remove any existing ACEs for the specified trustee.

### -field grfInheritance

A set of bit flags that determines whether other containers or objects can inherit the 
ACE from the primary object to which the 
ACL is attached. The value of this member corresponds to the inheritance portion (low-order byte) of the <b>AceFlags</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure. This parameter can be NO_INHERITANCE to indicate that the ACE is not inheritable; or it can be a combination of the following values.

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
Other containers that are contained by the primary object inherit the ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_NO_PROPAGATE"></a><a id="inherit_no_propagate"></a><dl>
<dt><b>INHERIT_NO_PROPAGATE</b></dt>
</dl>
</td>
<td width="60%">
Inherit but do not propagate.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY"></a><a id="inherit_only"></a><dl>
<dt><b>INHERIT_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Inherit only.

</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the primary object to which the ACL is attached, but objects contained by the primary object inherit the ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_INHERITANCE"></a><a id="no_inheritance"></a><dl>
<dt><b>NO_INHERITANCE</b></dt>
</dl>
</td>
<td width="60%">
Do not inherit.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
The OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE flags are not propagated to an inherited ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
</dl>
</td>
<td width="60%">
Noncontainer objects contained by the primary object inherit the ACE.

</td>
</tr>
<tr>
<td width="40%"><a id="SUB_CONTAINERS_AND_OBJECTS_INHERIT"></a><a id="sub_containers_and_objects_inherit"></a><dl>
<dt><b>SUB_CONTAINERS_AND_OBJECTS_INHERIT</b></dt>
</dl>
</td>
<td width="60%">
Both containers and noncontainer objects that are contained by the primary object inherit the ACE. This flag corresponds to the combination of the CONTAINER_INHERIT_ACE and OBJECT_INHERIT_ACE flags.

</td>
</tr>
<tr>
<td width="40%"><a id="SUB_CONTAINERS_ONLY_INHERIT"></a><a id="sub_containers_only_inherit"></a><dl>
<dt><b>SUB_CONTAINERS_ONLY_INHERIT</b></dt>
</dl>
</td>
<td width="60%">
Other containers that are contained by the primary object inherit the ACE. This flag corresponds to the CONTAINER_INHERIT_ACE flag.

</td>
</tr>
<tr>
<td width="40%"><a id="SUB_OBJECTS_ONLY_INHERIT"></a><a id="sub_objects_only_inherit"></a><dl>
<dt><b>SUB_OBJECTS_ONLY_INHERIT</b></dt>
</dl>
</td>
<td width="60%">
Noncontainer objects contained by the primary object inherit the ACE. This flag corresponds to the OBJECT_INHERIT_ACE flag.

</td>
</tr>
</table>

### -field Trustee

A <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure that identifies the user, group, or program (such as a Windows service) to which the ACE applies.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-access_mode">ACCESS_MODE</a>



<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-buildexplicitaccesswithnamea">BuildExplicitAccessWithName</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora">BuildSecurityDescriptor</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-lookupsecuritydescriptorpartsa">LookupSecurityDescriptorParts</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>

## -remarks

> [!NOTE]
> The accctrl.h header defines EXPLICIT_ACCESS_ as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
