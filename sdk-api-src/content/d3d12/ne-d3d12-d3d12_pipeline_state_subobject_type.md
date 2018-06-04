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

# D3D12_PIPELINE_STATE_SUBOBJECT_TYPE enumeration


## -description


Specifies the type of a sub-object in a pipeline state stream description.


## -enum-fields




### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_ROOT_SIGNATURE

Indicates a root signature subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VS

Indicates a vertex shader subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PS

Indicates a pixel shader subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DS

Indicates a domain shader subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_HS

Indicates a hull shader subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_GS

Indicates a geometry shader subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CS

Indicates a compute shader subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_STREAM_OUTPUT

Indicates a stream-output subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_BLEND

Indicates a blend subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_MASK

Indicates a sample mask subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER

Indicates indicates a rasterizer subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL

Indicates a depth stencil subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_INPUT_LAYOUT

Indicates an input layout subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_IB_STRIP_CUT_VALUE

Indicates an index buffer strip cut value subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY

Indicates a primitive topology subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RENDER_TARGET_FORMATS

Indicates a render target formats subobject type. This subobject type corresponds to the D3D12_RT_FORMAT_ARRAY structure, which wraps an array of render target formats along with a count of the array elements.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL_FORMAT

Indicates a depth stencil format subobject.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_SAMPLE_DESC

Indicates a sample description subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_NODE_MASK

Indicates a node mask subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_CACHED_PSO

Indicates a cached pipeline state object subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_FLAGS

Indicates a flags subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_DEPTH_STENCIL1

Indicates an expanded depth stencil subobject type. This expansion of the depth stencil subobject supports optional depth bounds checking.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_VIEW_INSTANCING

Indicates a view instancing subobject type.


### -field D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_MAX_VALID

A sentinal value that marks the exclusive upper-bound of valid values this enumeration represents.


## -remarks



This enum is used in the creation of pipeline state objects using the ID3D12Device1::CreatePipelineState method. The CreatePipelineState method takes a D3D12_PIPELINE_STATE_STREAM_DESC as one of its parameters, this structure in turn describes a bytestream made up of alternating D3D12_PIPELINE_STATE_SUBOBJECT_TYPE enumeration values and their corresponding subobject description structs. This bytestream description can be made a concrete type by defining a structure that has the same alternating pattern of alternating D3D12_PIPELINE_STATE_SUBOBJECT_TYPE enumeration values and their corresponding subobject description structs as members.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

