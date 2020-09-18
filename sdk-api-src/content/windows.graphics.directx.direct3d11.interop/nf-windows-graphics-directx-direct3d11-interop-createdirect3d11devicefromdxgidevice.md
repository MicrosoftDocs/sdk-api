---
UID: NF:windows.graphics.directx.direct3d11.interop.CreateDirect3D11DeviceFromDXGIDevice
title: CreateDirect3D11DeviceFromDXGIDevice function
description: Creates an instance of IDirect3DDevice from an IDXGIDevice.
helpviewer_keywords: ["DF768592-3A0D-4FEA-AE30-CDD5406CAC9D","CreateDirect3D11DeviceFromDXGIDevice","CreateDirect3D11DeviceFromDXGIDevice function [Direct3D 11]","windows.graphics.directx.direct3d11.interop/CreateDirect3D11DeviceFromDXGIDevice","direct3d11.createdirect3d11devicefromdxgidevice"]
tech.root: winrt
ms.assetid: DF768592-3A0D-4FEA-AE30-CDD5406CAC9D
ms.date: 05/13/2019
ms.keywords: DF768592-3A0D-4FEA-AE30-CDD5406CAC9D, CreateDirect3D11DeviceFromDXGIDevice, CreateDirect3D11DeviceFromDXGIDevice function [Direct3D 11], windows.graphics.directx.direct3d11.interop/CreateDirect3D11DeviceFromDXGIDevice, direct3d11.createdirect3d11devicefromdxgidevice
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
 - CreateDirect3D11DeviceFromDXGIDevice
 - windows.graphics.directx.direct3d11.interop/CreateDirect3D11DeviceFromDXGIDevice
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
 - CreateDirect3D11DeviceFromDXGIDevice
---

# CreateDirect3D11DeviceFromDXGIDevice function


## -description

Creates an instance of [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) from an [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice).

## -parameters

### -param dxgiDevice [in]

Type: **[IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)\***

The [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) to create the Direct3DDevice from.

### -param graphicsDevice [out]

Type: **[IInspectable](/windows/desktop/api/inspectable/nn-inspectable-iinspectable)\*\***

A Direct3DDevice instance that wraps the DXGIDevice.

## -returns

Type: [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).

## -remarks

While we recommend [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/index), if you're using C++/CX then you should call [CreateDirect3DDevice](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) instead of **CreateDirect3D11DeviceFromDXGIDevice**. If you're using WRL then **CreateDirect3D11DeviceFromDXGIDevice** can be used as shown in this code example.

```cpp
using namespace Microsoft::WRL;
ComPtr<ABI::Windows::Graphics::DirectX::Direct3D11::IDirect3DDevice> device;
ComPtr<IInspectable> inspectableSurface;
If (SUCCEEDED(CreateDirect3D11DeviceFromDXGIDevice(dxgiDevice, &inspectableSurface))
{
    hr = inspectableSurface.As(&device);
}
```

## -see-also

[Core functions](/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-functions)