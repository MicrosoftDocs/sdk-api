---
UID: NN:windows.graphics.directx.direct3d11.interop.IDirect3DDxgiInterfaceAccess
title: IDirect3DDxgiInterfaceAccess (windows.graphics.directx.direct3d11.interop.h)
author: windows-sdk-content
description: IDirect3DDxgiInterfaceAccess is a COM interface, which must be implemented by anything that implements IDirect3DDevice or IDirect3DSurface.
tech.root: direct3d11
ms.assetid: 95B3D1FF-AED4-44E1-AD83-16C070F30194
ms.author: windowssdkdev
ms.date: 04/25/2019
ms.keywords: IDirect3DDxgiInterfaceAccess, IDirect3DDxgiInterfaceAccess interface, IDirect3DDxgiInterfaceAccess interface,described, windows.graphics.directx.direct3d11.interop.idirect3ddxgiInterfaceaccess, windows/IDirect3DDxgiInterfaceAccess
ms.topic: interface
req.header: windows.graphics.directx.direct3d11.interop.h
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
req.namespace: Windows::Graphics::DirectX::Direct3D11
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.graphics.directx.direct3d11.interop.h
api_name:
 - IDirect3DDxgiInterfaceAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDxgiInterfaceAccess interface

## -description

IDirect3DDxgiInterfaceAccess is a COM interface, which must be implemented by anything that implements [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) or [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface).

## Inheritance

The **ID3D12GraphicsCommandList5** interface inherits from the [IUnknown interface](/windows/desktop/api/unknwn/nn-unknwn-iunknown).

## -members

The **ID3D12GraphicsCommandList5** interface has these methods.

|Method|Description|
|-|-|
|[GetInterface](nf-windows-graphics-directx-direct3d11-interop-idirect3ddxgiInterfaceaccess-getinterface.md)|Retrieves the DXGI interface that is wrapped by the IDirect3DDxgiInterfaceAccess object.|

## -see-also

[Core interfaces](/windows/desktop/direct3d12/direct3d-12-interfaces)
