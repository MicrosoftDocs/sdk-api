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

# IValueMapItem::get_Value


## -description


Retrieves or sets the value of the item.

This property is read/write.


## -parameters


## -remarks



The variant type is VT_UI8 if the <a href="https://msdn.microsoft.com/cc217b3b-389a-4d15-b47d-456778f3eaec">ValueMapType</a> enumeration is plaIndex, plaFlag or plaFlagArray.

The variant type is VT_UI4 if <a href="https://msdn.microsoft.com/cc217b3b-389a-4d15-b47d-456778f3eaec">ValueMapType</a> is plaValidation.




## -see-also




<a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">IValueMap::Value</a>



<a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a>



<a href="https://msdn.microsoft.com/006d134d-d14b-4964-b46c-7dd2353d2493">IValueMapItem::ValueMapType</a>
 

 

