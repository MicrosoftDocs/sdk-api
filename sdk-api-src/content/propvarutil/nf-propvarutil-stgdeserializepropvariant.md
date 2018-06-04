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

# StgDeserializePropVariant function


## -description


The <b>StgDeserializePropVariant</b> function converts a SERIALIZEDPROPERTYVALUE data type to a PROPVARIANT data type.


## -parameters




### -param pprop [in]

A pointer to the  <b>SERIALIZEDPROPERTYVALUE</b> buffer.


### -param cbMax [in]

The size of the <i>pprop</i> buffer in bytes.


### -param ppropvar

TBD




#### - pvar [out]

A pointer to a <b>PROPVARIANT</b>.


## -returns



This function can return one of these values.




## -remarks



This function deserializes a <b>PROPVARIANT</b> data type. This function is similar to the <a href="https://msdn.microsoft.com/ea4196e6-fc99-4288-942a-e5283f2e5544">StgConvertPropertyToVariant</a> function. The <b>StgDeserializePropVariant</b> function uses the default value of <b>CP_WINUNICODE</b> for the code page and a system provided allocator that uses task memory.  Use <b>StgDeserializePropVariant</b> unless you want to specify which code page and memory allocator to use.




## -see-also




<a href="https://msdn.microsoft.com/ea4196e6-fc99-4288-942a-e5283f2e5544">StgConvertPropertyToVariant</a>



<a href="https://msdn.microsoft.com/e1382c1e-3f9e-41a2-8e95-fc3702e516d3">StgSerializePropVariant</a>
 

 

