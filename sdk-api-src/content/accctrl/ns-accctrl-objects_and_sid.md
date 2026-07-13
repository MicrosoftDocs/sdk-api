---
UID: NS:accctrl._OBJECTS_AND_SID
title: OBJECTS_AND_SID (accctrl.h)
description: Contains a security identifier (SID) that identifies a trustee and GUIDs that identify the object types of an object-specific access control entry (ACE).
helpviewer_keywords: ["*POBJECTS_AND_SID","ACE_INHERITED_OBJECT_TYPE_PRESENT","ACE_OBJECT_TYPE_PRESENT","OBJECTS_AND_SID","OBJECTS_AND_SID structure [Security]","POBJECTS_AND_SID","POBJECTS_AND_SID structure pointer [Security]","_OBJECTS_AND_SID","_win32_objects_and_sid_str","accctrl/OBJECTS_AND_SID","accctrl/POBJECTS_AND_SID","security.objects_and_sid"]
old-location: security\objects_and_sid.htm
tech.root: security
ms.assetid: 77ba8a3c-01e5-4a3e-835f-c7b9ef60035a
ms.date: 12/05/2018
ms.keywords: '*POBJECTS_AND_SID, ACE_INHERITED_OBJECT_TYPE_PRESENT, ACE_OBJECT_TYPE_PRESENT, OBJECTS_AND_SID, OBJECTS_AND_SID structure [Security], POBJECTS_AND_SID, POBJECTS_AND_SID structure pointer [Security], _OBJECTS_AND_SID, _win32_objects_and_sid_str, accctrl/OBJECTS_AND_SID, accctrl/POBJECTS_AND_SID, security.objects_and_sid'
req.header: accctrl.h
req.include-header: 
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
req.typenames: OBJECTS_AND_SID, *POBJECTS_AND_SID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OBJECTS_AND_SID
 - accctrl/_OBJECTS_AND_SID
 - POBJECTS_AND_SID
 - accctrl/POBJECTS_AND_SID
 - OBJECTS_AND_SID
 - accctrl/OBJECTS_AND_SID
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
 - OBJECTS_AND_SID
---

# OBJECTS_AND_SID structure


## -description

The <b>OBJECTS_AND_SID</b> structure contains a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) that identifies a trustee and GUIDs that identify the object types of an object-specific <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE).

## -struct-fields

### -field ObjectsPresent

Indicates whether the <b>ObjectTypeGuid</b> and <b>InheritedObjectTypeGuid</b> members contain GUIDs. This parameter can be a combination of the following values. 




					

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
The <b>ObjectTypeGuid</b> member contains a GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="ACE_INHERITED_OBJECT_TYPE_PRESENT"></a><a id="ace_inherited_object_type_present"></a><dl>
<dt><b>ACE_INHERITED_OBJECT_TYPE_PRESENT</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The <b>InheritedObjectTypeGuid</b> member contains a GUID.

</td>
</tr>
</table>

### -field ObjectTypeGuid

A 
<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of object, property set, or property protected by the ACE. If this ACE is inherited, the GUID identifies the type of object, property set, or property protected by the inherited ACE. This GUID must be a valid schema identifier in the Active Directory schema.

If the ACE_OBJECT_TYPE_PRESENT bit is not set in the <b>ObjectsPresent</b> member, the <b>ObjectTypeGuid</b> member is ignored, and the ACE protects the object to which the ACL is assigned.

### -field InheritedObjectTypeGuid

A <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> structure that identifies the type of object that can inherit the ACE. This GUID must be a valid schema identifier in the Active Directory schema.

If the ACE_INHERITED_OBJECT_TYPE_PRESENT bit is not set in the <b>ObjectsPresent</b> member, the <b>InheritedObjectTypeGuid</b> member is ignored, and all types of child objects can inherit the ACE. Otherwise, only the specified object type can inherit the ACE. In either case, inheritance is also controlled by the inheritance flags in the <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure as well as by any protection against inheritance placed on the child objects.

### -field pSid

A pointer to the SID of the trustee to whom the ACE applies.

## -remarks

The <b>ptstrName</b> member of a <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure can be a pointer to an <b>OBJECTS_AND_SID</b> structure. This enables functions such as <a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a> and <a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a> to store object-specific ACE information in the <b>Trustee</b> member of an <a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a> structure.

When you use this structure in a call to <a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a>, <b>ObjectTypeGuid</b> and <b>InheritedObjectTypeGuid</b> must be valid schema identifiers in the Active Directory schema. The system does not verify the GUIDs; they are used as is.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-explicit_access_a">EXPLICIT_ACCESS</a>



<a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-getexplicitentriesfromacla">GetExplicitEntriesFromAcl</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-setentriesinacla">SetEntriesInAcl</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>