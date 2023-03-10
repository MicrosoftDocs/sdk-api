---
UID: NF:windows.graphics.directx.direct3d11.interop.CreateDirect3D11SurfaceFromDXGISurface
title: CreateDirect3D11SurfaceFromDXGISurface function
description: Creates an instance of IDirect3DSurface from an IDXGISurface.
helpviewer_keywords: ["81213ad6-5736-1d54-c0a6-628697437568","CreateDirect3D11SurfaceFromDXGISurface","CreateDirect3D11SurfaceFromDXGISurface function [Direct3D 11]","windows.graphics.directx.direct3d11.interop/CreateDirect3D11SurfaceFromDXGISurface","direct3d11.createdirect3d11surfacefromdxgisurface"]
tech.root: winrt
ms.assetid: 81213ad6-5736-1d54-c0a6-628697437568
ms.date: 05/13/2019
ms.keywords: 81213ad6-5736-1d54-c0a6-628697437568, CreateDirect3D11SurfaceFromDXGISurface, CreateDirect3D11SurfaceFromDXGISurface function [Direct3D 11], windows.graphics.directx.direct3d11.interop/CreateDirect3D11SurfaceFromDXGISurface, direct3d11.createdirect3d11surfacefromdxgisurface
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
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - CreateDirect3D11SurfaceFromDXGISurface
 - windows.graphics.directx.direct3d11.interop/CreateDirect3D11SurfaceFromDXGISurface
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
 - CreateDirect3D11SurfaceFromDXGISurface
---

# CreateDirect3D11SurfaceFromDXGISurface function


## -description

Creates an instance of [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) from an [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface).

## -parameters

### -param dxgiSurface [in]

Type: **[IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)\***

The [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) to create the IDirect3D11Surface from.

### -param graphicsSurface [out]

Type: **[IInspectable](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)\*\***

An [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) instance that wraps the [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface).

## -returns

Type: [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

While we recommend [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/index), if you're using C++/CX then you should call [CreateDirect3DSurface](./nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface.md) instead of **CreateDirect3D11DeviceFromDXGIDevice**. If you're using WRL then **CreateDirect3D11DeviceFromDXGIDevice** can be used as shown in this code example.

```cpp
using namespace Microsoft::WRL;
ComPtr<ABI::Windows::Graphics::DirectX::Direct3D11::IDirect3DSurface> surface;
ComPtr<IInspectable> inspectableSurface;
If (SUCCEEDED(CreateDirect3D11SurfaceFromDXGISurface(dxgiSurface, &inspectableSurface))
{
    hr = inspectableSurface.As(&surface);
}
```

## -see-also

[Core functions](/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-functions)