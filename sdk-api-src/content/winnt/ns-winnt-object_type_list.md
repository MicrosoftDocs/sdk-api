---
UID: NS:winnt._OBJECT_TYPE_LIST
title: OBJECT_TYPE_LIST (winnt.h)
description: Identifies an object type element in a hierarchy of object types.
helpviewer_keywords: ["*POBJECT_TYPE_LIST","ACCESS_OBJECT_GUID","ACCESS_PROPERTY_GUID","ACCESS_PROPERTY_SET_GUID","OBJECT_TYPE_LIST","OBJECT_TYPE_LIST structure [Security]","POBJECT_TYPE_LIST","POBJECT_TYPE_LIST structure pointer [Security]","_OBJECT_TYPE_LIST","_win32_object_type_list_str","security.object_type_list","winnt/OBJECT_TYPE_LIST","winnt/POBJECT_TYPE_LIST"]
old-location: security\object_type_list.htm
tech.root: security
ms.assetid: c729ff1a-65f3-4f6f-84dd-5700aead75ce
ms.date: 12/05/2018
ms.keywords: '*POBJECT_TYPE_LIST, ACCESS_OBJECT_GUID, ACCESS_PROPERTY_GUID, ACCESS_PROPERTY_SET_GUID, OBJECT_TYPE_LIST, OBJECT_TYPE_LIST structure [Security], POBJECT_TYPE_LIST, POBJECT_TYPE_LIST structure pointer [Security], _OBJECT_TYPE_LIST, _win32_object_type_list_str, security.object_type_list, winnt/OBJECT_TYPE_LIST, winnt/POBJECT_TYPE_LIST'
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
req.typenames: OBJECT_TYPE_LIST, *POBJECT_TYPE_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OBJECT_TYPE_LIST
 - winnt/_OBJECT_TYPE_LIST
 - POBJECT_TYPE_LIST
 - winnt/POBJECT_TYPE_LIST
 - OBJECT_TYPE_LIST
 - winnt/OBJECT_TYPE_LIST
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
 - OBJECT_TYPE_LIST
---

# OBJECT_TYPE_LIST structure


## -description

The <b>OBJECT_TYPE_LIST</b> structure identifies an object type element in a hierarchy of object types. The 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype">AccessCheckByType</a> functions use an array of <b>OBJECT_TYPE_LIST</b> structures to define a hierarchy of an object and its subobjects, such as property sets and properties.

## -struct-fields

### -field Level

Specifies the level of the object type in the hierarchy of an object and its subobjects. Level zero indicates the object itself. Level one indicates a subobject of the object, such as a property set. Level two indicates a subobject of the level one subobject, such as a property. There can be a maximum of five levels numbered zero through four. 




Directory service objects use the following level values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACCESS_OBJECT_GUID"></a><a id="access_object_guid"></a><dl>
<dt><b>ACCESS_OBJECT_GUID</b></dt>
</dl>
</td>
<td width="60%">
Indicates the object itself at level zero.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_PROPERTY_SET_GUID"></a><a id="access_property_set_guid"></a><dl>
<dt><b>ACCESS_PROPERTY_SET_GUID</b></dt>
</dl>
</td>
<td width="60%">
Indicates a property set at level one.

</td>
</tr>
<tr>
<td width="40%"><a id="ACCESS_PROPERTY_GUID"></a><a id="access_property_guid"></a><dl>
<dt><b>ACCESS_PROPERTY_GUID</b></dt>
</dl>
</td>
<td width="60%">
Indicates a property at level two.

</td>
</tr>
</table>

### -field Sbz

Should be zero. Reserved for future use.

### -field ObjectType

A pointer to the GUID for the object or subobject.

## -see-also

<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype">AccessCheckByType</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytypeandauditalarma">AccessCheckByTypeAndAuditAlarm</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist">AccessCheckByTypeResultList</a>



<a href="/windows/desktop/api/winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma">AccessCheckByTypeResultListAndAuditAlarm</a>