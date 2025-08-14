---
UID: NF:aclapi.BuildExplicitAccessWithNameW
title: BuildExplicitAccessWithNameW function (aclapi.h)
description: Initializes an EXPLICIT_ACCESS structure with data specified by the caller. The trustee is identified by a name string. (Unicode)
helpviewer_keywords: ["BuildExplicitAccessWithName", "BuildExplicitAccessWithName function [Security]", "BuildExplicitAccessWithNameW", "CONTAINER_INHERIT_ACE", "INHERIT_ONLY_ACE", "MultipleTrusteeOperation", "NO_PROPAGATE_INHERIT_ACE", "OBJECT_INHERIT_ACE", "SUB_CONTAINERS_AND_OBJECTS_INHERIT", "SUB_CONTAINERS_ONLY_INHERIT", "SUB_OBJECTS_ONLY_INHERIT", "TrusteeForm", "TrusteeType", "_win32_buildexplicitaccesswithname", "aclapi/BuildExplicitAccessWithName", "aclapi/BuildExplicitAccessWithNameW", "pMultipleTrustee", "security.buildexplicitaccesswithname"]
old-location: security\buildexplicitaccesswithname.htm
tech.root: security
ms.assetid: 5f12db19-63cf-4be6-9450-3c36e425967b
ms.date: 12/05/2018
ms.keywords: BuildExplicitAccessWithName, BuildExplicitAccessWithName function [Security], BuildExplicitAccessWithNameA, BuildExplicitAccessWithNameW, CONTAINER_INHERIT_ACE, INHERIT_ONLY_ACE, MultipleTrusteeOperation, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, SUB_CONTAINERS_AND_OBJECTS_INHERIT, SUB_CONTAINERS_ONLY_INHERIT, SUB_OBJECTS_ONLY_INHERIT, TrusteeForm, TrusteeType, _win32_buildexplicitaccesswithname, aclapi/BuildExplicitAccessWithName, aclapi/BuildExplicitAccessWithNameA, aclapi/BuildExplicitAccessWithNameW, pMultipleTrustee, security.buildexplicitaccesswithname
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BuildExplicitAccessWithNameW (Unicode) and BuildExplicitAccessWithNameA (ANSI)
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
 - BuildExplicitAccessWithNameW
 - aclapi/BuildExplicitAccessWithNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-trustee-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-security-trustee-l1-1-1.dll
 - advapi32legacy.dll
api_name:
 - BuildExplicitAccessWithName
 - BuildExplicitAccessWithNameA
 - BuildExplicitAccessWithNameW
---

# BuildExplicitAccessWithNameW function


## -description

The <b>BuildExplicitAccessWithName</b> function initializes an 
<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure with data specified by the caller. The trustee is identified by a name string.

## -parameters

### -param pExplicitAccess [in, out]

A pointer to an 
<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure to initialize. The <b>BuildExplicitAccessWithName</b> function does not allocate any memory. This parameter cannot be <b>NULL</b>.

### -param pTrusteeName [in, optional]

A pointer to a <b>null</b>-terminated string that contains the name of the trustee for the <b>ptstrName</b> member of the 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure. The <b>BuildExplicitAccessWithName</b> function sets the other members of the <b>TRUSTEE</b> structure as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="pMultipleTrustee"></a><a id="pmultipletrustee"></a><a id="PMULTIPLETRUSTEE"></a><dl>
<dt><b><b>pMultipleTrustee</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b>

</td>
</tr>
<tr>
<td width="40%"><a id="MultipleTrusteeOperation"></a><a id="multipletrusteeoperation"></a><a id="MULTIPLETRUSTEEOPERATION"></a><dl>
<dt><b><b>MultipleTrusteeOperation</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
NO_MULTIPLE_TRUSTEE

</td>
</tr>
<tr>
<td width="40%"><a id="TrusteeForm"></a><a id="trusteeform"></a><a id="TRUSTEEFORM"></a><dl>
<dt><b><b>TrusteeForm</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
TRUSTEE_IS_NAME

</td>
</tr>
<tr>
<td width="40%"><a id="TrusteeType"></a><a id="trusteetype"></a><a id="TRUSTEETYPE"></a><dl>
<dt><b><b>TrusteeType</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
TRUSTEE_IS_UNKNOWN

</td>
</tr>
</table>

### -param AccessPermissions [in]

Specifies an <a href="/windows/desktop/SecGloss/a-gly">access mask</a> for the <b>grfAccessPermissions</b> member of the <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure. The mask is a set of bit flags that use the 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> format to specify the access rights that an 
<a href="/windows/desktop/SecAuthZ/ace">ACE</a> allows, denies, or audits for the trustee. The functions that use the <b>EXPLICIT_ACCESS</b> structure do not convert, interpret, or validate the bits in this mask.

### -param AccessMode [in]

Specifies an access mode for the <b>grfAccessMode</b> member of the <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure. The access mode indicates whether the <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) allows, denies, or audits the specified rights. For a <a href="/windows/desktop/SecGloss/d-gly">discretionary access control list</a> (DACL), this parameter can be one of the values from the 
<a href="/windows/desktop/api/accctrl/ne-accctrl-access_mode">ACCESS_MODE</a> enumeration. For a <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL), this parameter can be a combination of <b>ACCESS_MODE</b> values.

### -param Inheritance [in]

Specifies an inheritance type for the <b>grfInheritance</b> member of the <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure. This value is a set of bit flags that determine whether other containers or objects can inherit the ACE from the primary object to which the 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> is attached. The value of this member corresponds to the inheritance portion (low-order byte) of the <b>AceFlags</b> member of the 
<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure. This parameter can be NO_INHERITANCE to indicate that the ACE is not inheritable, or it can be a combination of the following values.

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
<td width="40%"><a id="INHERIT_ONLY_ACE"></a><a id="inherit_only_ace"></a><dl>
<dt><b>INHERIT_ONLY_ACE</b></dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the primary object to which the ACL is attached, but objects contained by the primary object inherit the ACE.

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
Other containers that are contained by the primary object inherit the ACE. This flag corresponds to the combination of the <b>CONTAINER_INHERIT_ACE</b> and  <b>INHERIT_ONLY_ACE</b> flags.

</td>
</tr>
<tr>
<td width="40%"><a id="SUB_OBJECTS_ONLY_INHERIT"></a><a id="sub_objects_only_inherit"></a><dl>
<dt><b>SUB_OBJECTS_ONLY_INHERIT</b></dt>
</dl>
</td>
<td width="60%">
Noncontainer objects contained by the primary object inherit the ACE. This flag corresponds to the combination of the <b>OBJECT_INHERIT_ACE</b> and  <b>INHERIT_ONLY_ACE</b> flags.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>

## -remarks

> [!NOTE]
> The aclapi.h header defines BuildExplicitAccessWithName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
