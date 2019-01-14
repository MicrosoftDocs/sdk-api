---
UID: NS:winnt._SYSTEM_AUDIT_CALLBACK_OBJECT_ACE
title: SYSTEM_AUDIT_CALLBACK_OBJECT_ACE
author: windows-sdk-content
description: The SYSTEM_AUDIT_CALLBACK_OBJECT_ACE structure defines an access control entry for a system access control list.
old-location: security\system_audit_callback_object_ace.htm
tech.root: SecAuthZ
ms.assetid: f547c928-4850-4072-be05-76a6c83b79bb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSYSTEM_AUDIT_CALLBACK_OBJECT_ACE, ACE_INHERITED_OBJECT_TYPE_PRESENT, ACE_OBJECT_TYPE_PRESENT, ADS_RIGHT_DS_CONTROL_ACCESS, ADS_RIGHT_DS_CREATE_CHILD, ADS_RIGHT_DS_READ_PROP and/or ADS_RIGHT_DS_WRITE_PROP, ADS_RIGHT_DS_SELF, PSYSTEM_AUDIT_CALLBACK_OBJECT_ACE, PSYSTEM_AUDIT_CALLBACK_OBJECT_ACE structure pointer [Security], SYSTEM_AUDIT_CALLBACK_OBJECT_ACE, SYSTEM_AUDIT_CALLBACK_OBJECT_ACE structure [Security], _SYSTEM_AUDIT_CALLBACK_OBJECT_ACE, security.system_audit_callback_object_ace, winnt/PSYSTEM_AUDIT_CALLBACK_OBJECT_ACE, winnt/SYSTEM_AUDIT_CALLBACK_OBJECT_ACE"
ms.topic: struct
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SYSTEM_AUDIT_CALLBACK_OBJECT_ACE
product: Windows
targetos: Windows
req.typenames: SYSTEM_AUDIT_CALLBACK_OBJECT_ACE, *PSYSTEM_AUDIT_CALLBACK_OBJECT_ACE
req.redist: 
---

# SYSTEM_AUDIT_CALLBACK_OBJECT_ACE structure


## -description


The <b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</b> structure defines an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) for a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL). The ACE can audit access to an object or subobjects such as property sets or properties. The ACE contains a set of access rights, a GUID that identifies the type of object or subobject, and a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) that identifies the <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trustee</a> for whom the system will audit access. The ACE also contains a GUID and a set of flags that control inheritance of the ACE by child objects.

When the <a href="https://msdn.microsoft.com/633c2a73-169c-4e0c-abb6-96c360bd63cf">AuthzAccessCheck</a> function is called, each <b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</b> structure contained in the DACL of a <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure passed through a pointer to the <b>AuthzAccessCheck</b> function invokes a call to the application-defined <a href="https://msdn.microsoft.com/e8a510e6-0739-4765-ad07-3bcb1b9c905c">AuthzAccessCheckCallback</a> function, in which a pointer to the <b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</b> structure found is passed in the <i>pAce</i> parameter.


## -struct-fields




### -field Header


<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure that specifies the size and type of ACE. It contains flags that control inheritance of the ACE by child objects. The structure also contains flags that indicate whether the ACE audits successful access attempts, failed access attempts, or both. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to SYSTEM_AUDIT_CALLBACK_OBJECT_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</b> structure.


### -field Mask

An 
<a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a> that specifies the access rights the system will audit for access attempts by the <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">trustee</a>.


### -field Flags

A set of bit flags that indicate whether the <b>ObjectType</b> and <b>InheritedObjectType</b> members contain GUIDs. This member can be a combination of the following values. Set all undefined bits to zero. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACE_OBJECT_TYPE_PRESENT"></a><a id="ace_object_type_present"></a><dl>
<dt><b>ACE_OBJECT_TYPE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> member contains a GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="ACE_INHERITED_OBJECT_TYPE_PRESENT"></a><a id="ace_inherited_object_type_present"></a><dl>
<dt><b>ACE_INHERITED_OBJECT_TYPE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>InheritedObjectType</b> member contains a GUID.

</td>
</tr>
</table>
 


### -field ObjectType

A 
<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that identifies a property set, property, extended right, or type of child object. 




This member is valid only if the ACE_OBJECT_TYPE_PRESENT bit is set in the <b>Flags</b> member. Otherwise, <b>ObjectType</b> is ignored.

The purpose of this GUID depends on the access rights specified in the <b>Mask</b> member.

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_READ_PROP_and_or_ADS_RIGHT_DS_WRITE_PROP"></a><a id="ads_right_ds_read_prop_and_or_ads_right_ds_write_prop"></a><a id="ADS_RIGHT_DS_READ_PROP_AND_OR_ADS_RIGHT_DS_WRITE_PROP"></a><dl>
<dt><b>ADS_RIGHT_DS_READ_PROP and/or ADS_RIGHT_DS_WRITE_PROP</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> GUID identifies a property set or property of the object. The ACE controls auditing of the trustee's attempts to read or write the property or property set.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_CONTROL_ACCESS"></a><a id="ads_right_ds_control_access"></a><dl>
<dt><b>ADS_RIGHT_DS_CONTROL_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> GUID identifies an extended access right.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_CREATE_CHILD"></a><a id="ads_right_ds_create_child"></a><dl>
<dt><b>ADS_RIGHT_DS_CREATE_CHILD</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> GUID identifies a type of child object. The ACE controls auditing of the trustee's attempts to create this type of child object.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_SELF"></a><a id="ads_right_ds_self"></a><dl>
<dt><b>ADS_RIGHT_DS_SELF</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> GUID identifies a validated write.

</td>
</tr>
</table>
 


### -field InheritedObjectType

A <a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that identifies the type of child object that can inherit the ACE. 




This member is valid only if the ACE_INHERITED_OBJECT_TYPE_PRESENT bit is set in the <b>Flags</b> member. If that bit is not set, <b>InheritedObjectType</b> is ignored and all types of child objects can inherit the ACE. In either case, inheritance is also controlled by the inheritance flags in the 
<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>, as well as by any protection against inheritance placed on the child objects.


### -field SidStart

The first <b>DWORD</b> of a trustee's SID. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data.


## -remarks



If neither the <b>ObjectType</b> nor <b>InheritedObjectType</b> GUID is specified, the <b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</b> structure has the same semantics as the <a href="https://msdn.microsoft.com/4d1799b0-3e55-48d7-94ff-c0094945adea">SYSTEM_AUDIT_CALLBACK_ACE</a> structure. In that case, use the 
<b>SYSTEM_AUDIT_CALLBACK_ACE</b> structure because it is smaller and more efficient.

An ACL that contains a <b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</b> structure must specify the ACL_REVISION_DS revision number in its 
<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a> structure.

When a <b>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</b> structure is created, sufficient memory must be allocated to accommodate the GUID structures in <b>ObjectType</b> and <b>InheritedObjectType</b> members, if one or both of them exists, as well as to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory that follows it.




## -see-also




<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/be852a0c-9d96-4b29-b5f9-d9c41d838c12">AddAuditAccessObjectAce</a>



<a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>
 

 

