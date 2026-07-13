---
UID: NS:accctrl._OBJECTS_AND_NAME_A
title: OBJECTS_AND_NAME_A (accctrl.h)
description: Contains a string that identifies a trustee by name and additional strings that identify the object types of an object-specific access control entry (ACE). (ANSI)
helpviewer_keywords: ["*POBJECTS_AND_NAME_A","ACE_INHERITED_OBJECT_TYPE_PRESENT","ACE_OBJECT_TYPE_PRESENT","OBJECTS_AND_NAME","OBJECTS_AND_NAME structure [Security]","OBJECTS_AND_NAME_","OBJECTS_AND_NAME_A","OBJECTS_AND_NAME_W","POBJECTS_AND_NAME","POBJECTS_AND_NAME structure pointer [Security]","_win32_objects_and_name_str","accctrl/OBJECTS_AND_NAME","accctrl/OBJECTS_AND_NAME_A","accctrl/OBJECTS_AND_NAME_W","accctrl/POBJECTS_AND_NAME","security.objects_and_name"]
old-location: security\objects_and_name.htm
tech.root: security
ms.assetid: ad91a302-f693-44e9-9655-ec4488ff78c4
ms.date: 12/05/2018
ms.keywords: '*POBJECTS_AND_NAME_A, ACE_INHERITED_OBJECT_TYPE_PRESENT, ACE_OBJECT_TYPE_PRESENT, OBJECTS_AND_NAME, OBJECTS_AND_NAME structure [Security], OBJECTS_AND_NAME_, OBJECTS_AND_NAME_A, OBJECTS_AND_NAME_W, POBJECTS_AND_NAME, POBJECTS_AND_NAME structure pointer [Security], _win32_objects_and_name_str, accctrl/OBJECTS_AND_NAME, accctrl/OBJECTS_AND_NAME_A, accctrl/OBJECTS_AND_NAME_W, accctrl/POBJECTS_AND_NAME, security.objects_and_name'
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
targetos: Windows
req.typenames: OBJECTS_AND_NAME_A, *POBJECTS_AND_NAME_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OBJECTS_AND_NAME_A
 - accctrl/_OBJECTS_AND_NAME_A
 - POBJECTS_AND_NAME_A
 - accctrl/POBJECTS_AND_NAME_A
 - OBJECTS_AND_NAME_A
 - accctrl/OBJECTS_AND_NAME_A
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
 - OBJECTS_AND_NAME
 - OBJECTS_AND_NAME_A
 - OBJECTS_AND_NAME_W
---

# OBJECTS_AND_NAME_A structure


## -description

The <b>OBJECTS_AND_NAME</b> structure contains a string that identifies a trustee by name and additional strings that identify the object types of an object-specific <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE).

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
<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a> enumeration that indicates the type of object.

### -field ObjectTypeName

A pointer to a null-terminated string that identifies the type of object to which the ACE applies.

This string must be a valid <a href="/windows/desktop/SecGloss/l-gly">LDAP</a> display name in the Active Directory schema.

If the ACE_INHERITED_OBJECT_TYPE_PRESENT bit is not set in the <b>ObjectsPresent</b> member, the <b>ObjectTypeName</b> member is ignored.

### -field InheritedObjectTypeName

A pointer to a null-terminated string that identifies the type of object that can inherit the ACE. 




This string must be a valid <a href="/windows/desktop/SecGloss/l-gly">LDAP</a> display name in the Active Directory schema.

If the ACE_INHERITED_OBJECT_TYPE_PRESENT bit is not set in the <b>ObjectsPresent</b> member, the <b>InheritedObjectTypeName</b> member is ignored, and all types of child objects can inherit the ACE. Otherwise, only the specified object type can inherit the ACE. In either case, inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure as well as by any protection against inheritance placed on the child objects.

### -field ptstrName

A pointer to a null-terminated string that contains the name of the trustee.

## -remarks

The <b>ptstrName</b> member of a <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE_A</a> structure is a pointer to an <b>OBJECTS_AND_NAME_A</b> structure if the <b>TrusteeForm</b> is <b>TRUSTEE_IS_OBJECTS_AND_NAME</b>. This enables functions such as <a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a> and <a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a> to store object-specific ACE information in the <b>Trustee</b> member of an <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure.





> [!NOTE]
> The accctrl.h header defines OBJECTS_AND_NAME_ as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_sid">OBJECTS_AND_SID</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE_A</a>
