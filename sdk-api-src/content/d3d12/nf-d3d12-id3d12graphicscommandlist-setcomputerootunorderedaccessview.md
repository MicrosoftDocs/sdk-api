---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetComputeRootUnorderedAccessView
title: ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView (d3d12.h)
description: Sets a CPU descriptor handle for the unordered-access-view resource in the compute root signature.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetComputeRootUnorderedAccessView method","ID3D12GraphicsCommandList.SetComputeRootUnorderedAccessView","ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView","SetComputeRootUnorderedAccessView","SetComputeRootUnorderedAccessView method","SetComputeRootUnorderedAccessView method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView","direct3d12.id3d12graphicscommandlist_setcomputerootunorderedaccessview"]
old-location: direct3d12\id3d12graphicscommandlist_setcomputerootunorderedaccessview.htm
tech.root: direct3d12
ms.assetid: 7C91B305-ABB2-4355-AA4B-3E1641ACF9E0
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetComputeRootUnorderedAccessView method, ID3D12GraphicsCommandList.SetComputeRootUnorderedAccessView, ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView, SetComputeRootUnorderedAccessView, SetComputeRootUnorderedAccessView method, SetComputeRootUnorderedAccessView method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView, direct3d12.id3d12graphicscommandlist_setcomputerootunorderedaccessview
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
 - ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView
 - d3d12/ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView
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
 - ID3D12GraphicsCommandList.SetComputeRootUnorderedAccessView
---

# ID3D12GraphicsCommandList::SetComputeRootUnorderedAccessView


## -description

Sets a CPU descriptor handle for the unordered-access-view resource in the compute root signature.

## -parameters

### -param RootParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The slot number for binding.

### -param BufferLocation [in]

Type: <b>D3D12_GPU_VIRTUAL_ADDRESS</b>

The GPU virtual address of the buffer.
            D3D12_GPU_VIRTUAL_ADDRESS is a typedef'd alias of UINT64.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>