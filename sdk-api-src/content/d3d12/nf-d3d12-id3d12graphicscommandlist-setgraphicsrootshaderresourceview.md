---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetGraphicsRootShaderResourceView
title: ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView (d3d12.h)
description: Sets a CPU descriptor handle for the shader resource in the graphics root signature.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetGraphicsRootShaderResourceView method","ID3D12GraphicsCommandList.SetGraphicsRootShaderResourceView","ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView","SetGraphicsRootShaderResourceView","SetGraphicsRootShaderResourceView method","SetGraphicsRootShaderResourceView method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView","direct3d12.id3d12graphicscommandlist_setgraphicsrootshaderresourceview"]
old-location: direct3d12\id3d12graphicscommandlist_setgraphicsrootshaderresourceview.htm
tech.root: direct3d12
ms.assetid: F16C8511-FF42-4DB3-81F7-9735FB1AADD7
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetGraphicsRootShaderResourceView method, ID3D12GraphicsCommandList.SetGraphicsRootShaderResourceView, ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView, SetGraphicsRootShaderResourceView, SetGraphicsRootShaderResourceView method, SetGraphicsRootShaderResourceView method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView, direct3d12.id3d12graphicscommandlist_setgraphicsrootshaderresourceview
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
 - ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView
 - d3d12/ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView
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
 - ID3D12GraphicsCommandList.SetGraphicsRootShaderResourceView
---

# ID3D12GraphicsCommandList::SetGraphicsRootShaderResourceView


## -description

Sets a CPU descriptor handle for the shader resource in the graphics root signature.

## -parameters

### -param RootParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The slot number for binding.

### -param BufferLocation [in]

Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>

The GPU virtual address of the Buffer.
            Textures are not supported. D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd alias of UINT64.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>