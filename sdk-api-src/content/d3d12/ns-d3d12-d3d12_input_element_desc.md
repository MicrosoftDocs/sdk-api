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

# D3D12_INPUT_ELEMENT_DESC structure


## -description


Describes a single element for the input-assembler stage of the graphics pipeline.


## -struct-fields




### -field SemanticName

The HLSL semantic associated with this element in a shader input-signature.


### -field SemanticIndex

The semantic index for the element. A semantic index modifies a semantic, with an integer index number. A semantic index is only needed in a 
        case where there is more than one element with the same semantic. For example, a 4x4 matrix would have four components each with the semantic 
        name <b>matrix</b>, however each of the four component would have different semantic indices (0, 1, 2, and 3).


### -field Format

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value that specifies the format of the element data.


### -field InputSlot

An integer value that identifies the input-assembler. For more info, see <a href="https://msdn.microsoft.com/84c0ca29-2356-4b7f-98ee-ff1758edc540">Input Slots</a>. Valid values are between 0 and 15. 


### -field AlignedByteOffset

Optional. Offset, in bytes, between each element. Use D3D12_APPEND_ALIGNED_ELEMENT (0xffffffff) for convenience to define the current element directly 
        after the previous one, including any packing if necessary.


### -field InputSlotClass

A value that identifies the input data class for a single input slot.


### -field InstanceDataStepRate

The number of instances to draw using the same per-instance data before advancing in the buffer by one element. This value must be 0 for an 
        element that contains per-vertex data (the slot class is set to the D3D12_INPUT_PER_VERTEX_DATA member of <a href="https://msdn.microsoft.com/09A14704-2E0B-4994-BED4-94F933A47317">D3D12_INPUT_CLASSIFICATION</a>).


## -remarks



This structure is a member of the <a href="https://msdn.microsoft.com/44C53830-AE80-402A-808C-2063011711A2">D3D12_INPUT_LAYOUT_DESC</a> structure. A pipeline state object contains a input-layout structure that defines one element being read from an input slot.




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

