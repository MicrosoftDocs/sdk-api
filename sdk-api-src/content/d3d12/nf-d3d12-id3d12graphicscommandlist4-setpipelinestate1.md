---
UID: NF:d3d12.ID3D12GraphicsCommandList4.SetPipelineState1
title: ID3D12GraphicsCommandList4::SetPipelineState1 (d3d12.h)
description: Sets a state object on the command list.
helpviewer_keywords: ["ID3D12GraphicsCommandList4 interface","SetPipelineState1 method","ID3D12GraphicsCommandList4.SetPipelineState1","ID3D12GraphicsCommandList4::SetPipelineState1","SetPipelineState1","SetPipelineState1 method","SetPipelineState1 method","ID3D12GraphicsCommandList4 interface","d3d12/ID3D12GraphicsCommandList4::SetPipelineState1","direct3d12.id3d12graphicscommandlist4_setpipelinestate1"]
old-location: direct3d12\id3d12graphicscommandlist4_setpipelinestate1.htm
tech.root: direct3d12
ms.assetid: CD408074-2B2A-461C-9CA8-DC967BC61067
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList4 interface,SetPipelineState1 method, ID3D12GraphicsCommandList4.SetPipelineState1, ID3D12GraphicsCommandList4::SetPipelineState1, SetPipelineState1, SetPipelineState1 method, SetPipelineState1 method,ID3D12GraphicsCommandList4 interface, d3d12/ID3D12GraphicsCommandList4::SetPipelineState1, direct3d12.id3d12graphicscommandlist4_setpipelinestate1
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
ms.custom: RS5, 19H1
f1_keywords:
 - ID3D12GraphicsCommandList4::SetPipelineState1
 - d3d12/ID3D12GraphicsCommandList4::SetPipelineState1
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
 - ID3D12GraphicsCommandList4.SetPipelineState1
---

# ID3D12GraphicsCommandList4::SetPipelineState1


## -description

Sets a state object on the command list.

## -parameters

### -param pStateObject

The state object to set on the command list. In the current release, this can only be of type <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_state_object_type">D3D12_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE</a>.

## -remarks

This method can be called from graphics or compute command lists and bundles.

This method is an alternative to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate">ID3D12GraphicsCommandList::SetPipelineState</a>, which is only defined for graphics and compute shaders.  There is only one pipeline state active on a command list at a time, so either call sets the current pipeline state.  The distinction between the calls is that each sets particular types of pipeline state only.  In the current release, <b>SetPipelineState1</b> is only used for setting raytracing pipeline state.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12graphicscommandlist4.md">ID3D12GraphicsCommandList4</a>
