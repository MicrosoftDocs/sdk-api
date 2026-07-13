---
UID: NF:windows.ui.composition.interop.ICompositionDrawingSurfaceInterop2.CopySurface
title: ICompositionDrawingSurfaceInterop2::CopySurface
description: Reads back the contents of a composition drawing surface (or a composition virtual drawing surface).
ms.date: 01/09/2020
tech.root: winrt
req.construct-type: function
req.header: windows.ui.composition.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - ICompositionDrawingSurfaceInterop2::CopySurface
 - windows.ui.composition.interop/ICompositionDrawingSurfaceInterop2::CopySurface
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - windows.ui.composition.interop.h
api_name:
 - ICompositionDrawingSurfaceInterop2::CopySurface
---

## -description

Reads back the contents of a composition drawing surface (or a composition virtual drawing surface).

## -parameters

### -param destinationResource [in]

Type: **[IUnknown](../unknwn/nn-unknwn-iunknown.md)\***

Represents the Direct3D texture that will receive the copy. You must have created this resource on the same Direct3D device as the one associated with the [CompositionGraphicsDevice](/uwp/api/Windows.UI.Composition.CompositionGraphicsDevice) that was used to create the source composition drawing surface (or composition virtual drawing surface).

### -param destinationOffsetX [in]

Type: **int**

The x-coordinate of an offset (into *destinationResource*) where the copy will be performed. No pixels above or to the left of this offset are changed by the copy operation. The argument can't be negative.

### -param destinationOffsetY [in]

Type: **int**

The y-coordinate of an offset (into *destinationResource*) where the copy will be performed. No pixels above or to the left of this offset are changed by the copy operation. The argument can't be negative.

### -param sourceRectangle [in]

Type: **const [RECT](../windef/ns-windef-rect.md)\***

An optional pointer to a constant **RECT** representing the rectangle on the source surface to copy out. The rectangle can't exceed the bounds of the source surface. In order to have enough room to receive the requested pixels, the destination resource must have at least as many pixels as the *destinationOffsetX* and *Y* parameters plus the width/height of this rectangle.

If this parameter is null, then the entire source surface is copied (and the source surface size is used to validate the size of the destination resource).

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

**S_OK** if successful, otherwise returns an [HRESULT](/windows/win32/com/structure-of-com-error-codes) error code indicating the reason for failure. Also see [COM Error Codes (UI, Audio, DirectX, Codec)](/windows/win32/com/com-error-codes-10).

## -remarks

To create a Direct2D or a Direct3D surface for use with [Windows.UI.Composition](/uwp/api/windows.ui.composition), you use the [composition drawing surface interoperation](./index.md) interfaces. You can use the **CopySurface** method to read back the contents of a composition drawing surface (or a composition virtual drawing surface). **CopySurface** is a synchronous and instantaneous copy from one part of video memory to another; you don't need to call **Commit**.

For any given composition drawing surface (or composition virtual drawing surface), your application can query for [ICompositionDrawingSurfaceInterop2](./nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2.md), and call **CopySurface** on that interface.

You can call **CopySurface** only when there are no pending updates to any surfaces belonging to the same [CompositionGraphicsDevice](/uwp/api/windows.ui.composition.compositiongraphicsdevice) as the source surface ([ICompositionDrawingSurfaceInterop::BeginDraw](./nf-windows-ui-composition-interop-icompositiondrawingsurfaceinterop-begindraw.md) has the same requirement). It's also illegal to call **CopySurface** on a non-virtual composition drawing surface that has never been updated, as its pixel contents are undefined. For virtual surfaces, since they are sparsely allocated, it's possible to specify a source rectangle that intersects uninitialized regions of the surface. In that case, the call is legal, but the result of the copy for those uninitialized regions is undefined.

> [!NOTE]
> This interface is available on Windows 10, version 1903 (10.0; Build 18362), but it is not defined in the `windows.ui.composition.interop.h` header file for that version of the Windows Software Development Kit (SDK). If you first obtain a pointer to an [ICompositionDrawingSurfaceInterop](./nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop.md) interface, you can then query that (via [QueryInterface](../unknwn/nf-unknwn-iunknown-queryinterface(refiid_void).md)) for a pointer to an [ICompositionDrawingSurfaceInterop2](./nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2.md) interface.

## Examples

For this scenario, we envisage a framework that uses **CompositionDrawingSurface** to grant the ability to render and compose custom content into a visual tree managed by the framework. The framework implements a low resource mode (to be used, for example, during application minimize or suspend). When in this mode, the framework releases most composition objects, including all surfaces. However, before releasing each surface, the framework extracts its pixels and compresses them (for example, using the PNG codec) so that it can reconstitute them later without having to call back into application code. This code example shows a helper function that the framework might implement to process each surface.

```cpp
HRESULT CompressSurface(_In_ ICompositionDrawingSurface* surface) 
{ 
    // Get the interop interface.
    ComPtr<ICompositionDrawingSurfaceInterop2> surfaceInterop; 
    RETURN_IF_FAILED(surface.As(&surfaceInterop)); 
 
    // Allocate a staging surface of equal size to the surface to compress.
    SizeInt32 size; 
    RETURN_IF_FAILED(surface->get_Size(&size)); 
 
    // Create a staging texture to receive a copy of the pixels.
    ComPtr<ID3D11Texture2D> stagingTexture; 
    RETURN_IF_FAILED(CreateStagingTexture(size, stagingTexture.GetAddressOf())); 
 
    // Copy the pixels out.
    RETURN_IF_FAILED(surfaceInterop->CopySurface(stagingTexture.get(), 0, 0, nullptr)); 
 
    // Compress the retrieved pixels.
    RETURN_IF_FAILED(CompressTexturePixels(stagingTexture.get())); 
 
    return S_OK; 
} 

HRESULT CreateStagingTexture(const SizeInt32& size, _Outptr_ ID3D11Texture2D** texture) 
{ 
    D3D11_TEXTURE2D_DESC surfaceDesc; 
 
    surfaceDesc.Width = size.Width; 
    surfaceDesc.Height = size.Height; 
    surfaceDesc.MipLevels = 1; 
    surfaceDesc.ArraySize = 1; 
    surfaceDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM; 
    surfaceDesc.SampleDesc.Count = 1; 
    surfaceDesc.SampleDesc.Quality = 0; 
    surfaceDesc.Usage = D3D11_USAGE_STAGING; 
    surfaceDesc.BindFlags = 0; 
    surfaceDesc.CPUAccessFlags = D3D11_CPU_ACCESS_READ; 
    surfaceDesc.MiscFlags = 0; 

    RETURN_IF_FAILED(g_d3d11Device->CreateTexture2D(surfaceDesc, false, texture)); 

    return S_OK; 
} 

HRESULT CompressTexturePixels(_In_ ID3D11Texture2D* texture) 
{ 
    // ... 
    // Map the texture, feed the pixels to WIC... 
    // ... 
} 
```

## -see-also

* [ICompositionDrawingSurfaceInterop interface](./nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop.md)
* [ICompositionDrawingSurfaceInterop2 interface](./nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2.md)
* [Composition native interoperation overview](/windows/uwp/composition/composition-native-interop)
