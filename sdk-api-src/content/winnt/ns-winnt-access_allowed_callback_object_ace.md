---
UID: NS:winnt._ACCESS_ALLOWED_CALLBACK_OBJECT_ACE
title: ACCESS_ALLOWED_CALLBACK_OBJECT_ACE (winnt.h)
description: Defines an access control entry (ACE) that controls allowed access to an object, property set, or property.
helpviewer_keywords: ["*PACCESS_ALLOWED_CALLBACK_OBJECT_ACE","0","ACCESS_ALLOWED_CALLBACK_OBJECT_ACE","ACCESS_ALLOWED_CALLBACK_OBJECT_ACE structure [Security]","ACE_INHERITED_OBJECT_TYPE_PRESENT","ACE_OBJECT_TYPE_PRESENT","ADS_RIGHT_DS_CONTROL_ACCESS","ADS_RIGHT_DS_CREATE_CHILD","ADS_RIGHT_DS_READ_PROP","ADS_RIGHT_DS_SELF","ADS_RIGHT_DS_WRITE_PROP","PACCESS_ALLOWED_CALLBACK_OBJECT_ACE","PACCESS_ALLOWED_CALLBACK_OBJECT_ACE structure pointer [Security]","_ACCESS_ALLOWED_CALLBACK_OBJECT_ACE","security.access_allowed_callback_object_ace","winnt/ACCESS_ALLOWED_CALLBACK_OBJECT_ACE","winnt/PACCESS_ALLOWED_CALLBACK_OBJECT_ACE"]
old-location: security\access_allowed_callback_object_ace.htm
tech.root: security
ms.assetid: 83b00ef3-f7b2-455e-8f3f-01b1da6024b7
ms.date: 12/05/2018
ms.keywords: '*PACCESS_ALLOWED_CALLBACK_OBJECT_ACE, 0, ACCESS_ALLOWED_CALLBACK_OBJECT_ACE, ACCESS_ALLOWED_CALLBACK_OBJECT_ACE structure [Security], ACE_INHERITED_OBJECT_TYPE_PRESENT, ACE_OBJECT_TYPE_PRESENT, ADS_RIGHT_DS_CONTROL_ACCESS, ADS_RIGHT_DS_CREATE_CHILD, ADS_RIGHT_DS_READ_PROP, ADS_RIGHT_DS_SELF, ADS_RIGHT_DS_WRITE_PROP, PACCESS_ALLOWED_CALLBACK_OBJECT_ACE, PACCESS_ALLOWED_CALLBACK_OBJECT_ACE structure pointer [Security], _ACCESS_ALLOWED_CALLBACK_OBJECT_ACE, security.access_allowed_callback_object_ace, winnt/ACCESS_ALLOWED_CALLBACK_OBJECT_ACE, winnt/PACCESS_ALLOWED_CALLBACK_OBJECT_ACE'
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
targetos: Windows
req.typenames: ACCESS_ALLOWED_CALLBACK_OBJECT_ACE, *PACCESS_ALLOWED_CALLBACK_OBJECT_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACCESS_ALLOWED_CALLBACK_OBJECT_ACE
 - winnt/_ACCESS_ALLOWED_CALLBACK_OBJECT_ACE
 - PACCESS_ALLOWED_CALLBACK_OBJECT_ACE
 - winnt/PACCESS_ALLOWED_CALLBACK_OBJECT_ACE
 - ACCESS_ALLOWED_CALLBACK_OBJECT_ACE
 - winnt/ACCESS_ALLOWED_CALLBACK_OBJECT_ACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - ACCESS_ALLOWED_CALLBACK_OBJECT_ACE
---

# ACCESS_ALLOWED_CALLBACK_OBJECT_ACE structure


## -description

The <b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</b> structure defines an  <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) that controls allowed access to an object, property set, or property.   The ACE contains a set of access rights, a <b>GUID</b> that identifies the type of object, and a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that identifies the <a href="/windows/desktop/SecGloss/t-gly">trustee</a> to whom the system will grant access. The ACE also contains a <b>GUID</b> and a set of flags that control inheritance of the ACE by child objects.

When the <a href="/windows/desktop/api/authz/nf-authz-authzaccesscheck">AuthzAccessCheck</a> function is called, each <b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</b> structure contained in the DACL of a <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure passed through a pointer to the <b>AuthzAccessCheck</b> function invokes a call to the application-defined <a href="/windows/desktop/SecAuthZ/authzaccesscheckcallback">AuthzAccessCheckCallback</a> function, in which a pointer to the <b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</b> structure found is passed in the <i>pAce</i> parameter.

## -struct-fields

### -field Header

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of ACE. It also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure should be set to ACCESS_ALLOWED_CALLBACK_OBJECT_ACE_TYPE, and the <b>AceSize</b> member should be set to the total number of bytes allocated for the <b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</b> structure.

### -field Mask

An 
<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a> that specifies the access rights the system will allow to the <a href="/windows/desktop/SecGloss/t-gly">trustee</a>.

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
<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>, as well as by any protection against inheritance placed on the child objects.

The offset of this member can vary. If the <b>Flags</b> member does not contain the ACE_OBJECT_TYPE_PRESENT flag, the <b>InheritedObjectType</b> member starts at the offset specified by the <b>ObjectType</b> member.

### -field SidStart

The first <b>DWORD</b> of a trustee's SID. The remaining bytes of the SID  are stored in contiguous memory after the <b>SidStart</b> member. This SID can be appended with application data.

## -remarks

If neither the <b>ObjectType</b> nor <b>InheritedObjectType</b> <b>GUID</b> is specified, the <b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</b> structure has the same semantics as those used by the <a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_callback_ace">ACCESS_ALLOWED_CALLBACK_ACE</a> structure. In that case, use the <b>ACCESS_ALLOWED_CALLBACK_ACE</b> structure because it is smaller and more efficient.

An ACL that contains an <b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</b> must specify the ACL_REVISION_DS revision number in its 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> header.

The access rights specified by the <b>Mask</b> member are granted to any <a href="/windows/desktop/SecGloss/t-gly">trustee</a> that possesses an enabled SID that matches the SID stored in the <b>SidStart</b> member.

When an <b>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</b> structure is created, sufficient memory must be allocated to accommodate the GUID structures in the <b>ObjectType</b> and <b>InheritedObjectType</b> members, if one or both of them exists, as well as to accommodate the complete SID of the trustee in the <b>SidStart</b> member and the contiguous memory that follows it.

## -see-also

<a href="/windows/desktop/SecAuthZ/ace">ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace">AddAuditAccessObjectAce</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>