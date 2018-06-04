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

# _PROVIDER_FILTER_INFO structure


## -description


Defines a filter and its data.


## -struct-fields




### -field Id

The filter identifier that identifies the filter in the manifest. This is the same value as the <b>value</b> attribute of the <a href="https://msdn.microsoft.com/f2874b3f-cf3a-4dd9-b914-6adaac33cf7b">FilterType</a> complex type.


### -field Version

The version number that identifies the version of the filter definition in the manifest. This is the same value as the <b>version</b> attribute of the <a href="https://msdn.microsoft.com/f2874b3f-cf3a-4dd9-b914-6adaac33cf7b">FilterType</a> complex type.


### -field MessageOffset

Offset from the beginning of this structure to the message string that describes the filter. This is the same value as the <b>message</b> attribute of the <a href="https://msdn.microsoft.com/f2874b3f-cf3a-4dd9-b914-6adaac33cf7b">FilterType</a> complex type.


### -field Reserved

Reserved.


### -field PropertyCount

The number of elements in the <i>EventPropertyInfoArray</i> array.


### -field EventPropertyInfoArray

An array of <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structures that define the filter data.


## -see-also




<a href="https://msdn.microsoft.com/bc0f4286-1f6e-4d99-ad84-af8ab5dbba2b">TdhEnumerateProviderFilters</a>
 

 

