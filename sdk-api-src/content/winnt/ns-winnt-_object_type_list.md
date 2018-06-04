---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _OBJECT_TYPE_LIST structure


## -description


The <b>OBJECT_TYPE_LIST</b> structure identifies an object type element in a hierarchy of object types. The 
<a href="https://msdn.microsoft.com/50acfc17-459d-464c-9927-88b32dd424c7">AccessCheckByType</a> functions use an array of <b>OBJECT_TYPE_LIST</b> structures to define a hierarchy of an object and its subobjects, such as property sets and properties.


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




<a href="https://msdn.microsoft.com/50acfc17-459d-464c-9927-88b32dd424c7">AccessCheckByType</a>



<a href="https://msdn.microsoft.com/ea14fd55-e0e4-4bf2-b20e-5874783c16c3">AccessCheckByTypeAndAuditAlarm</a>



<a href="https://msdn.microsoft.com/ce713421-d4ff-48ed-b751-5e5c5397d820">AccessCheckByTypeResultList</a>



<a href="https://msdn.microsoft.com/4b53a15a-5a6b-40c7-acf8-26b1f4bca4ae">AccessCheckByTypeResultListAndAuditAlarm</a>
 

 

