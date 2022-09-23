---
UID: NF:d3d12.ID3D12Device.CreateRenderTargetView
title: ID3D12Device::CreateRenderTargetView (d3d12.h)
description: Creates a render-target view for accessing resource data. (ID3D12Device.CreateRenderTargetView)
helpviewer_keywords: ["CreateRenderTargetView","CreateRenderTargetView method","CreateRenderTargetView method","ID3D12Device interface","ID3D12Device interface","CreateRenderTargetView method","ID3D12Device.CreateRenderTargetView","ID3D12Device::CreateRenderTargetView","d3d12/ID3D12Device::CreateRenderTargetView","direct3d12.id3d12device_createrendertargetview"]
old-location: direct3d12\id3d12device_createrendertargetview.htm
tech.root: direct3d12
ms.assetid: B5BFAE54-4FAC-47E5-A7F1-3F9E78FED3B4
ms.date: 12/05/2018
ms.keywords: CreateRenderTargetView, CreateRenderTargetView method, CreateRenderTargetView method,ID3D12Device interface, ID3D12Device interface,CreateRenderTargetView method, ID3D12Device.CreateRenderTargetView, ID3D12Device::CreateRenderTargetView, d3d12/ID3D12Device::CreateRenderTargetView, direct3d12.id3d12device_createrendertargetview
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
 - ID3D12Device::CreateRenderTargetView
 - d3d12/ID3D12Device::CreateRenderTargetView
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
 - ID3D12Device.CreateRenderTargetView
---

# ID3D12Device::CreateRenderTargetView


## -description

Creates a render-target view for accessing resource data.

## -parameters

### -param pResource [in, optional]

Type: <b><a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a> object that represents the render target.
          

At least one of <i>pResource</i> or <i>pDesc</i>  must be provided.
A null <i>pResource</i> is used to initialize a null descriptor, which guarantees D3D11-like null binding behavior (reading 0s, writes are discarded), but must have a valid <i>pDesc</i> in order to determine the descriptor type.

### -param pDesc [in, optional]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc">D3D12_RENDER_TARGET_VIEW_DESC</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_target_view_desc">D3D12_RENDER_TARGET_VIEW_DESC</a> structure that describes the render-target view.

A null <i>pDesc</i> is used to initialize a default descriptor, if possible. This behavior is identical to the D3D11 null descriptor behavior, where defaults are filled in. This behavior inherits the resource format and dimension (if not typeless) and RTVs target the first mip and all array slices. Not all resources support null descriptor initialization.

### -param DestDescriptor [in]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle">D3D12_CPU_DESCRIPTOR_HANDLE</a></b>

Describes the CPU descriptor handle that represents the destination where the newly-created render target view will reside.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>
