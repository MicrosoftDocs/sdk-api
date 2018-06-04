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

# StgConvertVariantToProperty function


## -description


The <b>StgConvertVariantToProperty</b> function converts a <b>PROPVARIANT</b> data type to a <b>SERIALIZEDPROPERTYVALUE</b> data type.


## -parameters




### -param pvar [in]

A  pointer to <b>PROPVARIANT</b>.


### -param CodePage [in]

A property set codepage.


### -param pprop [out, optional]

Optional. A pointer to <b>SERIALIZEDPROPERTYVALUE</b>.


### -param pcb [in, out]

A pointer to the remaining stream length, updated to the actual property size on return.


### -param pid [in]

The propid (used if indirect).


### -param fReserved [in]

Reserver. The value must be <b>FALSE</b>.


### -param pcIndirect [in, out, optional]

Optional. A pointer to the indirect property count.


## -returns



Returns a pointer to <b>SERIALIZEDPROPERTYVALUE</b>.




## -remarks



This function converts a <b>PROPVARIANT</b> to a property. If the function fails it throws an exception that represents <b>STATUS_INVALID_PARAMETER NT_STATUS</b>.




## -see-also




<a href="https://msdn.microsoft.com/ea4196e6-fc99-4288-942a-e5283f2e5544">StgConvertPropertyToVariant</a>



<a href="https://msdn.microsoft.com/e1382c1e-3f9e-41a2-8e95-fc3702e516d3">StgSerializePropVariant</a>
 

 

