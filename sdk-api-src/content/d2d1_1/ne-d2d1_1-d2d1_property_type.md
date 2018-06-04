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

# D2D1_PROPERTY_TYPE enumeration


## -description


Specifies the types of properties supported by the Direct2D property interface. 


## -enum-fields




### -field D2D1_PROPERTY_TYPE_UNKNOWN

An unknown property.


### -field D2D1_PROPERTY_TYPE_STRING

An arbitrary-length string.


### -field D2D1_PROPERTY_TYPE_BOOL

A 32-bit integer value constrained to be either 0 or 1.


### -field D2D1_PROPERTY_TYPE_UINT32

An unsigned 32-bit integer.


### -field D2D1_PROPERTY_TYPE_INT32

A signed 32-bit integer.


### -field D2D1_PROPERTY_TYPE_FLOAT

A 32-bit float.


### -field D2D1_PROPERTY_TYPE_VECTOR2

Two 32-bit float values.


### -field D2D1_PROPERTY_TYPE_VECTOR3

 Three 32-bit float values.


### -field D2D1_PROPERTY_TYPE_VECTOR4

Four 32-bit float values.


### -field D2D1_PROPERTY_TYPE_BLOB

An arbitrary number of bytes.


### -field D2D1_PROPERTY_TYPE_IUNKNOWN

A returned COM or nano-COM interface. 


### -field D2D1_PROPERTY_TYPE_ENUM

An enumeration. The value should be treated as a <b>UINT32</b> with a defined array of fields to specify the bindings to human-readable strings.


### -field D2D1_PROPERTY_TYPE_ARRAY

An enumeration. The value is the count of sub-properties in the array. The set of array elements will be contained in the sub-property.


### -field D2D1_PROPERTY_TYPE_CLSID

A CLSID.


### -field D2D1_PROPERTY_TYPE_MATRIX_3X2

A 3x2 matrix of  float values.


### -field D2D1_PROPERTY_TYPE_MATRIX_4X3

A 4x2 matrix of  float values.


### -field D2D1_PROPERTY_TYPE_MATRIX_4X4

A 4x4 matrix of  float values.


### -field D2D1_PROPERTY_TYPE_MATRIX_5X4

A 5x4 matrix of  float values.


### -field D2D1_PROPERTY_TYPE_COLOR_CONTEXT

A nano-COM color context interface pointer.


### -field D2D1_PROPERTY_TYPE_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/c38bfcc0-c696-41cc-9531-7c8f15c0b512">ID2D1Properties</a>



<a href="https://msdn.microsoft.com/42e80588-9e80-4f30-9a3c-77b64f88ff7a">ID2D1Properties::GetType</a>
 

 

