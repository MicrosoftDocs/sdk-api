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

# _D3D_SHADER_VARIABLE_CLASS enumeration


## -description


Values that identify the class of a shader variable.


## -enum-fields




### -field D3D_SVC_SCALAR

The shader variable is a scalar.


### -field D3D_SVC_VECTOR

The shader variable is a vector.


### -field D3D_SVC_MATRIX_ROWS

The shader variable is a row-major matrix.


### -field D3D_SVC_MATRIX_COLUMNS

The shader variable is a column-major matrix.


### -field D3D_SVC_OBJECT

The shader variable is an object.


### -field D3D_SVC_STRUCT

The shader variable is a structure.


### -field D3D_SVC_INTERFACE_CLASS

The shader variable is a class.


### -field D3D_SVC_INTERFACE_POINTER

The shader variable is an interface.


### -field D3D10_SVC_SCALAR

The shader variable is a scalar.


### -field D3D10_SVC_VECTOR

The shader variable is a vector.


### -field D3D10_SVC_MATRIX_ROWS

The shader variable is a row-major matrix.


### -field D3D10_SVC_MATRIX_COLUMNS

The shader variable is a column-major matrix.


### -field D3D10_SVC_OBJECT

The shader variable is an object.


### -field D3D10_SVC_STRUCT

The shader variable is a structure.


### -field D3D11_SVC_INTERFACE_CLASS

The shader variable is a class.


### -field D3D11_SVC_INTERFACE_POINTER

The shader variable is an interface.


### -field D3D_SVC_FORCE_DWORD

This value is not used by a programmer; it exists to force the enumeration to compile to 32 bits.


## -remarks



The class of a shader variable is not a programming class; the class identifies the variable class such as scalar, vector, object, and so on. <b>D3D_SHADER_VARIABLE_CLASS</b>-typed values are specified in the <b>Class</b> member of the <a href="https://msdn.microsoft.com/8d2067a3-17f8-4496-a613-581f5e35fe93">D3D11_SHADER_TYPE_DESC</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/002154d5-74a6-48fb-b55f-8687e4505fc7">Common Version Enumerations</a>
 

 

