---
UID: NF:d3d12.ID3D12PipelineLibrary1.LoadPipeline
title: ID3D12PipelineLibrary1::LoadPipeline (d3d12.h)
description: Retrieves the requested PSO from the library. The pipeline stream description is matched against the library database, and remembered in order to prevent duplication of PSO contents.
helpviewer_keywords: ["ID3D12PipelineLibrary1 interface","LoadPipeline method","ID3D12PipelineLibrary1.LoadPipeline","ID3D12PipelineLibrary1::LoadPipeline","LoadPipeline","LoadPipeline method","LoadPipeline method","ID3D12PipelineLibrary1 interface","d3d12/ID3D12PipelineLibrary1::LoadPipeline","direct3d12.id3d12pipelinelibrary1_loadpipeline"]
old-location: direct3d12\id3d12pipelinelibrary1_loadpipeline.htm
tech.root: direct3d12
ms.assetid: 842092FF-906D-4595-8C43-07F0349CA1A3
ms.date: 12/05/2018
ms.keywords: ID3D12PipelineLibrary1 interface,LoadPipeline method, ID3D12PipelineLibrary1.LoadPipeline, ID3D12PipelineLibrary1::LoadPipeline, LoadPipeline, LoadPipeline method, LoadPipeline method,ID3D12PipelineLibrary1 interface, d3d12/ID3D12PipelineLibrary1::LoadPipeline, direct3d12.id3d12pipelinelibrary1_loadpipeline
f1_keywords:
- d3d12/ID3D12PipelineLibrary1.LoadPipeline
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
- ID3D12PipelineLibrary1.LoadPipeline
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Retrieves the requested PSO from the library. The pipeline stream description is matched against the library database, and remembered in order to prevent duplication of PSO contents.

## -parameters

### -param pName [in]

Type: <b>LPCWSTR</b>

<a href="/cpp/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

The unique name of the PSO.

### -param pDesc [in]

Type: <b>const <a href="../d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc.md">D3D12_PIPELINE_STATE_STREAM_DESC</a>*</b>

<a href="/cpp/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_In_</code>

Describes the required PSO using a <a href="../d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc.md">D3D12_PIPELINE_STATE_STREAM_DESC</a> structure. This description is matched against the library database, and stored in order to prevent duplication of PSO contents.

### -param riid

Type: <b>REFIID</b>

Specifies a REFIID for the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a> object.

Your app should typically set this argument and the following argument, *ppPipelineState*, by using the macro IID_PPV_ARGS(&amp;PSO1), where PSO1 is the name of the object.

### -param ppPipelineState [out]

Type: <b>void**</b>

<a href="/cpp/code-quality/annotating-function-parameters-and-return-values">SAL</a>: <code>_COM_Outptr_</code>

Specifies the pointer that will reference the PSO after the function successfully returns.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code, which can include E_INVALIDARG if the name doesn't exist or the stream description doesn't match the data in the library, and E_OUTOFMEMORY if the function is unable to allocate the resulting PSO.

## -remarks

This function takes the pipeline description as a <a href="../d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc.md">D3D12_PIPELINE_STATE_STREAM_DESC</a> and is a replacement for the <a href="../d3d12/nf-d3d12-id3d12pipelinelibrary-loadgraphicspipeline.md">ID3D12PipelineLibrary::LoadGraphicsPipeline</a> and <a href="../d3d12/nf-d3d12-id3d12pipelinelibrary-loadcomputepipeline.md">ID3D12PipelineLibrary::LoadComputePipeline</a> functions, which take their pipeline description as the less-flexible <a href="../d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc.md">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> and <a href="../d3d12/ns-d3d12-d3d12_compute_pipeline_state_desc.md">D3D12_COMPUTE_PIPELINE_STATE_DESC</a> structs, respectively.

## -see-also

See <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_pipeline_state_stream_desc"><b>D3D12_PIPELINE_STATE_STREAM_DESC</b></a> for a description of the layout and behavior of a streaming pipeline desc.


<a href="../d3d12/nn-d3d12-id3d12pipelinelibrary1.md">ID3D12PipelineLibrary1</a>
