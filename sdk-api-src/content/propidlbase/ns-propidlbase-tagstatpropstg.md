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

# tagSTATPROPSTG structure


## -description



			The 
<b>STATPROPSTG</b> structure contains data about a single property in a property set. This data is the property ID and type tag, and the optional string name that may be associated with the property.


<a href="https://msdn.microsoft.com/73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf">IPropertyStorage::Enum</a> supplies a pointer to the 
<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a> interface on an enumerator object that can be used to enumerate the 
<b>STATPROPSTG</b> structures for the properties in the current property set. 
<b>STATPROPSTG</b> is defined as:


## -struct-fields




### -field lpwstrName

A wide-character null-terminated Unicode string that contains the optional string name associated with the property. May be <b>NULL</b>. This member must be freed using 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>.


### -field propid

A 32-bit identifier that uniquely identifies the property within the property set. All properties within property sets must have unique property identifiers.


### -field vt

The property type.


## -see-also




<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a>



<a href="https://msdn.microsoft.com/73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf">IPropertyStorage::Enum</a>
 

 

