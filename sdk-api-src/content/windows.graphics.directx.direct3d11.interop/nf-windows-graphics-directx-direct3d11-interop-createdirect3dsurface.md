---
UID: NF:windows.graphics.directx.direct3d11.interop.CreateDirect3DSurface
title: CreateDirect3DSurface
description: Creates an instance of [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) from an [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface).
helpviewer_keywords: ["interop::CreateDirect3DSurface"]
tech.root: winrt
ms.assetid: 01a51e06-4c21-bffb-212e-cea0f718e519
ms.date: 05/13/2019
ms.keywords: interop::CreateDirect3DSurface
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
targetos: Windows
f1_keywords:
 - CreateDirect3DSurface
 - windows.graphics.directx.direct3d11.interop/CreateDirect3DSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
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

