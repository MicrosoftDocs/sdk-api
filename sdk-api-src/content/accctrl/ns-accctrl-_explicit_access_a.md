---
UID: NS:accctrl._EXPLICIT_ACCESS_A
title: "_EXPLICIT_ACCESS_A"
author: windows-sdk-content
description: Defines access control information for a specified trustee.
old-location: security\explicit_access.htm
tech.root: secauthz
ms.assetid: 6fe09542-10dd-439c-adf8-a4e06943ddb2
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PEXPLICIT_ACCESSA, *PEXPLICIT_ACCESS_A, CONTAINER_INHERIT_ACE, EXPLICIT_ACCESS, EXPLICIT_ACCESS structure [Security], EXPLICIT_ACCESSA, EXPLICIT_ACCESS_, EXPLICIT_ACCESS_A, EXPLICIT_ACCESS_W, INHERIT_NO_PROPAGATE, INHERIT_ONLY, INHERIT_ONLY_ACE, NO_INHERITANCE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, PEXPLICIT_ACCESS, PEXPLICIT_ACCESS structure pointer [Security], SUB_CONTAINERS_AND_OBJECTS_INHERIT, SUB_CONTAINERS_ONLY_INHERIT, SUB_OBJECTS_ONLY_INHERIT, _EXPLICIT_ACCESS_A, _EXPLICIT_ACCESS_W, _win32_explicit_access_str, accctrl/EXPLICIT_ACCESS, accctrl/EXPLICIT_ACCESS_A, accctrl/EXPLICIT_ACCESS_W, accctrl/PEXPLICIT_ACCESS, security.explicit_access"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: EXPLICIT_ACCESS_A, *PEXPLICIT_ACCESS_A, EXPLICIT_ACCESSA, *PEXPLICIT_ACCESSA
req.redist: 
---

# _EXPLICIT_ACCESS_A structure


## -description


The <b>EXPLICIT_ACCESS</b> structure defines access control information for a specified trustee. Access control functions, such as 
<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a> and 
<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a>, use this structure to describe the information in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a>(ACE) of an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -struct-fields




### -field grfAccessPermissions

A set of bit flags that use the 
<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a> format to specify the access rights that an ACE allows, denies, or audits for the trustee. The functions that use the <b>EXPLICIT_ACCESS</b> structure do not convert, interpret, or validate the bits in this mask.


### -field grfAccessMode

A value from the 
<a href="https://msdn.microsoft.com/52d1b3a3-eed5-4603-9056-520320da2a52">ACCESS_MODE</a> enumeration. For a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL), this flag indicates whether the ACL allows or denies the specified access rights. For a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL), this flag indicates whether the ACL generates audit messages for successful attempts to use the specified access rights, or failed attempts, or both. When modifying an existing ACL, you can specify the REVOKE_ACCESS flag to remove any existing ACEs for the specified trustee.


### -field grfInheritance

A set of bit flags that determines whether other containers or objects can inherit the 
ACE from the primary object to which the 
ACL is attached. The value of this member corresponds to the inheritance portion (low-order byte) of the <b>AceFlags</b> member of the 
<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure. This parameter can be NO_INHERITANCE to indicate that the ACE is not inheritable; or it can be a combination of the following values.

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

A <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure that identifies the user, group, or program (such as a Windows service) to which the ACE applies.


## -see-also




<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/52d1b3a3-eed5-4603-9056-520320da2a52">ACCESS_MODE</a>



<a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACE</a>



<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>



<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/5f12db19-63cf-4be6-9450-3c36e425967b">BuildExplicitAccessWithName</a>



<a href="https://msdn.microsoft.com/becc1218-5bc3-4ab2-86f8-3ebd10e16966">BuildSecurityDescriptor</a>



<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a>



<a href="https://msdn.microsoft.com/68c3f56b-6c48-4f4b-bd38-9f4e346c663b">LookupSecurityDescriptorParts</a>



<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

