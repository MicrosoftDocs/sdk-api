---
UID: NS:accctrl._OBJECTS_AND_NAME_A
title: "_OBJECTS_AND_NAME_A"
author: windows-sdk-content
description: Contains a string that identifies a trustee by name and additional strings that identify the object types of an object-specific access control entry (ACE).
old-location: security\objects_and_name.htm
tech.root: secauthz
ms.assetid: ad91a302-f693-44e9-9655-ec4488ff78c4
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*POBJECTS_AND_NAME_A, ACE_INHERITED_OBJECT_TYPE_PRESENT, ACE_OBJECT_TYPE_PRESENT, OBJECTS_AND_NAME, OBJECTS_AND_NAME structure [Security], OBJECTS_AND_NAME_, OBJECTS_AND_NAME_A, OBJECTS_AND_NAME_W, POBJECTS_AND_NAME, POBJECTS_AND_NAME structure pointer [Security], _OBJECTS_AND_NAME_A, _win32_objects_and_name_str, accctrl/OBJECTS_AND_NAME, accctrl/OBJECTS_AND_NAME_A, accctrl/OBJECTS_AND_NAME_W, accctrl/POBJECTS_AND_NAME, security.objects_and_name"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OBJECTS_AND_NAME_W (Unicode) and OBJECTS_AND_NAME_A (ANSI)
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
 - OBJECTS_AND_NAME
 - OBJECTS_AND_NAME_A
 - OBJECTS_AND_NAME_W
product: Windows
targetos: Windows
req.typenames: OBJECTS_AND_NAME_A, *POBJECTS_AND_NAME_A
req.redist: 
---

# _OBJECTS_AND_NAME_A structure


## -description


The <b>OBJECTS_AND_NAME</b> structure contains a string that identifies a trustee by name and additional strings that identify the object types of an object-specific <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE).


## -struct-fields




### -field ObjectsPresent

Indicates whether the <b>ObjectTypeName</b> and <b>InheritedObjectTypeName</b> members contain strings. This parameter can be a combination of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACE_OBJECT_TYPE_PRESENT"></a><a id="ace_object_type_present"></a><dl>
<dt><b>ACE_OBJECT_TYPE_PRESENT</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The <b>ObjectTypeName</b> member contains a string.

</td>
</tr>
<tr>
<td width="40%"><a id="ACE_INHERITED_OBJECT_TYPE_PRESENT"></a><a id="ace_inherited_object_type_present"></a><dl>
<dt><b>ACE_INHERITED_OBJECT_TYPE_PRESENT</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The <b>InheritedObjectTypeName</b> member contains a string.

</td>
</tr>
</table>
 


### -field ObjectType

Specifies a value from the 
<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a> enumeration that indicates the type of object.


### -field ObjectTypeName

A pointer to a null-terminated string that identifies the type of object to which the ACE applies.

This string must be a valid <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">LDAP</a> display name in the Active Directory schema.


### -field InheritedObjectTypeName

A pointer to a null-terminated string that identifies the type of object that can inherit the ACE. 




This string must be a valid <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">LDAP</a> display name in the Active Directory schema.

If the ACE_INHERITED_OBJECT_TYPE_PRESENT bit is not set in the <b>ObjectsPresent</b> member, the <b>InheritedObjectTypeName</b> member is ignored, and all types of child objects can inherit the ACE. Otherwise, only the specified object type can inherit the ACE. In either case, inheritance is also controlled by the inheritance flags in the <a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>structure as well as by any protection against inheritance placed on the child objects.


### -field ptstrName

A pointer to a null-terminated string that contains the name of the trustee.


## -remarks



The <b>ptstrName</b> member of a <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure can be a pointer to an <b>OBJECTS_AND_NAME</b> structure. This enables functions such as <a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a> and <a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a> to store object-specific ACE information in the <b>Trustee</b> member of an <a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/d23f15d6-0453-4aaf-a2db-7528b551a992">ACE_HEADER</a>



<a href="https://msdn.microsoft.com/6fe09542-10dd-439c-adf8-a4e06943ddb2">EXPLICIT_ACCESS</a>



<a href="https://msdn.microsoft.com/186aa6aa-efc3-4f8a-acad-e257da3dac0b">GetExplicitEntriesFromAcl</a>



<a href="https://msdn.microsoft.com/77ba8a3c-01e5-4a3e-835f-c7b9ef60035a">OBJECTS_AND_SID</a>



<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/05960fc1-1ad2-4c19-a65c-62259af5e18c">SetEntriesInAcl</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

