---
UID: NF:d3d12.ID3D12Device2.CreatePipelineState
title: ID3D12Device2::CreatePipelineState (d3d12.h)
description: Creates a pipeline state object from a pipeline state stream description.
helpviewer_keywords: ["CreatePipelineState","CreatePipelineState method","CreatePipelineState method","ID3D12Device2 interface","ID3D12Device2 interface","CreatePipelineState method","ID3D12Device2.CreatePipelineState","ID3D12Device2::CreatePipelineState","d3d12/ID3D12Device2::CreatePipelineState","direct3d12.id3d12device2_createpipelinestate"]
old-location: direct3d12\id3d12device2_createpipelinestate.htm
tech.root: direct3d12
ms.assetid: 90557451-CB7A-4F05-8BDB-B611FE034CBB
ms.date: 12/05/2018
ms.keywords: CreatePipelineState, CreatePipelineState method, CreatePipelineState method,ID3D12Device2 interface, ID3D12Device2 interface,CreatePipelineState method, ID3D12Device2.CreatePipelineState, ID3D12Device2::CreatePipelineState, d3d12/ID3D12Device2::CreatePipelineState, direct3d12.id3d12device2_createpipelinestate
f1_keywords:
- d3d12/ID3D12Device2.CreatePipelineState
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d12.dll
api_name:
- ID3D12Device2.CreatePipelineState
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Device2::CreatePipelineState


## -description


Creates a pipeline state object from a pipeline state stream description.


## -parameters




### -param pDesc

Type: <b>const <a href="../d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc.md">D3D12_PIPELINE_STATE_STREAM_DESC</a>*</b>

The address of a <a href="../d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc.md">D3D12_PIPELINE_STATE_STREAM_DESC</a> structure that describes the pipeline state.


### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the pipeline state interface (<a href="../d3d12/nn-d3d12-id3d12pipelinestate.md">ID3D12PipelineState</a>).

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the pipeline state can be obtained by using the __uuidof() macro. For example, __uuidof(ID3D12PipelineState) will get the <b>GUID</b> of the interface to a pipeline state.


### -param ppPipelineState [out]

Type: <b>void**</b>

<a href="/cpp/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_COM_Outptr_</code>

A pointer to a memory block that receives a pointer to the <a href="../d3d12/nn-d3d12-id3d12pipelinestate.md">ID3D12PipelineState</a> interface for the pipeline state object.

The pipeline state object is an immutable state object. It contains no methods.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns <b>E_OUTOFMEMORY</b> if there is insufficient memory to create the pipeline state object. See <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> for other possible return values.




## -remarks



This function takes the pipeline description as a <a href="../d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc.md">D3D12_PIPELINE_STATE_STREAM_DESC</a> and combines the functionality of the <a href="../d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate.md">ID3D12Device::CreateGraphicsPipelineState</a> and <a href="../d3d12/nf-d3d12-id3d12device-createcomputepipelinestate.md">ID3D12Device::CreateComputePipelineState</a> functions, which take their pipeline description as the less-flexible <a href="../d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc.md">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> and <a href="../d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc.md">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structs, respectively.




## -see-also


See <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc"><b>D3D12_PIPELINE_STATE_STREAM_DESC</b></a> for a description of the layout and behavior of a streaming pipeline desc.


<a href="../d3d12/nn-d3d12-id3d12device2.md">ID3D12Device2</a>
 

 
