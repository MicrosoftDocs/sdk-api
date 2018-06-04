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

# IValueMap::get_Value


## -description


Retrieves or sets the value of the collection.

This property is read/write.


## -parameters


## -remarks



Depending on the value of the <a href="https://msdn.microsoft.com/42cea1e6-c945-4bae-ac65-a052b4069e5f">IValueMap::ValueMapType</a> property, this value is either one of the values in the collection or the value derived by combining all the item values in the collection with the <b>OR</b> operator.

The variant type is VT_UI8 if the <a href="https://msdn.microsoft.com/cc217b3b-389a-4d15-b47d-456778f3eaec">ValueMapType</a> enumeration is <b>plaIndex</b>, <b>plaFlag</b> or <b>plaFlagArray</b>.

The variant type is VT_UI4 if the <a href="https://msdn.microsoft.com/cc217b3b-389a-4d15-b47d-456778f3eaec">ValueMapType</a> enumeration is <b>plaValidation</b>.




## -see-also




<a href="https://msdn.microsoft.com/a7134395-91c6-4ea1-8b76-63830048289f">IValueMap</a>



<a href="https://msdn.microsoft.com/42cea1e6-c945-4bae-ac65-a052b4069e5f">IValueMap::ValueMapType</a>
 

 

