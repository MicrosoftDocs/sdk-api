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

# tagPROPSPEC structure


## -description



			The 
<b>PROPSPEC</b> structure is used by many of the methods of 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> to specify a property either by its property identifier (ID) or the associated string name.


## -struct-fields




### -field ulKind

Indicates the union member used. This member can be one of the following values.

<table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRSPEC_LPWSTR"></a><a id="prspec_lpwstr"></a><dl>
<dt><b>PRSPEC_LPWSTR</b></dt>
<dt>Value:  0</dt>
</dl>
</td>
<td width="60%">
The <b>lpwstr</b> member is used and set to a string name.

</td>
</tr>
<tr>
<td width="40%"><a id="PRSPEC_PROPID"></a><a id="prspec_propid"></a><dl>
<dt><b>PRSPEC_PROPID</b></dt>
<dt>Value:  1</dt>
</dl>
</td>
<td width="60%">
The <b>propid</b> member is used and set to a property ID value.

</td>
</tr>
</table>
 


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.propid

Specifies the value of the property ID. Use either this value or the following <b>lpwstr</b>, not both.


### -field DUMMYUNIONNAME.lpwstr

Specifies the string name of the property as a null-terminated Unicode string.


## -remarks



String names are optional and can be assigned to a set of properties when the property is created with a call to <a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">IPropertyStorage::WriteMultiple</a> or later with a call to <a href="https://msdn.microsoft.com/3612bf29-344a-4389-bd3b-56b9fa297362">IPropertyStorage::WritePropertyNames</a>.




## -see-also




<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>
 

 

