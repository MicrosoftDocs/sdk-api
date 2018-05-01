---
UID: NF:aclapi.BuildExplicitAccessWithNameA
title: BuildExplicitAccessWithNameA function
author: windows-driver-content
description: Initializes an EXPLICIT_ACCESS structure with data specified by the caller. The trustee is identified by a name string.
old-location: security\buildexplicitaccesswithname.htm
old-project: SecAuthZ
ms.assetid: 5f12db19-63cf-4be6-9450-3c36e425967b
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: BuildExplicitAccessWithName, BuildExplicitAccessWithName function [Security], BuildExplicitAccessWithNameA, BuildExplicitAccessWithNameW, CONTAINER_INHERIT_ACE, INHERIT_ONLY_ACE, MultipleTrusteeOperation, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, SUB_CONTAINERS_AND_OBJECTS_INHERIT, SUB_CONTAINERS_ONLY_INHERIT, SUB_OBJECTS_ONLY_INHERIT, TrusteeForm, TrusteeType, _win32_buildexplicitaccesswithname, aclapi/BuildExplicitAccessWithName, aclapi/BuildExplicitAccessWithNameA, aclapi/BuildExplicitAccessWithNameW, pMultipleTrustee, security.buildexplicitaccesswithname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: TRUSTEE_W, *PTRUSTEE_W, TRUSTEEW, *PTRUSTEEW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	API-MS-Win-security-trustee-l1-1-1.dll
-	advapi32legacy.dll
api_name:
-	BuildExplicitAccessWithName
-	BuildExplicitAccessWithNameA
-	BuildExplicitAccessWithNameW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# BuildExplicitAccessWithNameA function


## -description



			The <b>BuildExplicitAccessWithName</b> function initializes an 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure with data specified by the caller. The trustee is identified by a name string.


## -parameters




### -param pExplicitAccess [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure to initialize. The <b>BuildExplicitAccessWithName</b> function does not allocate any memory. This parameter cannot be <b>NULL</b>.


### -param pTrusteeName [in, optional]

A pointer to a <b>null</b>-terminated string that contains the name of the trustee for the <b>ptstrName</b> member of the 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. The <b>BuildExplicitAccessWithName</b> function sets the other members of the <b>TRUSTEE</b> structure as follows.

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

Specifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access mask</a> for the <b>grfAccessPermissions</b> member of the <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure. The mask is a set of bit flags that use the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> format to specify the access rights that an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a> allows, denies, or audits for the trustee. The functions that use the <b>EXPLICIT_ACCESS</b> structure do not convert, interpret, or validate the bits in this mask.


### -param AccessMode [in]

Specifies an access mode for the <b>grfAccessMode</b> member of the <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure. The access mode indicates whether the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) allows, denies, or audits the specified rights. For a <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL), this parameter can be one of the values from the 
<a href="https://msdn.microsoft.com/52d1b3a3-eed5-4603-9056-520320da2a52">ACCESS_MODE</a> enumeration. For a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL), this parameter can be a combination of <b>ACCESS_MODE</b> values.


### -param Inheritance [in]

Specifies an inheritance type for the <b>grfInheritance</b> member of the <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure. This value is a set of bit flags that determine whether other containers or objects can inherit the ACE from the primary object to which the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> is attached. The value of this member corresponds to the inheritance portion (low-order byte) of the <b>AceFlags</b> member of the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure. This parameter can be NO_INHERITANCE to indicate that the ACE is not inheritable, or it can be a combination of the following values.

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
 


## -returns




						This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a>



<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a>



<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

