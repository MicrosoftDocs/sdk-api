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

# _D3D10_EFFECT_TYPE_DESC structure


## -description


Describes an effect-variable type.


## -struct-fields




### -field TypeName

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A string that contains the variable name.


### -field Class

Type: <b><a href="https://msdn.microsoft.com/e638c059-9c92-43fe-9fae-8a0cf535af8f">D3D10_SHADER_VARIABLE_CLASS</a></b>

The variable class (see <a href="https://msdn.microsoft.com/e638c059-9c92-43fe-9fae-8a0cf535af8f">D3D10_SHADER_VARIABLE_CLASS</a>).


### -field Type

Type: <b><a href="https://msdn.microsoft.com/fac84252-ec19-4fc9-9171-143b63347888">D3D10_SHADER_VARIABLE_TYPE</a></b>

The variable type (see <a href="https://msdn.microsoft.com/fac84252-ec19-4fc9-9171-143b63347888">D3D10_SHADER_VARIABLE_TYPE</a>).


### -field Elements

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of elements if the variable is an array; otherwise 0.


### -field Members

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of members if the variable is a structure; otherwise 0.


### -field Rows

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of rows if the variable is a matrix; otherwise 0.


### -field Columns

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of columns if the variable is a matrix; otherwise 0.


### -field PackedSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes that the variable consumes when it is packed tightly by the compiler.


### -field UnpackedSize

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes that the variable consumes before it is packed by the compiler.


### -field Stride

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of bytes between elements.


## -remarks



To get an effect-variable type, call <a href="https://msdn.microsoft.com/cd046d58-8c7b-47b4-a75b-374edb06b33a">ID3D10EffectType::GetDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/bbd69b4b-d2f4-471f-a607-328f5fc603b5">Effect Structures (Direct3D 10)</a>
 

 

