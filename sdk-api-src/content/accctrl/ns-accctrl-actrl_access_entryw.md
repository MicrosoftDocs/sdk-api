---
UID: NS:accctrl._ACTRL_ACCESS_ENTRYW
title: ACTRL_ACCESS_ENTRYW (accctrl.h)
description: Contains access-control information for a specified trustee. This structure stores information equivalent to the access-control information stored in an ACE. (Unicode)
helpviewer_keywords: ["*PACTRL_ACCESS_ENTRYW","ACTRL_ACCESS_ALLOWED","ACTRL_ACCESS_DENIED","ACTRL_ACCESS_ENTRY","ACTRL_ACCESS_ENTRY structure [COM]","ACTRL_ACCESS_ENTRYA","ACTRL_ACCESS_ENTRYW","ACTRL_AUDIT_FAILURE","ACTRL_AUDIT_SUCCESS","ACTRL_CHANGE_ACCESS","ACTRL_CHANGE_OWNER","ACTRL_DELETE","ACTRL_READ_CONTROL","ACTRL_STD_RIGHTS_ALL","ACTRL_STD_RIGHT_REQUIRED","ACTRL_SYNCHRONIZE","ACTRL_SYSTEM_ACCESS","COM_RIGHTS_ACTIVATE_LOCAL","COM_RIGHTS_ACTIVATE_REMOTE","COM_RIGHTS_EXECUTE","COM_RIGHTS_EXECUTE_LOCAL","COM_RIGHTS_EXECUTE_REMOTE","CONTAINER_INHERIT_ACE","INHERIT_ONLY_ACE","NO_PROPAGATE_INHERIT_ACE","OBJECT_INHERIT_ACE","PACTRL_ACCESS_ENTRY","PACTRL_ACCESS_ENTRY structure pointer [COM]","SUB_CONTAINERS_AND_OBJECTS_INHERIT","SUB_CONTAINERS_ONLY_INHERIT","SUB_OBJECTS_ONLY_INHERIT","_ACTRL_ACCESS_ENTRYA","_ACTRL_ACCESS_ENTRYW","accctrl/ACTRL_ACCESS_ENTRY","accctrl/ACTRL_ACCESS_ENTRYA","accctrl/ACTRL_ACCESS_ENTRYW","accctrl/PACTRL_ACCESS_ENTRY","com.actrl_access_entry"]
old-location: com\actrl_access_entry.htm
tech.root: com
ms.assetid: bcb2ad72-7b00-4582-b05e-e00720a4db77
ms.date: 12/05/2018
ms.keywords: '*PACTRL_ACCESS_ENTRYW, ACTRL_ACCESS_ALLOWED, ACTRL_ACCESS_DENIED, ACTRL_ACCESS_ENTRY, ACTRL_ACCESS_ENTRY structure [COM], ACTRL_ACCESS_ENTRYA, ACTRL_ACCESS_ENTRYW, ACTRL_AUDIT_FAILURE, ACTRL_AUDIT_SUCCESS, ACTRL_CHANGE_ACCESS, ACTRL_CHANGE_OWNER, ACTRL_DELETE, ACTRL_READ_CONTROL, ACTRL_STD_RIGHTS_ALL, ACTRL_STD_RIGHT_REQUIRED, ACTRL_SYNCHRONIZE, ACTRL_SYSTEM_ACCESS, COM_RIGHTS_ACTIVATE_LOCAL, COM_RIGHTS_ACTIVATE_REMOTE, COM_RIGHTS_EXECUTE, COM_RIGHTS_EXECUTE_LOCAL, COM_RIGHTS_EXECUTE_REMOTE, CONTAINER_INHERIT_ACE, INHERIT_ONLY_ACE, NO_PROPAGATE_INHERIT_ACE, OBJECT_INHERIT_ACE, PACTRL_ACCESS_ENTRY, PACTRL_ACCESS_ENTRY structure pointer [COM], SUB_CONTAINERS_AND_OBJECTS_INHERIT, SUB_CONTAINERS_ONLY_INHERIT, SUB_OBJECTS_ONLY_INHERIT, _ACTRL_ACCESS_ENTRYA, _ACTRL_ACCESS_ENTRYW, accctrl/ACTRL_ACCESS_ENTRY, accctrl/ACTRL_ACCESS_ENTRYA, accctrl/ACTRL_ACCESS_ENTRYW, accctrl/PACTRL_ACCESS_ENTRY, com.actrl_access_entry'
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ACTRL_ACCESS_ENTRYW (Unicode) and ACTRL_ACCESS_ENTRYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACTRL_ACCESS_ENTRYW, *PACTRL_ACCESS_ENTRYW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACTRL_ACCESS_ENTRYW
 - accctrl/_ACTRL_ACCESS_ENTRYW
 - PACTRL_ACCESS_ENTRYW
 - accctrl/PACTRL_ACCESS_ENTRYW
 - ACTRL_ACCESS_ENTRYW
 - accctrl/ACTRL_ACCESS_ENTRYW
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
 - ACTRL_ACCESS_ENTRY
 - ACTRL_ACCESS_ENTRYA
 - ACTRL_ACCESS_ENTRYW
---

# ACTRL_ACCESS_ENTRYW structure


## -description

 Contains access-control information for a specified trustee. This structure stores information equivalent to the access-control information stored in an <a href="/windows/desktop/SecAuthZ/ace">ACE</a>.

## -struct-fields

### -field Trustee

A <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure that identifies the user, group, or program (such as a service) to which the access-control entry applies.

### -field fAccessFlags

Indicates how the access rights specified by the <b>Access</b> and <b>ProvSpecificAccess</b> members apply to the trustee. This member can be one of the following values. If you are using this structure with the COM implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>, this member must be ACTRL_ACCESS_ALLOWED or ACTRL_ACCESS_DENIED. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACTRL_ACCESS_ALLOWED"></a><a id="actrl_access_allowed"></a><dl>
<dt><b>ACTRL_ACCESS_ALLOWED</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The rights are allowed.

</td>
</tr>
<tr>
<td width="40%"><a id="ACTRL_ACCESS_DENIED"></a><a id="actrl_access_denied"></a><dl>
<dt><b>ACTRL_ACCESS_DENIED</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The rights are denied.

</td>
</tr>
<tr>
<td width="40%"><a id="ACTRL_AUDIT_SUCCESS"></a><a id="actrl_audit_success"></a><dl>
<dt><b>ACTRL_AUDIT_SUCCESS</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The system generates audit messages for failed attempts to use the rights.

</td>
</tr>
<tr>
<td width="40%"><a id="ACTRL_AUDIT_FAILURE"></a><a id="actrl_audit_failure"></a><dl>
<dt><b>ACTRL_AUDIT_FAILURE</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The system generates audit messages for successful attempts to use the rights.

</td>
</tr>
</table>

### -field Access

A bitmask that specifies the access rights that the entry allows, denies, or audits for the trustee.

This member must use the provider-independent access flags, such as ACTRL_READ_CONTROL, rather than access flags such as READ_CONTROL. The provider for the object type converts these provider-independent flags to the corresponding provider-specific flags.

If you are using this structure with the COM implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>, this member must be COM_RIGHTS_EXECUTE.

<a id="ACTRL_SYSTEM_ACCESS"></a>
<a id="actrl_system_access"></a>


#### ACTRL_SYSTEM_ACCESS

<a id="ACTRL_DELETE"></a>
<a id="actrl_delete"></a>


#### ACTRL_DELETE

<a id="ACTRL_READ_CONTROL"></a>
<a id="actrl_read_control"></a>


#### ACTRL_READ_CONTROL

<a id="ACTRL_CHANGE_ACCESS"></a>
<a id="actrl_change_access"></a>


#### ACTRL_CHANGE_ACCESS

<a id="ACTRL_CHANGE_OWNER"></a>
<a id="actrl_change_owner"></a>


#### ACTRL_CHANGE_OWNER

<a id="ACTRL_SYNCHRONIZE"></a>
<a id="actrl_synchronize"></a>


#### ACTRL_SYNCHRONIZE

<a id="ACTRL_STD_RIGHTS_ALL"></a>
<a id="actrl_std_rights_all"></a>


#### ACTRL_STD_RIGHTS_ALL

<a id="ACTRL_STD_RIGHT_REQUIRED"></a>
<a id="actrl_std_right_required"></a>


#### ACTRL_STD_RIGHT_REQUIRED

<a id="COM_RIGHTS_EXECUTE"></a>
<a id="com_rights_execute"></a>


#### COM_RIGHTS_EXECUTE

<a id="COM_RIGHTS_EXECUTE_LOCAL"></a>
<a id="com_rights_execute_local"></a>


#### COM_RIGHTS_EXECUTE_LOCAL

<a id="COM_RIGHTS_EXECUTE_REMOTE"></a>
<a id="com_rights_execute_remote"></a>


#### COM_RIGHTS_EXECUTE_REMOTE

<a id="COM_RIGHTS_ACTIVATE_LOCAL"></a>
<a id="com_rights_activate_local"></a>


#### COM_RIGHTS_ACTIVATE_LOCAL

<a id="COM_RIGHTS_ACTIVATE_REMOTE"></a>
<a id="com_rights_activate_remote"></a>


#### COM_RIGHTS_ACTIVATE_REMOTE

### -field ProvSpecificAccess

A bitmask that specifies access rights specific to the provider type. The functions that use the <b>ACTRL_ACCESS_ENTRY</b> structure pass these bits on to the provider without interpreting them. In most cases, this member should be 0.

### -field Inheritance

A set of bit flags that determines whether other containers or objects can inherit the access-control entry from the primary object to which the access list is attached. If you are using this structure with the COM implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>, this value must be NO_INHERITANCE, which indicates that the access-control entry is not inheritable. Otherwise, this value can be NO_INHERITANCE or it can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONTAINER_INHERIT_ACE"></a><a id="container_inherit_ace"></a><dl>
<dt><b>CONTAINER_INHERIT_ACE</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Other containers that are contained by the primary object inherit the entry. 


</td>
</tr>
<tr>
<td width="40%"><a id="INHERIT_ONLY_ACE_"></a><a id="inherit_only_ace_"></a><dl>
<dt><b>INHERIT_ONLY_ACE
</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
The ACE does not apply to the primary object to which the ACL is attached, but objects contained by the primary object inherit the entry.

</td>
</tr>
<tr>
<td width="40%"><a id="NO_PROPAGATE_INHERIT_ACE"></a><a id="no_propagate_inherit_ace"></a><dl>
<dt><b>NO_PROPAGATE_INHERIT_ACE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The OBJECT_INHERIT_ACE and CONTAINER_INHERIT_ACE flags are not propagated to an inherited entry.


</td>
</tr>
<tr>
<td width="40%"><a id="OBJECT_INHERIT_ACE"></a><a id="object_inherit_ace"></a><dl>
<dt><b>OBJECT_INHERIT_ACE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Noncontainer objects contained by the primary object inherit the entry.

</td>
</tr>
<tr>
<td width="40%"><a id="SUB_CONTAINERS_AND_OBJECTS_INHERIT"></a><a id="sub_containers_and_objects_inherit"></a><dl>
<dt><b>SUB_CONTAINERS_AND_OBJECTS_INHERIT</b></dt>
<dt>0x3</dt>
</dl>
</td>
<td width="60%">
Both containers and noncontainer objects that are contained by the primary object inherit the entry. This flag corresponds to the combination of the CONTAINER_INHERIT_ACE and OBJECT_INHERIT_ACE flags.


</td>
</tr>
<tr>
<td width="40%"><a id="SUB_CONTAINERS_ONLY_INHERIT"></a><a id="sub_containers_only_inherit"></a><dl>
<dt><b>SUB_CONTAINERS_ONLY_INHERIT</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Other containers that are contained by the primary object inherit the entry. This flag corresponds to the CONTAINER_INHERIT_ACE flag.


</td>
</tr>
<tr>
<td width="40%"><a id="SUB_OBJECTS_ONLY_INHERIT"></a><a id="sub_objects_only_inherit"></a><dl>
<dt><b>SUB_OBJECTS_ONLY_INHERIT</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Noncontainer objects contained by the primary object inherit the entry. This flag corresponds to the OBJECT_INHERIT_ACE flag.


</td>
</tr>
</table>

### -field lpInheritProperty

A pointer to a null-terminated string that identifies the object types that can inherit the entry. If you are using this structure with the COM implementation of <a href="/windows/desktop/api/iaccess/nn-iaccess-iaccesscontrol">IAccessControl</a>, this member must be <b>NULL</b>. 



##### - Access.ACTRL_CHANGE_ACCESS

<a id="ACTRL_CHANGE_OWNER"></a>
<a id="actrl_change_owner"></a>

##### - Access.ACTRL_CHANGE_OWNER

<a id="ACTRL_SYNCHRONIZE"></a>
<a id="actrl_synchronize"></a>

##### - Access.ACTRL_DELETE

<a id="ACTRL_READ_CONTROL"></a>
<a id="actrl_read_control"></a>

##### - Access.ACTRL_READ_CONTROL

<a id="ACTRL_CHANGE_ACCESS"></a>
<a id="actrl_change_access"></a>

##### - Access.ACTRL_STD_RIGHTS_ALL

<a id="ACTRL_STD_RIGHT_REQUIRED"></a>
<a id="actrl_std_right_required"></a>

##### - Access.ACTRL_STD_RIGHT_REQUIRED

<a id="COM_RIGHTS_EXECUTE"></a>
<a id="com_rights_execute"></a>

##### - Access.ACTRL_SYNCHRONIZE

<a id="ACTRL_STD_RIGHTS_ALL"></a>
<a id="actrl_std_rights_all"></a>

##### - Access.ACTRL_SYSTEM_ACCESS

<a id="ACTRL_DELETE"></a>
<a id="actrl_delete"></a>

##### - Access.COM_RIGHTS_ACTIVATE_LOCAL

<a id="COM_RIGHTS_ACTIVATE_REMOTE"></a>
<a id="com_rights_activate_remote"></a>

##### - Access.COM_RIGHTS_ACTIVATE_REMOTE


##### - Access.COM_RIGHTS_EXECUTE

<a id="COM_RIGHTS_EXECUTE_LOCAL"></a>
<a id="com_rights_execute_local"></a>

##### - Access.COM_RIGHTS_EXECUTE_LOCAL

<a id="COM_RIGHTS_EXECUTE_REMOTE"></a>
<a id="com_rights_execute_remote"></a>

##### - Access.COM_RIGHTS_EXECUTE_REMOTE

<a id="COM_RIGHTS_ACTIVATE_LOCAL"></a>
<a id="com_rights_activate_local"></a>

## -see-also

<a href="/windows/desktop/api/accctrl/ns-accctrl-actrl_access_entry_lista">ACTRL_ACCESS_ENTRY_LIST</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>

## -remarks

> [!NOTE]
> The accctrl.h header defines ACTRL_ACCESS_ENTRY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
