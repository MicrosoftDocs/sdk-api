---
UID: NS:winnt._ACCESS_ALLOWED_OBJECT_ACE
title: ACCESS_ALLOWED_OBJECT_ACE (winnt.h)
description: Defines an access control entry (ACE) that controls allowed access to an object, a property set, or property.helpviewer_keywords: ["*PACCESS_ALLOWED_OBJECT_ACE","0","ACCESS_ALLOWED_OBJECT_ACE","ACCESS_ALLOWED_OBJECT_ACE structure [Security]","ACE_INHERITED_OBJECT_TYPE_PRESENT","ACE_OBJECT_TYPE_PRESENT","ADS_RIGHT_DS_CONTROL_ACCESS","ADS_RIGHT_DS_CREATE_CHILD","ADS_RIGHT_DS_READ_PROP","ADS_RIGHT_DS_SELF","ADS_RIGHT_DS_WRITE_PROP","PACCESS_ALLOWED_OBJECT_ACE","PACCESS_ALLOWED_OBJECT_ACE structure pointer [Security]","_ACCESS_ALLOWED_OBJECT_ACE","_win32_access_allowed_object_ace_str","security.access_allowed_object_ace","winnt/ACCESS_ALLOWED_OBJECT_ACE","winnt/PACCESS_ALLOWED_OBJECT_ACE"]
old-location: security\access_allowed_object_ace.htm
tech.root: SecAuthZ
ms.assetid: ee91ca50-e81b-4872-95eb-349c2d5be004
ms.date: 12/05/2018
ms.keywords: '*PACCESS_ALLOWED_OBJECT_ACE, 0, ACCESS_ALLOWED_OBJECT_ACE, ACCESS_ALLOWED_OBJECT_ACE structure [Security], ACE_INHERITED_OBJECT_TYPE_PRESENT, ACE_OBJECT_TYPE_PRESENT, ADS_RIGHT_DS_CONTROL_ACCESS, ADS_RIGHT_DS_CREATE_CHILD, ADS_RIGHT_DS_READ_PROP, ADS_RIGHT_DS_SELF, ADS_RIGHT_DS_WRITE_PROP, PACCESS_ALLOWED_OBJECT_ACE, PACCESS_ALLOWED_OBJECT_ACE structure pointer [Security], _ACCESS_ALLOWED_OBJECT_ACE, _win32_access_allowed_object_ace_str, security.access_allowed_object_ace, winnt/ACCESS_ALLOWED_OBJECT_ACE, winnt/PACCESS_ALLOWED_OBJECT_ACE'
f1_keywords:
- winnt/ACCESS_ALLOWED_OBJECT_ACE
dev_langs:
- c++
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
- ACCESS_ALLOWED_OBJECT_ACE
targetos: Windows
req.typenames: ACCESS_ALLOWED_OBJECT_ACE, *PACCESS_ALLOWED_OBJECT_ACE
req.redist: 
ms.custom: 19H1
---

# ACCESS_ALLOWED_OBJECT_ACE structure


## -description


The <b>ACCESS_ALLOWED_OBJECT_ACE</b> structure defines an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) that controls allowed access to an object, a property set, or property.   The ACE contains a set of access rights, a <b>GUID</b> that identifies the type of object, and a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that identifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/t-gly">trustee</a> to whom the system will grant access. The ACE also contains a <b>GUID</b> and a set of flags that control inheritance of the ACE by child objects.


## -struct-fields




### -field Header


<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to ACCESS_ALLOWED_OBJECT_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>ACCESS_ALLOWED_OBJECT_ACE</b> structure.


### -field Mask

An 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> that specifies the access rights the system will allow to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/t-gly">trustee</a>.


### -field Flags

A set of bit flags that indicate whether the <b>ObjectType</b> and <b>InheritedObjectType</b> members are present. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Neither <b>ObjectType</b> nor <b>InheritedObjectType</b> are present. The <b>SidStart</b> member follows immediately after the <b>Flags</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="ACE_OBJECT_TYPE_PRESENT"></a><a id="ace_object_type_present"></a><dl>
<dt><b>ACE_OBJECT_TYPE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
<b>ObjectType</b> is present and contains a <b>GUID</b>. 




If this value is not specified, the <b>InheritedObjectType</b> member follows immediately after the <b>Flags</b> member.

</td>
</tr>
<tr>
<td width="40%"><a id="ACE_INHERITED_OBJECT_TYPE_PRESENT"></a><a id="ace_inherited_object_type_present"></a><dl>
<dt><b>ACE_INHERITED_OBJECT_TYPE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
<b>InheritedObjectType</b> is present and contains a <b>GUID</b>. 




If this value is not specified, all types of child objects can inherit the ACE.

</td>
</tr>
</table>
 


### -field ObjectType

This member exists only if the ACE_OBJECT_TYPE_PRESENT bit is set in the <b>Flags</b> member. Otherwise, the <b>InheritedObjectType</b> member follows immediately after the <b>Flags</b> member. 




If this member exists, it is a 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies a property set, property, extended right, or type of child object. The purpose of this <b>GUID</b> depends on the access rights specified in the <b>Mask</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_CONTROL_ACCESS"></a><a id="ads_right_ds_control_access"></a><dl>
<dt><b>ADS_RIGHT_DS_CONTROL_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> <b>GUID</b> identifies an extended access right.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_CREATE_CHILD"></a><a id="ads_right_ds_create_child"></a><dl>
<dt><b>ADS_RIGHT_DS_CREATE_CHILD</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> <b>GUID</b> identifies a type of child object. The ACE controls the trustee's right to create this type of child object.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_READ_PROP"></a><a id="ads_right_ds_read_prop"></a><dl>
<dt><b>ADS_RIGHT_DS_READ_PROP</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> <b>GUID</b> identifies a property set or property of the object. The ACE controls the trustee's right to read the property or property set.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_WRITE_PROP"></a><a id="ads_right_ds_write_prop"></a><dl>
<dt><b>ADS_RIGHT_DS_WRITE_PROP</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> <b>GUID</b> identifies a property set or property of the object. The ACE controls the trustee's right to write the property or property set.

</td>
</tr>
<tr>
<td width="40%"><a id="ADS_RIGHT_DS_SELF"></a><a id="ads_right_ds_self"></a><dl>
<dt><b>ADS_RIGHT_DS_SELF</b></dt>
</dl>
</td>
<td width="60%">
The <b>ObjectType</b> <b>GUID</b> identifies a validated write.

</td>
</tr>
</table>
 


### -field InheritedObjectType

This member exists only if the ACE_INHERITED_OBJECT_TYPE_PRESENT bit is set in the <b>Flags</b> member. 




If this member exists, it is a 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of child object that can inherit the ACE. Inheritance is also controlled by the inheritance flags in the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>, as well as by any protection against inheritance placed on the child objects.

The offset of this member can vary. If the <b>Flags</b> member does not contain the ACE_OBJECT_TYPE_PRESENT flag, the <b>InheritedObjectType</b> member starts at the offset specified by the <b>ObjectType</b> member.


### -field SidStart

Specifies the first <b>DWORD</b> of a SID that identifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/t-gly">trustee</a> to whom the access rights are granted. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data. 




The offset of this member can vary. If the <b>Flags</b> member is zero, the <b>SidStart</b> member starts at the offset specified by the <b>ObjectType</b> member. If <b>Flags</b> contains only one flag (either ACE_OBJECT_TYPE_PRESENT or ACE_INHERITED_OBJECT_TYPE_PRESENT), the <b>SidStart</b> member starts at the offset specified by the <b>InheritedObjectType</b> member.


## -remarks



If neither the <b>ObjectType</b> nor <b>InheritedObjectType</b> <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> is specified, the <b>ACCESS_ALLOWED_OBJECT_ACE</b> structure has the same semantics as those used by the <a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a> structure. In that case, use the <b>ACCESS_ALLOWED_ACE</b> structure because it is smaller and more efficient.

An ACL that contains an <b>ACCESS_ALLOWED_OBJECT_ACE</b> must specify the ACL_REVISION_DS revision number in its 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> header.

The access rights specified by the <b>Mask</b> member are granted to any <a href="https://docs.microsoft.com/windows/desktop/SecGloss/t-gly">trustee</a> that possesses an enabled SID that matches the SID stored in the <b>SidStart</b> member.

An <b>ACCESS_ALLOWED_OBJECT_ACE</b> structure can be created in an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace">AddAccessAllowedObjectAce</a> function. When this function is used, the correct amount of memory needed to accommodate the GUID structures in the <b>ObjectType</b> and <b>InheritedObjectType</b> members, if one or both of them exists, as well as to accommodate the trustee's SID is automatically allocated. In addition, the values of the <b>Header.AceType</b> and <b>Header.AceSize</b> members are set automatically.	When an <b>ACCESS_ALLOWED_OBJECT_ACE</b> structure is created outside an ACL, sufficient memory must be allocated to accommodate the GUID structures in the <b>ObjectType</b> and <b>InheritedObjectType</b> members, if one or both of them exists, as well as to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory following it. In addition,  the values of the <b>Header.AceType</b> and <b>Header.AceSize</b> members must be set explicitly by the application.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="https://docs.microsoft.com/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace">AddAccessAllowedObjectAce</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a>
 

 

