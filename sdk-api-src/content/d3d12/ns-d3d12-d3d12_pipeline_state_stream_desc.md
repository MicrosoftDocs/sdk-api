---
UID: NS:d3d12.D3D12_PIPELINE_STATE_STREAM_DESC
title: D3D12_PIPELINE_STATE_STREAM_DESC (d3d12.h)
description: Describes a pipeline state stream.
helpviewer_keywords: ["D3D12_PIPELINE_STATE_STREAM_DESC","D3D12_PIPELINE_STATE_STREAM_DESC structure","d3d12/D3D12_PIPELINE_STATE_STREAM_DESC","direct3d12.d3d12_pipeline_state_stream_desc"]
old-location: direct3d12\d3d12_pipeline_state_stream_desc.htm
tech.root: direct3d12
ms.assetid: 2CC9051B-09B1-49F5-9392-3E0AE3AB1277
ms.date: 12/05/2018
ms.keywords: D3D12_PIPELINE_STATE_STREAM_DESC, D3D12_PIPELINE_STATE_STREAM_DESC structure, d3d12/D3D12_PIPELINE_STATE_STREAM_DESC, direct3d12.d3d12_pipeline_state_stream_desc
f1_keywords:
- d3d12/D3D12_PIPELINE_STATE_STREAM_DESC
dev_langs:
- c++
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- d3d12.h
api_name:
- D3D12_PIPELINE_STATE_STREAM_DESC
targetos: Windows
req.typenames: D3D12_PIPELINE_STATE_STREAM_DESC
req.redist: 
ms.custom: 19H1
---

# D3D12_PIPELINE_STATE_STREAM_DESC structure


## -description


Describes a pipeline state stream.


## -struct-fields




### -field SizeInBytes

<a href="/cpp/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

Specifies the size of the opaque data structure pointed to by the pPipelineStateSubobjectStream member, in bytes.


### -field pPipelineStateSubobjectStream

<a href="/cpp/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_reads_(_Inexpressible_("Dependentonsizeofsubobjects"))</code>

Specifies the address of a data structure that describes as a bytestream an arbitrary pipeline state subobject.


## -remarks



Use this structure with the **[ID3D12Device2::CreatePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)** method to create pipeline state objects. 

The format of the provided stream should consist of an alternating set of **[D3D12_PIPELINE_STATE_SUBOBJECT_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)**, and the corresponding subobject types for them (for example, **D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER** pairs with **[D3D12_RASTERIZER_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)**. In terms of alignment, the D3D12 runtime expects subobjects to be individual struct pairs of enum-struct, rather than a continuous set of fields. It also expects them to be aligned to the natural word alignment of the system. This can be achieved either using `alignas(void*)`, or making a `union` of the enum + subobject and a `void*`. 

> [!IMPORTANT]
> It isn't sufficient to simply union the **D3D12_PIPELINE_STATE_SUBOBJECT_TYPE** with a **void\***, because this will result in certain subobjects being misaligned.
> For example, **D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_PRIMITIVE_TOPOLOGY** is followed by a **[D3D12_PRIMITIVE_TOPOLOGY_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type)** enum. If the subobject type is unioned with a **void\***, then there will be additional padding between these 2 members, resulting in corruption of the stream.
> Because of this, you should union the entire subobject struct with a **void\***, when `alignas` is not available

An example of a suitable subobject for use with **[D3D12_RASTERIZER_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)** is shown here:

```cpp
struct alignas(void*) StreamingRasterizerDesc
{
private:
  D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type = D3D12_PIPELINE_STATE_SUBOBJECT_TYPE_RASTERIZER;
public:
  D3D12_RASTERIZER_DESC Desc;
}
```

The runtime will determine the type of a pipeline stream (valid types being **COMPUTE**, **GRAPHICS**, and **MESH**), by which subobject type, out of **VS** (vertex shader), **CS** (compute shader), and **MS** (mesh shader), is found. If the runtime finds none of these shaders, it will fail pipeline creation. If it finds multiple of these shaders which are not null, it will also fail. This means it is legal to have both, for example, a **CS** and **VS** in your stream object, provided only one has a non-null pointer for the shader bytecode for any given call to **[ID3D12Device2::CreatePipelineState](/windows/win32/api/d3d12/nf-d3d12-id3d12device2-createpipelinestate)**.
Subobject types irrelevant to the pipeline (e.g a compute shader subobject in a graphics stream) will be ignored.
If a subobject is not provided (excluding the above required subobjects), the runtime will provide a default value for it.

Consider using the `d3dx12.h` extensions for C++, which provide a set of helper structs for all pipeline subobjects (for example, the above struct is very similar to `CD3DX12_PIPELINE_STATE_STREAM_RASTERIZER`). This header can be found under the **[DirectX-Headers](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h)** repo on github.

### -runtime-validation

The runtime will validate the PSO desc is either a compute, mesh, or graphics pipeline, that all subobjects are recognised types, and that there are not duplicate subobjects.

> [!NOTE]
> Some subobjects are considered to be a "derived" version of others for the purposes of recognising duplicated subobjects. For example, if the runtime discovers a **[D3D12_DEPTH_STENCIL_DESC](windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)** subobject, and then later a **[D3D12_DEPTH_STENCIL_DESC1](windows/win32/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)**, it will consider these duplicate subobjects and fail. 


## -see-also




<a href="/windows/win32/direct3d12/direct3d-12-structures">Core Structures</a>
 

 
