---
UID: NF:d3d12.ID3D12Device.CreateConstantBufferView
title: ID3D12Device::CreateConstantBufferView (d3d12.h)
description: Creates a constant-buffer view for accessing resource data.
helpviewer_keywords: ["CreateConstantBufferView","CreateConstantBufferView method","CreateConstantBufferView method","ID3D12Device interface","ID3D12Device interface","CreateConstantBufferView method","ID3D12Device.CreateConstantBufferView","ID3D12Device::CreateConstantBufferView","d3d12/ID3D12Device::CreateConstantBufferView","direct3d12.id3d12device_createconstantbufferview"]
old-location: direct3d12\id3d12device_createconstantbufferview.htm
tech.root: direct3d12
ms.assetid: 13251F82-4AE9-4234-A0C8-0E666F8A1856
ms.date: 12/05/2018
ms.keywords: CreateConstantBufferView, CreateConstantBufferView method, CreateConstantBufferView method,ID3D12Device interface, ID3D12Device interface,CreateConstantBufferView method, ID3D12Device.CreateConstantBufferView, ID3D12Device::CreateConstantBufferView, d3d12/ID3D12Device::CreateConstantBufferView, direct3d12.id3d12device_createconstantbufferview
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
 - ID3D12Device::CreateConstantBufferView
 - d3d12/ID3D12Device::CreateConstantBufferView
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
 - ID3D12Device.CreateConstantBufferView
---

# ID3D12Device::CreateConstantBufferView


## -description

Creates a constant-buffer view for accessing resource data.

## -parameters

### -param pDesc [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc">D3D12_CONSTANT_BUFFER_VIEW_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc">D3D12_CONSTANT_BUFFER_VIEW_DESC</a> structure that describes the constant-buffer view.

### -param DestDescriptor [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the constant-buffer view.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>