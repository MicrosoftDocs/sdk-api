---
UID: NF:windows.graphics.directx.direct3d11.interop.CreateDirect3DSurface
title: interop::CreateDirect3DSurface
ms.date: 05/10/2019
ms.keywords: interop::CreateDirect3DSurface
ms.topic: function
author: windows-sdk-content
description: Creates an instance of [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) from an [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface).
tech.root: direct3d11
ms.author: windowssdkdev
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: D3D11.dll
req.header: windows.graphics.directx.direct3d11.interop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: D3D11.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - D3D11.dll
api_name:
 - interop::CreateDirect3DSurface
---

## -description
Creates an instance of [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) from an [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface).

## -parameters

### -param dxgiSurface [in]
Type: **[IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)\***

The [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) to create the IDirect3D11Surface from.

## -returns
Type: **[IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface)\^**

Returns the created [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) instance.

## -remarks
While we recommend [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/index), if you're using C++/CX, then you should use this function. Otherwise, you should use the [CreateDirect3D11SurfaceFromDXGISurface](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) function instead.

## -see-also
