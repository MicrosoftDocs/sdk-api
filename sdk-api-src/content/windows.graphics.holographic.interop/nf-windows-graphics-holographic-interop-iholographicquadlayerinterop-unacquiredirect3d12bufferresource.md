---
UID: NF:windows.graphics.holographic.interop.IHolographicQuadLayerInterop.UnacquireDirect3D12BufferResource
title: IHolographicQuadLayerInterop::UnacquireDirect3D12BufferResource
description: The IHolographicQuadLayerInterop::UnacquireDirect3D12BufferResource function un-acquires a Direct3D 12 buffer resource.
tech.root: direct3d12
ms.date: 08/03/2022
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
 - IHolographicQuadLayerInterop::UnacquireDirect3D12BufferResource
f1_keywords:
 - IHolographicQuadLayerInterop::UnacquireDirect3D12BufferResource
 - windows.graphics.holographic.interop/IHolographicQuadLayerInterop::UnacquireDirect3D12BufferResource
dev_langs:
 - c++
---

## -description

The **UnacquireDirect3D12BufferResource** method relinquishes control of a Direct3D 12 buffer resource to the platform.

A resource that has been acquired, but not submitted, can be un-acquired to return control of the buffer back to the platform. A resource that has been un-acquired can be re-acquired at a later time.

## -parameters

### -param pResourceToUnacquire

Type: **[ID3D12Resource](../d3d12/nn-d3d12-id3d12resource.md)\***

The Direct3D 12 resource to relinquish control of.

## -returns

**S_OK** if successful, otherwise returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) error code indicating the reason for failure. Also see [COM Error Codes (UI, Audio, DirectX, Codec)](/windows/win32/com/com-error-codes-10).

## -see-also
