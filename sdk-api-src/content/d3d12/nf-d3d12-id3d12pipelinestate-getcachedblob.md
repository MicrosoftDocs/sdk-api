---
UID: NF:d3d12.ID3D12PipelineState.GetCachedBlob
title: ID3D12PipelineState::GetCachedBlob (d3d12.h)
description: Gets the cached blob representing the pipeline state.
helpviewer_keywords: ["GetCachedBlob","GetCachedBlob method","GetCachedBlob method","ID3D12PipelineState interface","ID3D12PipelineState interface","GetCachedBlob method","ID3D12PipelineState.GetCachedBlob","ID3D12PipelineState::GetCachedBlob","d3d12/ID3D12PipelineState::GetCachedBlob","direct3d12.id3d12pipelinestate_getcachedblob"]
old-location: direct3d12\id3d12pipelinestate_getcachedblob.htm
tech.root: direct3d12
ms.assetid: 318FCFEE-74A7-4546-989E-9AF674D2B853
ms.date: 12/05/2018
ms.keywords: GetCachedBlob, GetCachedBlob method, GetCachedBlob method,ID3D12PipelineState interface, ID3D12PipelineState interface,GetCachedBlob method, ID3D12PipelineState.GetCachedBlob, ID3D12PipelineState::GetCachedBlob, d3d12/ID3D12PipelineState::GetCachedBlob, direct3d12.id3d12pipelinestate_getcachedblob
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
 - ID3D12PipelineState::GetCachedBlob
 - d3d12/ID3D12PipelineState::GetCachedBlob
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
 - ID3D12PipelineState.GetCachedBlob
---

# ID3D12PipelineState::GetCachedBlob


## -description

Gets the cached blob representing the pipeline state.

## -parameters

### -param ppBlob [out]

Type: <b>ID3DBlob**</b>

After this method returns, points to the cached blob representing the pipeline state.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

Refer to the remarks for <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cached_pipeline_state">D3D12_CACHED_PIPELINE_STATE</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pipelinestate">ID3D12PipelineState</a>