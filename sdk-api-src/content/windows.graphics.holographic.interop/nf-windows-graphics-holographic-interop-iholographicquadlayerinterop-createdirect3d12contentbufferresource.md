---
UID: NF:windows.graphics.holographic.interop.IHolographicQuadLayerInterop.CreateDirect3D12ContentBufferResource
title: IHolographicQuadLayerInterop::CreateDirect3D12ContentBufferResource
description: Creates a Direct3D 12 resource for use as a content buffer for the layer.
tech.root: direct3d12
ms.date: 12/12/2019
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: windows.graphics.holographic.interop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - windows.graphics.holographic.interop.h
api_name:
 - IHolographicQuadLayerInterop::CreateDirect3D12ContentBufferResource
f1_keywords:
 - IHolographicQuadLayerInterop::CreateDirect3D12ContentBufferResource
 - windows.graphics.holographic.interop/IHolographicQuadLayerInterop::CreateDirect3D12ContentBufferResource
dev_langs:
 - c++
---

## -description

The **CreateDirect3D12ContentBufferResource** method creates a Direct3D 12 resource for use as a back buffer for the corresponding [HolographicQuadLayer](/uwp/api/windows.graphics.holographic.holographicquadlayer) API object.

The [D3D12_RESOURCE_DESC](../d3d12/ns-d3d12-d3d12_resource_desc.md) structure can contain any set of valid initial values. Any values that won't work with this quad layer object will be overridden in the struct indicated by *pTexture2DDesc*, which is not an optional parameter. The resource is created so that it is already committed to a heap.

## -parameters

### -param pDevice

Type: **[ID3D12Device](../d3d12/nn-d3d12-id3d12device.md)\***

A Direct3D 12 device, which will be used to create the resource.

### -param pTexture2DDesc

Type: **[D3D12_RESOURCE_DESC](../d3d12/ns-d3d12-d3d12_resource_desc.md)\***

The Direct3D 12 resource description. This parameter is not optional.

**CreateDirect3D12ContentBufferResource** adjusts the description as needed to comply with platform requirements, such as buffer size or format restrictions, which are determined at runtime. Your application should inspect the descriptor for the texture returned in *ppCreatedTexture2DResource*, and respond appropriately to any differences from what was specified.

### -param ppTexture2DResource

Type: **[ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md)\*\***

If successful, the Direct3D 12 2D texture resource for use as a content buffer. Otherwise, `nullptr`.

## -returns

**S_OK** if successful, otherwise returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) error code indicating the reason for failure. Also see [COM Error Codes (UI, Audio, DirectX, Codec)](/windows/win32/com/com-error-codes-10).

## -see-also