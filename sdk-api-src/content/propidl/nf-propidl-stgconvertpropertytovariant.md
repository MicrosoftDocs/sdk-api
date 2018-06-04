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

# StgConvertPropertyToVariant function


## -description


The <b>StgConvertPropertyToVariant</b> function converts a <b>SERIALIZEDPROPERTYVALUE</b> data type to a <b>PROPVARIANT</b> data type.


## -parameters




### -param pprop

TBD


### -param CodePage [in]

A property set codepage.


### -param pvar [out]

A pointer to <b>PROPVARIANT</b>.


### -param pma [in]

A pointer to a class that implements the <a href="https://msdn.microsoft.com/a0735b62-5ed3-42df-a320-b58c742645a8">IMemoryAllocator</a> abstract class.


#### - prop [in]

A pointer to <b>SERIALIZEDPROPERTYVALUE</b>.


## -returns



Returns <b>TRUE</b> is the property converted was an indirect type (<b>VT_STREAM</b> or <b>VT_STREAMED_OBJECT</b>); otherwise <b>FALSE</b>.




## -remarks



This function converts a property  to a <b>PROPVARIANT</b> data type. If the function fails, it throws an exception that represents an <b>NT_STATUS</b> such as <b>STATUS_INVALID_PARAMETER</b>.




## -see-also




<a href="https://msdn.microsoft.com/3d35b808-4fa6-44ec-9c46-96ceee1dafd0">StgConvertVariantToProperty</a>



<a href="https://msdn.microsoft.com/55b4de40-d81d-4989-8f57-a286815fa495">StgDeserializePropVariant</a>
 

 

