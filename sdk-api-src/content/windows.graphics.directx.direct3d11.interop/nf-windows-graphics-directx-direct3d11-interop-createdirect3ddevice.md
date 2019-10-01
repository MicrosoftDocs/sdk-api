---
UID: NF:windows.graphics.directx.direct3d11.interop.CreateDirect3DDevice
title: CreateDirect3DDevice
author: windows-sdk-content
description: Creates an instance of [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) from an [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice).
tech.root: WinRT
ms.assetid: 0eaed3be-e3d8-b431-68cc-e4e1baf5c6fe
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: interop::CreateDirect3DDevice
ms.topic: function
f1_keywords: 
 - "windows.graphics.directx.direct3d11.interop/interop::CreateDirect3DDevice"
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D11.dll
api_name:
 - interop::CreateDirect3DDevice
targetos: Windows
---

## -description
Creates an instance of [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) from an [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice).

## -parameters

### -param dxgiDevice [in]
Type: **[IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)\***

The [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) to create the Direct3DDevice from.

## -returns
Type: **[IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice)\^**

Returns the created [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) instance.

## -remarks
While we recommend [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/index), if you're using C++/CX, then you should use this function. Otherwise, you should use the [CreateDirect3D11DeviceFromDXGIDevice](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) function instead.

## -see-also
