---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetGraphicsRootConstantBufferView
title: ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView (d3d12.h)
description: Sets a CPU descriptor handle for the constant buffer in the graphics root signature.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetGraphicsRootConstantBufferView method","ID3D12GraphicsCommandList.SetGraphicsRootConstantBufferView","ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView","SetGraphicsRootConstantBufferView","SetGraphicsRootConstantBufferView method","SetGraphicsRootConstantBufferView method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView","direct3d12.id3d12graphicscommandlist_setgraphicsrootconstantbufferview"]
old-location: direct3d12\id3d12graphicscommandlist_setgraphicsrootconstantbufferview.htm
tech.root: direct3d12
ms.assetid: 59F6E33A-9BD8-4ED3-8CA7-235E2A0C2686
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetGraphicsRootConstantBufferView method, ID3D12GraphicsCommandList.SetGraphicsRootConstantBufferView, ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView, SetGraphicsRootConstantBufferView, SetGraphicsRootConstantBufferView method, SetGraphicsRootConstantBufferView method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView, direct3d12.id3d12graphicscommandlist_setgraphicsrootconstantbufferview
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
 - ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView
 - d3d12/ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView
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
 - ID3D12GraphicsCommandList.SetGraphicsRootConstantBufferView
---

# ID3D12GraphicsCommandList::SetGraphicsRootConstantBufferView


## -description

Sets a CPU descriptor handle for the constant buffer in the graphics root signature.

## -parameters

### -param RootParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The slot number for binding.

### -param BufferLocation [in]

Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>

The GPU virtual address of the constant buffer.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd alias of UINT64.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>