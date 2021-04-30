---
UID: NF:d3d12.ID3D12Device.CreateDepthStencilView
title: ID3D12Device::CreateDepthStencilView (d3d12.h)
description: Creates a depth-stencil view for accessing resource data.
helpviewer_keywords: ["CreateDepthStencilView","CreateDepthStencilView method","CreateDepthStencilView method","ID3D12Device interface","ID3D12Device interface","CreateDepthStencilView method","ID3D12Device.CreateDepthStencilView","ID3D12Device::CreateDepthStencilView","d3d12/ID3D12Device::CreateDepthStencilView","direct3d12.id3d12device_createdepthstencilview"]
old-location: direct3d12\id3d12device_createdepthstencilview.htm
tech.root: direct3d12
ms.assetid: 57C0CA35-CFBE-4D79-B8D7-BD01CEBEA144
ms.date: 12/05/2018
ms.keywords: CreateDepthStencilView, CreateDepthStencilView method, CreateDepthStencilView method,ID3D12Device interface, ID3D12Device interface,CreateDepthStencilView method, ID3D12Device.CreateDepthStencilView, ID3D12Device::CreateDepthStencilView, d3d12/ID3D12Device::CreateDepthStencilView, direct3d12.id3d12device_createdepthstencilview
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
 - ID3D12Device::CreateDepthStencilView
 - d3d12/ID3D12Device::CreateDepthStencilView
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
 - ID3D12Device.CreateDepthStencilView
---

# ID3D12Device::CreateDepthStencilView


## -description

Creates a depth-stencil view for accessing resource data.

## -parameters

### -param pResource [in, optional]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> object that represents the depth stencil.
          

At least one of <i>pResource</i> or <i>pDesc</i>  must be provided.
A null <i>pResource</i> is used to initialize a null descriptor, which guarantees D3D11-like null binding behavior (reading 0s, writes are discarded), but must have a valid <i>pDesc</i> in order to determine the descriptor type.

### -param pDesc [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc">D3D12_DEPTH_STENCIL_VIEW_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure that describes the depth-stencil view.
          

A null <i>pDesc</i> is used to initialize a default descriptor, if possible. This behavior is identical to the D3D11 null descriptor behavior, where defaults are filled in. This behavior inherits the resource format and dimension (if not typeless) and DSVs target the  first mip and all array slices. Not all resources support null descriptor initialization.

### -param DestDescriptor [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the start of the heap that holds the depth-stencil view.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>