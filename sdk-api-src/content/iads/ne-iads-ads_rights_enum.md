---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0048_0001
title: ADS_RIGHTS_ENUM (iads.h)
description: Specifies access rights assigned to an Active Directory object.
helpviewer_keywords: ["ADS_RIGHTS_ENUM","ADS_RIGHTS_ENUM enumeration [ADSI]","ADS_RIGHT_ACCESS_SYSTEM_SECURITY","ADS_RIGHT_ACTRL_DS_LIST","ADS_RIGHT_DELETE","ADS_RIGHT_DS_CONTROL_ACCESS","ADS_RIGHT_DS_CREATE_CHILD","ADS_RIGHT_DS_DELETE_CHILD","ADS_RIGHT_DS_DELETE_TREE","ADS_RIGHT_DS_LIST_OBJECT","ADS_RIGHT_DS_READ_PROP","ADS_RIGHT_DS_SELF","ADS_RIGHT_DS_WRITE_PROP","ADS_RIGHT_GENERIC_ALL","ADS_RIGHT_GENERIC_EXECUTE","ADS_RIGHT_GENERIC_READ","ADS_RIGHT_GENERIC_WRITE","ADS_RIGHT_READ_CONTROL","ADS_RIGHT_SYNCHRONIZE","ADS_RIGHT_WRITE_DAC","ADS_RIGHT_WRITE_OWNER","_ds_ads_rights_enum","adsi.ads__rights__enum","adsi.ads_rights_enum","iads/ADS_RIGHTS_ENUM","iads/ADS_RIGHT_ACCESS_SYSTEM_SECURITY","iads/ADS_RIGHT_ACTRL_DS_LIST","iads/ADS_RIGHT_DELETE","iads/ADS_RIGHT_DS_CONTROL_ACCESS","iads/ADS_RIGHT_DS_CREATE_CHILD","iads/ADS_RIGHT_DS_DELETE_CHILD","iads/ADS_RIGHT_DS_DELETE_TREE","iads/ADS_RIGHT_DS_LIST_OBJECT","iads/ADS_RIGHT_DS_READ_PROP","iads/ADS_RIGHT_DS_SELF","iads/ADS_RIGHT_DS_WRITE_PROP","iads/ADS_RIGHT_GENERIC_ALL","iads/ADS_RIGHT_GENERIC_EXECUTE","iads/ADS_RIGHT_GENERIC_READ","iads/ADS_RIGHT_GENERIC_WRITE","iads/ADS_RIGHT_READ_CONTROL","iads/ADS_RIGHT_SYNCHRONIZE","iads/ADS_RIGHT_WRITE_DAC","iads/ADS_RIGHT_WRITE_OWNER"]
old-location: adsi\ads_rights_enum.htm
tech.root: adsi
ms.assetid: ade64dd8-e08c-4f68-b3bf-ccc252272a99
ms.date: 12/05/2018
ms.keywords: ADS_RIGHTS_ENUM, ADS_RIGHTS_ENUM enumeration [ADSI], ADS_RIGHT_ACCESS_SYSTEM_SECURITY, ADS_RIGHT_ACTRL_DS_LIST, ADS_RIGHT_DELETE, ADS_RIGHT_DS_CONTROL_ACCESS, ADS_RIGHT_DS_CREATE_CHILD, ADS_RIGHT_DS_DELETE_CHILD, ADS_RIGHT_DS_DELETE_TREE, ADS_RIGHT_DS_LIST_OBJECT, ADS_RIGHT_DS_READ_PROP, ADS_RIGHT_DS_SELF, ADS_RIGHT_DS_WRITE_PROP, ADS_RIGHT_GENERIC_ALL, ADS_RIGHT_GENERIC_EXECUTE, ADS_RIGHT_GENERIC_READ, ADS_RIGHT_GENERIC_WRITE, ADS_RIGHT_READ_CONTROL, ADS_RIGHT_SYNCHRONIZE, ADS_RIGHT_WRITE_DAC, ADS_RIGHT_WRITE_OWNER, _ds_ads_rights_enum, adsi.ads__rights__enum, adsi.ads_rights_enum, iads/ADS_RIGHTS_ENUM, iads/ADS_RIGHT_ACCESS_SYSTEM_SECURITY, iads/ADS_RIGHT_ACTRL_DS_LIST, iads/ADS_RIGHT_DELETE, iads/ADS_RIGHT_DS_CONTROL_ACCESS, iads/ADS_RIGHT_DS_CREATE_CHILD, iads/ADS_RIGHT_DS_DELETE_CHILD, iads/ADS_RIGHT_DS_DELETE_TREE, iads/ADS_RIGHT_DS_LIST_OBJECT, iads/ADS_RIGHT_DS_READ_PROP, iads/ADS_RIGHT_DS_SELF, iads/ADS_RIGHT_DS_WRITE_PROP, iads/ADS_RIGHT_GENERIC_ALL, iads/ADS_RIGHT_GENERIC_EXECUTE, iads/ADS_RIGHT_GENERIC_READ, iads/ADS_RIGHT_GENERIC_WRITE, iads/ADS_RIGHT_READ_CONTROL, iads/ADS_RIGHT_SYNCHRONIZE, iads/ADS_RIGHT_WRITE_DAC, iads/ADS_RIGHT_WRITE_OWNER
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_RIGHTS_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0048_0001
 - iads/__MIDL___MIDL_itf_ads_0001_0048_0001
 - ADS_RIGHTS_ENUM
 - iads/ADS_RIGHTS_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_RIGHTS_ENUM
---

# ADS_RIGHTS_ENUM enumeration


## -description

The <b>ADS_RIGHTS_ENUM</b> enumeration specifies 
    access rights assigned to an Active Directory object. The 
    <a href="/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods">IADsAccessControlEntry.AccessMask</a> 
    property contains a combination of these values for an Active Directory object.

For more information and a list of possible access right values for file or file share objects, see 
    <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

For more information and a list of possible access right values for registry objects, see 
    <a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registry Key Security and Access Rights</a>.

## -enum-fields

### -field ADS_RIGHT_DELETE:0x10000

The right to delete the object.

### -field ADS_RIGHT_READ_CONTROL:0x20000

The right to read data from the security descriptor of the object, not including the data in the SACL.

### -field ADS_RIGHT_WRITE_DAC:0x40000

The right to modify the discretionary access-control list (DACL) in the object security descriptor.

### -field ADS_RIGHT_WRITE_OWNER:0x80000

The right to assume ownership of the object. The user must be an object trustee. The user cannot transfer the ownership to other users.

### -field ADS_RIGHT_SYNCHRONIZE:0x100000

The right to use the object for synchronization. This enables a thread to wait until the object is in the signaled state.

### -field ADS_RIGHT_ACCESS_SYSTEM_SECURITY:0x1000000

The right to get or set the SACL in the object security descriptor.

### -field ADS_RIGHT_GENERIC_READ:0x80000000

The right to read permissions on this object, read all the properties on this object, list this object name when the parent container is listed, and list the contents of this object if it is a container.

### -field ADS_RIGHT_GENERIC_WRITE:0x40000000

The right to read permissions on this object, write all the properties on this object, and perform all validated writes to this object.

### -field ADS_RIGHT_GENERIC_EXECUTE:0x20000000

The right to read permissions on, and list the contents of,  a container object.

### -field ADS_RIGHT_GENERIC_ALL:0x10000000

The right to create or delete child objects, delete a subtree, read and write properties, examine child objects and the object itself, add and remove the object from the directory, and read or write with an extended right.

### -field ADS_RIGHT_DS_CREATE_CHILD:0x1

The right to create child objects of the object. The <b>ObjectType</b> member of an ACE can contain a <b>GUID</b> that identifies the type of child object whose creation is controlled. If <b>ObjectType</b> does not contain a <b>GUID</b>, the ACE controls the creation of all child object types.

### -field ADS_RIGHT_DS_DELETE_CHILD:0x2

The right to delete child objects of the object. The <b>ObjectType</b> member of an ACE can contain a <b>GUID</b> that identifies a type of child object whose deletion is controlled. If <b>ObjectType</b> does not contain a <b>GUID</b>, the ACE controls the deletion of all child object types.

### -field ADS_RIGHT_ACTRL_DS_LIST:0x4

The right to list child objects of this object. For more information about this right, see <a href="/windows/desktop/AD/controlling-object-visibility">Controlling Object Visibility</a>.

### -field ADS_RIGHT_DS_SELF:0x8

The right to perform an operation controlled by a validated write access right. The <b>ObjectType</b> member of an ACE can contain a <b>GUID</b> that identifies the validated write. If <b>ObjectType</b> does not contain a <b>GUID</b>, the ACE controls the rights to perform all valid write operations associated with the object.

### -field ADS_RIGHT_DS_READ_PROP:0x10

The right to read properties of the object. The <b>ObjectType</b> member of an ACE can contain a <b>GUID</b> that identifies a property set or property. If <b>ObjectType</b> does not contain a <b>GUID</b>, the ACE controls the right to read all of the object properties.

### -field ADS_RIGHT_DS_WRITE_PROP:0x20

The right to write properties of the object. The <b>ObjectType</b> member of an ACE can contain a <b>GUID</b> that identifies a property set or property. If <b>ObjectType</b> does not contain a <b>GUID</b>, the ACE controls the right to write all of the object properties.

### -field ADS_RIGHT_DS_DELETE_TREE:0x40

The right to delete all child objects of this object, regardless of the permissions of the child objects.

### -field ADS_RIGHT_DS_LIST_OBJECT:0x80

The right to list a particular object. If the user is not granted such a right, and the user does not have <b>ADS_RIGHT_ACTRL_DS_LIST</b> set on the object parent, the object is hidden from the user. This right is ignored if the third character of the <a href="/windows/desktop/ADSchema/a-dsheuristics">dSHeuristics</a> property is '0' or not set. For more information, see <a href="/windows/desktop/AD/controlling-object-visibility">Controlling Object Visibility</a>.

### -field ADS_RIGHT_DS_CONTROL_ACCESS:0x100

The right to perform an operation controlled by an extended access right. The <b>ObjectType</b> member of an ACE can contain a <b>GUID</b> that identifies the extended right. If <b>ObjectType</b> does not contain a <b>GUID</b>, the ACE controls the right to perform all extended right operations associated with the object.

## -remarks

To assign access rights to an object, set the <b>AccessMask</b> field of an
    access-control entry (ACE) to a combination of the constants defined in this enumeration. In addition to the 
    <b>AccessMask</b> field, an ACE can have other fields, including 
    <b>ACEType</b>, <b>ACEFlags</b>, 
    <b>ObjectType</b>, <b>InheritedObjectType</b>, 
    <b>Flags</b>, and <b>Trustee</b>. The 
    <a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a> interface provides property 
    methods to obtain and modify these fields.

The <b>ObjectType</b> field specifies a <b>GUID</b> that 
    identifies the property set, property, extended right, or type of child object to which the ACE applies. The 
    <b>InheritedObjectType</b> field specifies a <b>GUID</b> that 
    identifies the type of child object that can inherit the ACE. The <b>Trustee</b> field 
    identifies the security principal to whom the ACE allows or denies the specified access rights.

For more information about <b>ACEType</b>, <b>ACEFlags</b>, and 
    <b>Flags</b>, see <a href="/windows/win32/api/iads/ne-iads-ads_acetype_enum">ADS_ACETYPE_ENUM</a>, 
    <a href="/windows/win32/api/iads/ne-iads-ads_aceflag_enum">ADS_ACEFLAG_ENUM</a>.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic 
    constants as defined above. Instead, use the numerical constants to set the appropriate flags in your VBScript 
    application. To use the symbolic constants as a good programming practice, write explicit declarations of such 
    constants, as done here, in your VBScript applications.</div>
<div> </div>
The specific access rights granted by the four generic rights enumerations 
    (<b>ADS_RIGHT_GENERIC_xxx</b>) is dependent on the specific ADSI service provider being 
    accessed. For Active Directory, these generic rights are defined in the Ntdsapi.h header file as 
    <b>DS_GENERIC_READ</b>, <b>DS_GENERIC_WRITE</b>, 
    <b>DS_GENERIC_EXECUTE</b>, and <b>DS_GENERIC_ALL</b>. For more 
    information about how to use the  Access Right and Access Masks, see 
    <a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_acetype_enum">ADS_ACETYPE_ENUM</a>



<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/access-rights-and-access-masks">Access Rights and Access Masks</a>



<a href="/windows/desktop/SecAuthZ/directory-services-access-rights">Directory Services Access Rights</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods">IADsAccessControlEntry.AccessMask</a>
