---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetPipelineState
title: ID3D12GraphicsCommandList::SetPipelineState (d3d12.h)
description: Sets all shaders and programs most of the fixed-function state of the graphics processing unit (GPU) pipeline.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetPipelineState method","ID3D12GraphicsCommandList.SetPipelineState","ID3D12GraphicsCommandList::SetPipelineState","SetPipelineState","SetPipelineState method","SetPipelineState method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetPipelineState","direct3d12.id3d12graphicscommandlist_setpipelinestate"]
old-location: direct3d12\id3d12graphicscommandlist_setpipelinestate.htm
tech.root: direct3d12
ms.assetid: 751E09A4-D8FE-4DEA-86D9-1C84265F2F21
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetPipelineState method, ID3D12GraphicsCommandList.SetPipelineState, ID3D12GraphicsCommandList::SetPipelineState, SetPipelineState, SetPipelineState method, SetPipelineState method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetPipelineState, direct3d12.id3d12graphicscommandlist_setpipelinestate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12GraphicsCommandList::SetPipelineState
 - d3d12/ID3D12GraphicsCommandList::SetPipelineState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.SetPipelineState
---

# ID3D12GraphicsCommandList::SetPipelineState


## -description

Sets all shaders and programs most of the fixed-function state of the graphics processing unit (GPU) pipeline.

## -parameters

### -param pPipelineState [in]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a>*</b>

Pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a> containing the pipeline state data.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>