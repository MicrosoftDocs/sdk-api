---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetComputeRootConstantBufferView
title: ID3D12GraphicsCommandList::SetComputeRootConstantBufferView (d3d12.h)
description: Sets a CPU descriptor handle for the constant buffer in the compute root signature.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetComputeRootConstantBufferView method","ID3D12GraphicsCommandList.SetComputeRootConstantBufferView","ID3D12GraphicsCommandList::SetComputeRootConstantBufferView","SetComputeRootConstantBufferView","SetComputeRootConstantBufferView method","SetComputeRootConstantBufferView method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetComputeRootConstantBufferView","direct3d12.id3d12graphicscommandlist_setcomputerootconstantbufferview"]
old-location: direct3d12\id3d12graphicscommandlist_setcomputerootconstantbufferview.htm
tech.root: direct3d12
ms.assetid: AEAB392F-365F-4EDB-AC57-FFAC40C800C0
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetComputeRootConstantBufferView method, ID3D12GraphicsCommandList.SetComputeRootConstantBufferView, ID3D12GraphicsCommandList::SetComputeRootConstantBufferView, SetComputeRootConstantBufferView, SetComputeRootConstantBufferView method, SetComputeRootConstantBufferView method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetComputeRootConstantBufferView, direct3d12.id3d12graphicscommandlist_setcomputerootconstantbufferview
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
 - ID3D12GraphicsCommandList::SetComputeRootConstantBufferView
 - d3d12/ID3D12GraphicsCommandList::SetComputeRootConstantBufferView
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
 - ID3D12GraphicsCommandList.SetComputeRootConstantBufferView
---

# ID3D12GraphicsCommandList::SetComputeRootConstantBufferView


## -description

Sets a CPU descriptor handle for the constant buffer in the compute root signature.

## -parameters

### -param RootParameterIndex [in]

Type: <b>UINT</b>

The slot number for binding.

### -param BufferLocation [in]

Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>

Specifies the D3D12_GPU_VIRTUAL_ADDRESS of the constant buffer.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>