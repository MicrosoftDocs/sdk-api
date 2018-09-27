---
UID: NS:authif._RADIUS_ATTRIBUTE_ARRAY
title: "_RADIUS_ATTRIBUTE_ARRAY"
author: windows-sdk-content
description: The RADIUS_ATTRIBUTE_ARRAY structure represents an array of attributes.
old-location: nps\IAS_radius_attribute_array.htm
tech.root: Nps
ms.assetid: 2eec8b05-c74d-4876-a475-0be7f60014d0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PRADIUS_ATTRIBUTE_ARRAY, PRADIUS_ATTRIBUTE_ARRAY, PRADIUS_ATTRIBUTE_ARRAY structure pointer [Network Policy Server], RADIUS_ATTRIBUTE_ARRAY, RADIUS_ATTRIBUTE_ARRAY structure [Network Policy Server], _RADIUS_ATTRIBUTE_ARRAY, _ias_radius_attribute_array, authif/PRADIUS_ATTRIBUTE_ARRAY, authif/RADIUS_ATTRIBUTE_ARRAY, ias.radius_attribute_array, nps.IAS_radius_attribute_array"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_ATTRIBUTE_ARRAY
product: Windows
targetos: Windows
req.typenames: RADIUS_ATTRIBUTE_ARRAY, *PRADIUS_ATTRIBUTE_ARRAY
req.redist: 
---

# _RADIUS_ATTRIBUTE_ARRAY structure


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS. Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</div><div> </div>The 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure represents an array of attributes.


## -struct-fields




### -field cbSize

Specifies the size of the structure.


### -field Add

Pointer to the <a href="https://msdn.microsoft.com/5ee5b673-6cb5-4a3e-9e3d-2b0010466fda">Add</a> function provided by NPS. NPS sets the value of the member.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes to which to append the specified attribute.

The 
<a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a> and 
<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### pAttr

Pointer to a 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> structure for the attribute to append to the array.


### -field AttributeAt

Pointer to the <a href="https://msdn.microsoft.com/73766632-bd70-4b0c-ac4c-b3e7901588cd">AttributeAt</a> function provided by NPS. NPS sets the value of the member.
   

The 
<a href="https://msdn.microsoft.com/73766632-bd70-4b0c-ac4c-b3e7901588cd">AttributeAt</a> function returns a const pointer to the specified attribute within the array.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes from which to retrieve the specified attribute.

The 
<a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a> and 
<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### dwIndex

Specifies the index of the attribute to retrieve. The function returns <b>NULL</b> if this index is out of range.

Use the 
<a href="https://msdn.microsoft.com/467909be-1184-419a-8cd9-a0ad008c94ef">GetSize</a> function to determine the size of the array. The largest index is one less than the size of the array.


### -field GetSize

Pointer to the <a href="https://msdn.microsoft.com/467909be-1184-419a-8cd9-a0ad008c94ef">GetSize</a> function provided by NPS. NPS sets the value of the member.

The 
<a href="https://msdn.microsoft.com/467909be-1184-419a-8cd9-a0ad008c94ef">GetSize</a> function returns the size of the attribute array.

The 
<a href="https://msdn.microsoft.com/467909be-1184-419a-8cd9-a0ad008c94ef">GetSize</a> function returns the size of the attribute array, not the largest index. Because attribute arrays use zero-based indexes, the size of the array is one greater than the largest index.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes for which to retrieve the size.

The 
<a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a> and 
<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.


### -field InsertAt

Pointer to the <a href="https://msdn.microsoft.com/d6591abd-e203-40ae-9790-06157ed8c20a">InsertAt</a> function provided by NPS. NPS sets the value of the member.

The 
<a href="https://msdn.microsoft.com/d6591abd-e203-40ae-9790-06157ed8c20a">InsertAt</a> function inserts the specified attribute at the specified index in the array.

When the 
<a href="https://msdn.microsoft.com/d6591abd-e203-40ae-9790-06157ed8c20a">InsertAt</a> function inserts a new attribute into the array, it increments the index of the pre-existing attribute at this index. Similarly, it increments the index of any pre-existing attributes at higher indexes.

To append an attribute to the end of the attribute array, use the 
<a href="https://msdn.microsoft.com/5ee5b673-6cb5-4a3e-9e3d-2b0010466fda">Add</a> function.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes in which to insert the specified attribute.

The 
<a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a> and 
<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### dwIndex

Specifies the index at which to insert the specified attribute.

Use the 
<a href="https://msdn.microsoft.com/467909be-1184-419a-8cd9-a0ad008c94ef">GetSize</a> function to determine the size of the array. The largest index is one less than the size of the array.



#### pAttr

Pointer to a 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> structure for the attribute to insert into the array.


### -field RemoveAt

Pointer to the <a href="https://msdn.microsoft.com/9302e224-d8b2-40fe-ba84-ddd0b108c021">RemoveAt</a> function provided by NPS. NPS sets the value of the member.

The 
<a href="https://msdn.microsoft.com/9302e224-d8b2-40fe-ba84-ddd0b108c021">RemoveAt</a> function removes the attribute at the specified index in the array.

When the <a href="https://msdn.microsoft.com/9302e224-d8b2-40fe-ba84-ddd0b108c021">RemoveAt</a> function removes an attribute from the array, it decrements the index of any pre-existing attributes at higher indexes.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes from which to remove the specified attribute.

The 
<a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a> and 
<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### dwIndex

Specifies the index of the attribute to remove.

Use the 
<a href="https://msdn.microsoft.com/467909be-1184-419a-8cd9-a0ad008c94ef">GetSize</a> function to determine the size of the array. The largest index is one less than the size of the array.


### -field SetAt

Pointer to the <a href="https://msdn.microsoft.com/7962de64-7140-4920-86ac-d2137df8c5a1">SetAt</a> function provided by NPS. NPS sets the value of the member.

The 
<a href="https://msdn.microsoft.com/7962de64-7140-4920-86ac-d2137df8c5a1">SetAt</a> function replaces the attribute at the specified index with the specified attribute.



#### This

Pointer to the 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structure that represents the array of attributes that contains the attribute to replace.

The 
<a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a> and 
<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a> functions return pointers to 
<b>RADIUS_ATTRIBUTE_ARRAY</b> structures.



#### dwIndex

Specifies the index of the attribute to replace.

Use the 
<a href="https://msdn.microsoft.com/467909be-1184-419a-8cd9-a0ad008c94ef">GetSize</a> function to determine the size of the array. The largest index is one less than the size of the array.



#### pAttr

Pointer to a 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> structure. The attribute represented by this structure replaces the attribute at the specified index.


## -remarks



The Extension DLL must not modify this structure. Changes to the array of attributes should be made by calling the functions provided as members of this structure.

This structure is used by Extension DLLs that export 
<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a>. The functions that add attributes to the array:

<a href="https://msdn.microsoft.com/5ee5b673-6cb5-4a3e-9e3d-2b0010466fda">Add</a>
<a href="https://msdn.microsoft.com/d6591abd-e203-40ae-9790-06157ed8c20a">InsertAt</a>
copy the contents of the caller-supplied 
<a href="https://msdn.microsoft.com/7c6e1a41-9736-4bd3-b709-779d871ead57">RADIUS_ATTRIBUTE</a> structure. Therefore, Extension DLLs that export 
<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a> need not export 
<a href="https://msdn.microsoft.com/2b76c648-a8d6-440c-b0b8-7c17f91ad961">RadiusExtensionFreeAttributes</a>.

This structure is returned by the functions 
<a href="https://msdn.microsoft.com/e8df573c-567e-476d-bff8-63e57b719f8a">GetRequest</a> and 
<a href="https://msdn.microsoft.com/c82797fb-7ff9-496e-9744-28825529156a">GetResponse</a>.




## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>



<a href="https://msdn.microsoft.com/8b13a21c-edbe-4982-8718-a34d62ecc38d">NPS Extensions Structures</a>



<a href="https://msdn.microsoft.com/13ff0645-d3f8-4220-a5bc-11bb515bca95">RADIUS_EXTENSION_CONTROL_BLOCK</a>



<a href="https://msdn.microsoft.com/993b1ded-9fa9-4834-a37d-4da9e8ed9640">RadiusExtensionProcess2</a>
 

 

