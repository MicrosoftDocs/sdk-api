---
UID: NE:d2d1_1.D2D1_PROPERTY_TYPE
title: D2D1_PROPERTY_TYPE
author: windows-sdk-content
description: Specifies the types of properties supported by the Direct2D property interface.
old-location: direct2d\__d2d1_property_type.htm
tech.root: direct2d
ms.assetid: 6535d71a-c76c-462c-9972-4db7e4ef383d
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: D2D1_PROPERTY_TYPE, D2D1_PROPERTY_TYPE enumeration [Direct2D], D2D1_PROPERTY_TYPE_ARRAY, D2D1_PROPERTY_TYPE_BLOB, D2D1_PROPERTY_TYPE_BOOL, D2D1_PROPERTY_TYPE_CLSID, D2D1_PROPERTY_TYPE_COLOR_CONTEXT, D2D1_PROPERTY_TYPE_ENUM, D2D1_PROPERTY_TYPE_FLOAT, D2D1_PROPERTY_TYPE_INT32, D2D1_PROPERTY_TYPE_IUNKNOWN, D2D1_PROPERTY_TYPE_MATRIX_3X2, D2D1_PROPERTY_TYPE_MATRIX_4X3, D2D1_PROPERTY_TYPE_MATRIX_4X4, D2D1_PROPERTY_TYPE_MATRIX_5X4, D2D1_PROPERTY_TYPE_STRING, D2D1_PROPERTY_TYPE_UINT32, D2D1_PROPERTY_TYPE_UNKNOWN, D2D1_PROPERTY_TYPE_VECTOR2, D2D1_PROPERTY_TYPE_VECTOR3, D2D1_PROPERTY_TYPE_VECTOR4, d2d1_1/D2D1_PROPERTY_TYPE, d2d1_1/D2D1_PROPERTY_TYPE_ARRAY, d2d1_1/D2D1_PROPERTY_TYPE_BLOB, d2d1_1/D2D1_PROPERTY_TYPE_BOOL, d2d1_1/D2D1_PROPERTY_TYPE_CLSID, d2d1_1/D2D1_PROPERTY_TYPE_COLOR_CONTEXT, d2d1_1/D2D1_PROPERTY_TYPE_ENUM, d2d1_1/D2D1_PROPERTY_TYPE_FLOAT, d2d1_1/D2D1_PROPERTY_TYPE_INT32, d2d1_1/D2D1_PROPERTY_TYPE_IUNKNOWN, d2d1_1/D2D1_PROPERTY_TYPE_MATRIX_3X2, d2d1_1/D2D1_PROPERTY_TYPE_MATRIX_4X3, d2d1_1/D2D1_PROPERTY_TYPE_MATRIX_4X4, d2d1_1/D2D1_PROPERTY_TYPE_MATRIX_5X4, d2d1_1/D2D1_PROPERTY_TYPE_STRING, d2d1_1/D2D1_PROPERTY_TYPE_UINT32, d2d1_1/D2D1_PROPERTY_TYPE_UNKNOWN, d2d1_1/D2D1_PROPERTY_TYPE_VECTOR2, d2d1_1/D2D1_PROPERTY_TYPE_VECTOR3, d2d1_1/D2D1_PROPERTY_TYPE_VECTOR4, direct2d.__d2d1_property_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D2d1_1.h
api_name:
 - D2D1_PROPERTY_TYPE
product: Windows
targetos: Windows
req.typenames: D2D1_PROPERTY_TYPE
req.redist: 
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
 

 

