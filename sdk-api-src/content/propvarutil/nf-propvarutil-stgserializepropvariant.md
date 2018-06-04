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

# StgSerializePropVariant function


## -description


The <b>StgSerializePropVariant</b> function converts a <b>PROPVARIANT</b> data type to a <b>SERIALIZEDPROPERTYVALUE</b> data type.


## -parameters




### -param ppropvar

TBD


### -param ppProp [out]

A pointer to the newly allocated  <b>SERIALIZEDPROPERTYVALUE</b>.


### -param pcb [out]

A pointer to the size of the newly allocated  <b>SERIALIZEDPROPERTYVALUE</b>.


#### - pVar [in]

A pointer to <b>PROPVARIANT</b>.


## -returns



This function can return one of these values.




## -remarks



The 
 <b>StgSerializePropVariant</b> function serializes a <b>PROPVARIANT</b>.  The function is similar to the <a href="https://msdn.microsoft.com/3d35b808-4fa6-44ec-9c46-96ceee1dafd0">StgConvertVariantToProperty</a> function, but   the <b>StgSerializePropVariant</b> function automatically handles memory allocation for the new <b>SERIALIZEDPROPERTYVALUE</b>.  In addition, <b>StgSerializePropVariant</b> uses the default values <b>CP_WINUNICODE</b> and PID_ILLEGAL for code page and property ID respectively.  Use <b>StgSerializePropVariant</b> unless control over these arguments is specifically needed.




## -see-also




<a href="https://msdn.microsoft.com/3d35b808-4fa6-44ec-9c46-96ceee1dafd0">StgConvertVariantToProperty</a>



<a href="https://msdn.microsoft.com/55b4de40-d81d-4989-8f57-a286815fa495">StgDeserializePropVariant</a>
 

 

