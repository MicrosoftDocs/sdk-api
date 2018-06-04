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

# StgPropertyLengthAsVariant function


## -description


The <b>StgPropertyLengthAsVariant</b> function examines a <b>SERIALIZEDPROPERTYVALUE</b>  and returns the amount of memory that this property would occupy as a <b>PROPVARIANT</b>.


## -parameters




### -param pProp [in]

A pointer to a <b>SERIALIZEDPROPERTYVALUE</b>.


### -param cbProp [in]

The size of the <i>pProp</i> buffer in bytes.


### -param CodePage [in]

A property set code page.


### -param bReserved [in]

Reserved. Must be 0.


## -returns



Returns the amount of memory the property would occupy as a <b>PROPVARIANT</b>.




## -remarks



Use this function to decide whether or not to deserialize a property value in a low-memory scenario.  Most applications will have no need to call this function.




## -see-also




<a href="https://msdn.microsoft.com/ea4196e6-fc99-4288-942a-e5283f2e5544">StgConvertPropertyToVariant</a>



<a href="https://msdn.microsoft.com/55b4de40-d81d-4989-8f57-a286815fa495">StgDeserializePropVariant</a>
 

 

