---
UID: NF:d2d1.ID2D1Factory.CreateDxgiSurfaceRenderTarget(IDXGISurface,constD2D1_RENDER_TARGET_PROPERTIES,ID2D1RenderTarget)
title: ID2D1Factory::CreateDxgiSurfaceRenderTarget
description: Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface. (overload 2/2)
helpviewer_keywords: ["CreateDxgiSurfaceRenderTarget","CreateDxgiSurfaceRenderTarget methods [Direct2D]","ID2D1Factory.CreateDxgiSurfaceRenderTarget","ID2D1Factory::CreateDxgiSurfaceRenderTarget","d2d1/CreateDxgiSurfaceRenderTarget","direct2d.id2d1factory_createdxgisurfacerendertarget"]
old-location: direct2d\id2d1factory_createdxgisurfacerendertarget.htm
tech.root: Direct2D
ms.assetid: 101744ea-97bc-4f92-88b0-fcdf0e4aaf4e
ms.date: 12/05/2018
ms.keywords: CreateDxgiSurfaceRenderTarget, CreateDxgiSurfaceRenderTarget methods [Direct2D], ID2D1Factory.CreateDxgiSurfaceRenderTarget, ID2D1Factory::CreateDxgiSurfaceRenderTarget, d2d1/CreateDxgiSurfaceRenderTarget, direct2d.id2d1factory_createdxgisurfacerendertarget
req.header: d2d1.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Factory::CreateDxgiSurfaceRenderTarget
 - d2d1/ID2D1Factory::CreateDxgiSurfaceRenderTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory::CreateDxgiSurfaceRenderTarget
---

## -description

Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface.

## -parameters

### -param dxgiSurface [in]

Type: <b><a href="/windows/win32/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a>*</b>

The IDXGISurface to which the render target will draw.

### -param renderTargetProperties [in]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>*</b>

The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering. For information about supported pixel formats, see  <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel  Formats and Alpha Modes</a>.

### -param renderTarget [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>**</b>

When this method returns, contains the address of the pointer to the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a> object created by this method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

To write to a Direct3D surface, you obtain an <a href="/windows/win32/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> and pass it to the CreateDxgiSurfaceRenderTarget method to create a DXGI surface render target; you can then use the DXGI surface render target to draw 2-D content to the DXGI surface.  

A DXGI surface render target is a type of <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>. Like other Direct2D render targets, you can use it to create resources and issue drawing commands. 

The DXGI surface render target and the DXGI surface must use the same DXGI format. If you specify the <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_UNKOWN</a> format when you create the render target, it will automatically use the surface's format.

The DXGI surface render target does not perform DXGI surface synchronization. 

For more information about creating and using DXGI surface render targets, see the <a href="/windows/win32/Direct2D/direct2d-and-direct3d-interoperation-overview">Direct2D and Direct3D Interoperability Overview</a>.

To work with Direct2D, the Direct3D device that provides the <a href="/windows/win32/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> must be created with the <b>D3D10_CREATE_DEVICE_BGRA_SUPPORT</b> flag.

When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU. By creating a render target once and retaining it as long as possible, you gain performance benefits. Your application should create render targets once and hold onto them for the life of the application or until the render target's <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> method returns the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created). 

## Examples

The following example obtains a DXGI surface (<i>pBackBuffer</i>) from an <a href="/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a> and uses it to create a DXGI surface render target.

```cpp
// Initialize *hwnd* with the handle of the window displaying the rendered content.
HWND hwnd;

// Get a surface in the swap chain
hr = m_pSwapChain->GetBuffer(
    0,
    IID_PPV_ARGS(&pBackBuffer));

if (SUCCEEDED(hr))
{
    // Create the DXGI Surface Render Target.
    float dpi = GetDpiForWindow(hwnd);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpi,
            dpi
            );

    // Create a Direct2D render target that can draw into the surface in the swap chain.

    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT);
}
```

## -see-also

[CreateDxgiSurfaceRenderTarget(IDXGISurface,const D2D1_RENDER_TARGET_PROPERTIES &,ID2D1RenderTarget)](./nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget).md)

<a href="/windows/win32/Direct2D/direct2d-and-direct3d-interoperation-overview">Direct2D and Direct3D interoperability overview</a>

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>
