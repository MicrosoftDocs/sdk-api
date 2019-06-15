---
UID: NF:d2d1.ID2D1Factory.CreateDxgiSurfaceRenderTarget
title: ID2D1Factory::CreateDxgiSurfaceRenderTarget (d2d1.h)
author: windows-sdk-content
description: Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface.
old-location: direct2d\id2d1factory_createdxgisurfacerendertarget.htm
tech.root: Direct2D
ms.assetid: 101744ea-97bc-4f92-88b0-fcdf0e4aaf4e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateDxgiSurfaceRenderTarget, CreateDxgiSurfaceRenderTarget methods [Direct2D], ID2D1Factory.CreateDxgiSurfaceRenderTarget, ID2D1Factory::CreateDxgiSurfaceRenderTarget, d2d1/CreateDxgiSurfaceRenderTarget, direct2d.id2d1factory_createdxgisurfacerendertarget
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory::CreateDxgiSurfaceRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory::CreateDxgiSurfaceRenderTarget


## -description


<span>Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)">CreateDxgiSurfaceRenderTarget(IDXGISurface*,D2D1_RENDER_TARGET_PROPERTIES&,ID2D1RenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371260(v=vs.85)">CreateDxgiSurfaceRenderTarget(IDXGISurface*,D2D1_RENDER_TARGET_PROPERTIES*,ID2D1RenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface. 

</td>
</tr>
</table>

## -parameters


## -remarks



To write to a Direct3D surface, you obtain an <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> and pass it to the <b>CreateDxgiSurfaceRenderTarget</b> method to create a DXGI surface render target; you can then use the DXGI surface render target to draw 2-D content to the DXGI surface.  

A DXGI surface render target is a type of <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>. Like other Direct2D render targets, you can use it to create resources and issue drawing commands. 

The DXGI surface render target and the DXGI surface must use the same DXGI format. If you specify the <a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_UNKOWN</a> format when you create the render target, it will automatically use the surface's format.

The DXGI surface render target does not perform DXGI surface synchronization. 

To work with Direct2D, the Direct3D device that provides the <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">IDXGISurface</a> must be created with the <b>D3D10_CREATE_DEVICE_BGRA_SUPPORT</b> flag.

For more information about creating and using DXGI surface render targets, see the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-and-direct3d-interoperation-overview">Direct2D and Direct3D Interoperability Overview</a>.

When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU. By creating a render target once and retaining it as long as possible, you gain performance benefits. Your application should create render targets once and hold onto them for the life of the application or until the render target's <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> method returns the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created). 




#### Examples

The following example obtains a  DXGI surface  (<i>pBackBuffer</i>) from an <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a> and uses it to create a DXGI surface render target.


```cpp
// Get a surface in the swap chain
hr = m_pSwapChain->GetBuffer(
    0,
    IID_PPV_ARGS(&pBackBuffer)
    );

```

```cpp
    if (SUCCEEDED(hr))
    {

```

```cpp
        // Create the DXGI Surface Render Target.
        FLOAT dpiX;
        FLOAT dpiY;
        m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                dpiX,
                dpiY
                );

        // Create a Direct2D render target which can draw into the surface in the swap chain

```

```cpp
        hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pBackBuffer,
            &props,
            &m_pBackBufferRT
            );

    }

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-and-direct3d-interoperation-overview">Direct2D and Direct3D Interoperability Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>
 

 

