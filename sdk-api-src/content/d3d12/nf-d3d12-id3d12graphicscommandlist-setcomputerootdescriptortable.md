---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetComputeRootDescriptorTable
title: ID3D12GraphicsCommandList::SetComputeRootDescriptorTable (d3d12.h)
description: Sets a descriptor table into the compute root signature.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetComputeRootDescriptorTable method","ID3D12GraphicsCommandList.SetComputeRootDescriptorTable","ID3D12GraphicsCommandList::SetComputeRootDescriptorTable","SetComputeRootDescriptorTable","SetComputeRootDescriptorTable method","SetComputeRootDescriptorTable method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetComputeRootDescriptorTable","direct3d12.id3d12graphicscommandlist_setcomputerootdescriptortable"]
old-location: direct3d12\id3d12graphicscommandlist_setcomputerootdescriptortable.htm
tech.root: direct3d12
ms.assetid: DC05D64A-39D0-4EF2-A9FE-956B499386F2
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetComputeRootDescriptorTable method, ID3D12GraphicsCommandList.SetComputeRootDescriptorTable, ID3D12GraphicsCommandList::SetComputeRootDescriptorTable, SetComputeRootDescriptorTable, SetComputeRootDescriptorTable method, SetComputeRootDescriptorTable method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetComputeRootDescriptorTable, direct3d12.id3d12graphicscommandlist_setcomputerootdescriptortable
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
 - ID3D12GraphicsCommandList::SetComputeRootDescriptorTable
 - d3d12/ID3D12GraphicsCommandList::SetComputeRootDescriptorTable
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
 - ID3D12GraphicsCommandList.SetComputeRootDescriptorTable
---

# ID3D12GraphicsCommandList::SetComputeRootDescriptorTable


## -description

Sets a descriptor table into the compute root signature.

## -parameters

### -param RootParameterIndex [in]

Type: <b>UINT</b>

The slot number for binding.

### -param BaseDescriptor [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle">D3D12_GPU_DESCRIPTOR_HANDLE</a></b>

A GPU_descriptor_handle object for the base descriptor to set.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>