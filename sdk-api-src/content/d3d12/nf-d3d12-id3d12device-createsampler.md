---
UID: NF:d3d12.ID3D12Device.CreateSampler
title: ID3D12Device::CreateSampler (d3d12.h)
description: Create a sampler object that encapsulates sampling information for a texture.
helpviewer_keywords: ["CreateSampler","CreateSampler method","CreateSampler method","ID3D12Device interface","ID3D12Device interface","CreateSampler method","ID3D12Device.CreateSampler","ID3D12Device::CreateSampler","d3d12/ID3D12Device::CreateSampler","direct3d12.id3d12device_createsampler"]
old-location: direct3d12\id3d12device_createsampler.htm
tech.root: direct3d12
ms.assetid: 453B2D3D-843E-4DB0-BC47-59BD9C78BFD6
ms.date: 12/05/2018
ms.keywords: CreateSampler, CreateSampler method, CreateSampler method,ID3D12Device interface, ID3D12Device interface,CreateSampler method, ID3D12Device.CreateSampler, ID3D12Device::CreateSampler, d3d12/ID3D12Device::CreateSampler, direct3d12.id3d12device_createsampler
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device::CreateSampler
 - d3d12/ID3D12Device::CreateSampler
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
 - ID3D12Device.CreateSampler
---

# ID3D12Device::CreateSampler


## -description

Create a sampler object that encapsulates sampling information for a texture.

## -parameters

### -param pDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc">D3D12_SAMPLER_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_sampler_desc">D3D12_SAMPLER_DESC</a> structure that describes the sampler.

### -param DestDescriptor [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the sampler.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>