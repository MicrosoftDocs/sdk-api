---
UID: NS:authif._RADIUS_ATTRIBUTE_ARRAY
title: RADIUS_ATTRIBUTE_ARRAY (authif.h)
description: The RADIUS_ATTRIBUTE_ARRAY structure represents an array of attributes.
helpviewer_keywords: ["*PRADIUS_ATTRIBUTE_ARRAY","PRADIUS_ATTRIBUTE_ARRAY","PRADIUS_ATTRIBUTE_ARRAY structure pointer [Network Policy Server]","RADIUS_ATTRIBUTE_ARRAY","RADIUS_ATTRIBUTE_ARRAY structure [Network Policy Server]","_ias_radius_attribute_array","authif/PRADIUS_ATTRIBUTE_ARRAY","authif/RADIUS_ATTRIBUTE_ARRAY","ias.radius_attribute_array","nps.IAS_radius_attribute_array"]
old-location: nps\IAS_radius_attribute_array.htm
tech.root: Nps
ms.assetid: 2eec8b05-c74d-4876-a475-0be7f60014d0
ms.date: 12/05/2018
ms.keywords: '*PRADIUS_ATTRIBUTE_ARRAY, PRADIUS_ATTRIBUTE_ARRAY, PRADIUS_ATTRIBUTE_ARRAY structure pointer [Network Policy Server], RADIUS_ATTRIBUTE_ARRAY, RADIUS_ATTRIBUTE_ARRAY structure [Network Policy Server], _ias_radius_attribute_array, authif/PRADIUS_ATTRIBUTE_ARRAY, authif/RADIUS_ATTRIBUTE_ARRAY, ias.radius_attribute_array, nps.IAS_radius_attribute_array'
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: RADIUS_ATTRIBUTE_ARRAY, *PRADIUS_ATTRIBUTE_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_ATTRIBUTE_ARRAY
 - authif/_RADIUS_ATTRIBUTE_ARRAY
 - PRADIUS_ATTRIBUTE_ARRAY
 - authif/PRADIUS_ATTRIBUTE_ARRAY
 - RADIUS_ATTRIBUTE_ARRAY
 - authif/RADIUS_ATTRIBUTE_ARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_ATTRIBUTE_ARRAY
---

# RADIUS_ATTRIBUTE_ARRAY structure


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure represents an array of attributes.

## -struct-fields

### -field cbSize

Specifies the size of the structure.

### -field Add

Pointer to the <a href="/previous-versions/ms688246(v=vs.85)">Add</a> function provided by NPS. NPS sets the value of the member.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes to which to append the specified attribute.

The 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> and 
<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### pAttr

Pointer to a 
<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">RADIUS_ATTRIBUTE</a> structure for the attribute to append to the array.

### -field AttributeAt

Pointer to the <a href="/previous-versions/ms688253(v=vs.85)">AttributeAt</a> function provided by NPS. NPS sets the value of the member.
   

The 
<a href="/previous-versions/ms688253(v=vs.85)">AttributeAt</a> function returns a const pointer to the specified attribute within the array.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes from which to retrieve the specified attribute.

The 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> and 
<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### dwIndex

Specifies the index of the attribute to retrieve. The function returns <b>NULL</b> if this index is out of range.

Use the 
<a href="/previous-versions/ms688277(v=vs.85)">GetSize</a> function to determine the size of the array. The largest index is one less than the size of the array.

### -field GetSize

Pointer to the <a href="/previous-versions/ms688277(v=vs.85)">GetSize</a> function provided by NPS. NPS sets the value of the member.

The 
<a href="/previous-versions/ms688277(v=vs.85)">GetSize</a> function returns the size of the attribute array.

The 
<a href="/previous-versions/ms688277(v=vs.85)">GetSize</a> function returns the size of the attribute array, not the largest index. Because attribute arrays use zero-based indexes, the size of the array is one greater than the largest index.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes for which to retrieve the size.

The 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> and 
<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.

### -field InsertAt

Pointer to the <a href="/previous-versions/ms688296(v=vs.85)">InsertAt</a> function provided by NPS. NPS sets the value of the member.

The 
<a href="/previous-versions/ms688296(v=vs.85)">InsertAt</a> function inserts the specified attribute at the specified index in the array.

When the 
<a href="/previous-versions/ms688296(v=vs.85)">InsertAt</a> function inserts a new attribute into the array, it increments the index of the pre-existing attribute at this index. Similarly, it increments the index of any pre-existing attributes at higher indexes.

To append an attribute to the end of the attribute array, use the 
<a href="/previous-versions/ms688246(v=vs.85)">Add</a> function.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes in which to insert the specified attribute.

The 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> and 
<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### dwIndex

Specifies the index at which to insert the specified attribute.

Use the 
<a href="/previous-versions/ms688277(v=vs.85)">GetSize</a> function to determine the size of the array. The largest index is one less than the size of the array.



#### pAttr

Pointer to a 
<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">RADIUS_ATTRIBUTE</a> structure for the attribute to insert into the array.

### -field RemoveAt

Pointer to the <a href="/previous-versions/ms688452(v=vs.85)">RemoveAt</a> function provided by NPS. NPS sets the value of the member.

The 
<a href="/previous-versions/ms688452(v=vs.85)">RemoveAt</a> function removes the attribute at the specified index in the array.

When the <a href="/previous-versions/ms688452(v=vs.85)">RemoveAt</a> function removes an attribute from the array, it decrements the index of any pre-existing attributes at higher indexes.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes from which to remove the specified attribute.

The 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> and 
<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### dwIndex

Specifies the index of the attribute to remove.

Use the 
<a href="/previous-versions/ms688277(v=vs.85)">GetSize</a> function to determine the size of the array. The largest index is one less than the size of the array.

### -field SetAt

Pointer to the <a href="/previous-versions/ms688456(v=vs.85)">SetAt</a> function provided by NPS. NPS sets the value of the member.

The 
<a href="/previous-versions/ms688456(v=vs.85)">SetAt</a> function replaces the attribute at the specified index with the specified attribute.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes that contains the attribute to replace.

The 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> and 
<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### dwIndex

Specifies the index of the attribute to replace.

Use the 
<a href="/previous-versions/ms688277(v=vs.85)">GetSize</a> function to determine the size of the array. The largest index is one less than the size of the array.



#### pAttr

Pointer to a 
<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">RADIUS_ATTRIBUTE</a> structure. The attribute represented by this structure replaces the attribute at the specified index.

## -remarks

The Extension DLL must not modify this structure. Changes to the array of attributes should be made by calling the functions provided as members of this structure.

This structure is used by Extension DLLs that export 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a>. The functions that add attributes to the array:

<a href="/previous-versions/ms688246(v=vs.85)">Add</a>
<a href="/previous-versions/ms688296(v=vs.85)">InsertAt</a>
copy the contents of the caller-supplied 
<a href="/windows/desktop/api/authif/ns-authif-radius_attribute">RADIUS_ATTRIBUTE</a> structure. Therefore, Extension DLLs that export 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a> need not export 
<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes">RadiusExtensionFreeAttributes</a>.

This structure is returned by the functions 
<a href="/previous-versions/ms688263(v=vs.85)">GetRequest</a> and 
<a href="/previous-versions/ms688270(v=vs.85)">GetResponse</a>.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-structures">NPS Extensions Structures</a>



<a href="/windows/desktop/api/authif/ns-authif-radius_extension_control_block">RADIUS_EXTENSION_CONTROL_BLOCK</a>



<a href="/windows/desktop/api/authif/nc-authif-pradius_extension_process_2">RadiusExtensionProcess2</a>