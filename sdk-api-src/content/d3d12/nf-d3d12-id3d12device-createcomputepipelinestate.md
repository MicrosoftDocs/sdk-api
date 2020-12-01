---
UID: NF:d3d12.ID3D12Device.CreateComputePipelineState
title: ID3D12Device::CreateComputePipelineState (d3d12.h)
description: Creates a compute pipeline state object.
helpviewer_keywords: ["CreateComputePipelineState","CreateComputePipelineState method","CreateComputePipelineState method","ID3D12Device interface","ID3D12Device interface","CreateComputePipelineState method","ID3D12Device.CreateComputePipelineState","ID3D12Device::CreateComputePipelineState","d3d12/ID3D12Device::CreateComputePipelineState","direct3d12.id3d12device_createcomputepipelinestate"]
old-location: direct3d12\id3d12device_createcomputepipelinestate.htm
tech.root: direct3d12
ms.assetid: FFA361B2-D8FA-4F5A-8D0C-022C2AA76B57
ms.date: 12/05/2018
ms.keywords: CreateComputePipelineState, CreateComputePipelineState method, CreateComputePipelineState method,ID3D12Device interface, ID3D12Device interface,CreateComputePipelineState method, ID3D12Device.CreateComputePipelineState, ID3D12Device::CreateComputePipelineState, d3d12/ID3D12Device::CreateComputePipelineState, direct3d12.id3d12device_createcomputepipelinestate
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::CreateComputePipelineState
 - d3d12/ID3D12Device::CreateComputePipelineState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateComputePipelineState
---

# ID3D12Device::CreateComputePipelineState


## -description

Creates a compute pipeline state object.

## -parameters

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc">D3D12_COMPUTE_PIPELINE_STATE_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structure that describes compute pipeline state.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the pipeline state interface (<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a>).
            The <b>REFIID</b>, or <b>GUID</b>, of the interface to the pipeline state can be obtained by using the __uuidof() macro.
            For example, __uuidof(ID3D12PipelineState) will get the <b>GUID</b> of the interface to a pipeline state.

### -param ppPipelineState [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a> interface for the pipeline state object.
            The pipeline state object is an immutable state object.  It contains no methods.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the pipeline state object.
              See <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>