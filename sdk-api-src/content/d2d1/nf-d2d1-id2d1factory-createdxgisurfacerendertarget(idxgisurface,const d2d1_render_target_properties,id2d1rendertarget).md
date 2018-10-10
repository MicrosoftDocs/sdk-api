---
UID: NF:d2d1.ID2D1Factory.CreateDxgiSurfaceRenderTarget(IDXGISurface,const D2D1_RENDER_TARGET_PROPERTIES,ID2D1RenderTarget)
title: ID2D1Factory::CreateDxgiSurfaceRenderTarget(IDXGISurface,const D2D1_RENDER_TARGET_PROPERTIES,ID2D1RenderTarget)
author: windows-sdk-content
description: Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface.
old-location: direct2d\ID2D1Factory_CreateDxgiSurfaceRenderTarget_ptr_IDXGISurface_ptr_D2D1_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1RenderTarget.htm
tech.root: Direct2D
ms.assetid: 1f24dd5e-271d-4780-b337-a9ab57f1d8f4
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CreateDxgiSurfaceRenderTarget, CreateDxgiSurfaceRenderTarget method [Direct2D], CreateDxgiSurfaceRenderTarget method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateDxgiSurfaceRenderTarget method, ID2D1Factory.CreateDxgiSurfaceRenderTarget, ID2D1Factory.CreateDxgiSurfaceRenderTarget(IDXGISurface,const D2D1_RENDER_TARGET_PROPERTIES,ID2D1RenderTarget), ID2D1Factory::CreateDxgiSurfaceRenderTarget, ID2D1Factory::CreateDxgiSurfaceRenderTarget(IDXGISurface,const D2D1_RENDER_TARGET_PROPERTIES,ID2D1RenderTarget), d2d1/ID2D1Factory::CreateDxgiSurfaceRenderTarget, direct2d.ID2D1Factory_CreateDxgiSurfaceRenderTarget_ptr_IDXGISurface_ptr_D2D1_RENDER_TARGET_PROPERTIES_ptr_ptr_ID2D1RenderTarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Factory.CreateDxgiSurfaceRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateDxgiSurfaceRenderTarget(IDXGISurface,const D2D1_RENDER_TARGET_PROPERTIES,ID2D1RenderTarget)


## -description


Creates a render target that draws to a DirectX Graphics Infrastructure (DXGI) surface. 


## -parameters




### -param dxgiSurface [in]

Type: <b><a href="http://msdn.microsoft.com/en-us/library/bb174565(VS.85).aspx">IDXGISurface</a>*</b>

The IDXGISurface to which the render target will draw. 


### -param renderTargetProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>*</b>

The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering. For information about supported pixel formats, see  <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel  Formats and Alpha Modes</a>.


### -param renderTarget [out]

Type: <b><a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>**</b>

When this method returns, contains the address of the pointer to the <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a> object created by this method.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To write to a Direct3D surface, you obtain an <a href="http://msdn.microsoft.com/en-us/library/bb174565(VS.85).aspx">IDXGISurface</a> and pass it to the <a href="https://msdn.microsoft.com/101744ea-97bc-4f92-88b0-fcdf0e4aaf4e">CreateDxgiSurfaceRenderTarget</a> method to create a DXGI surface render target; you can then use the DXGI surface render target to draw 2-D content to the DXGI surface.  

A DXGI surface render target is a type of <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>. Like other Direct2D render targets, you can use it to create resources and issue drawing commands. 

The DXGI surface render target and the DXGI surface must use the same DXGI format. If you specify the <a href="http://msdn.microsoft.com/en-us/library/bb173059(VS.85).aspx">DXGI_FORMAT_UNKOWN</a> format when you create the render target, it will automatically use the surface's format.

The DXGI surface render target does not perform DXGI surface synchronization. 

To work with Direct2D, the Direct3D device that provides the <a href="http://msdn.microsoft.com/en-us/library/bb174565(VS.85).aspx">IDXGISurface</a> must be created with the <b>D3D10_CREATE_DEVICE_BGRA_SUPPORT</b> flag.

For more information about creating and using DXGI surface render targets, see the <a href="https://msdn.microsoft.com/27680714-dc68-44eb-ab16-2cae3529b352">Direct2D and Direct3D Interoperability Overview</a>.

When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU. By creating a render target once and retaining it as long as possible, you gain performance benefits. Your application should create render targets once and hold onto them for the life of the application or until the render target's <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> method returns the <a href="https://msdn.microsoft.com/018bfca5-6ef4-497c-a4b6-8502c3cdac1b">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created). 




#### Examples

The following example obtains a  DXGI surface  (<i>pBackBuffer</i>) from an <a href="http://msdn.microsoft.com/en-us/library/bb174569(VS.85).aspx">IDXGISwapChain</a> and uses it to create a DXGI surface render target.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Get a surface in the swap chain
hr = m_pSwapChain-&gt;GetBuffer(
    0,
    IID_PPV_ARGS(&amp;pBackBuffer)
    );
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    if (SUCCEEDED(hr))
    {
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>        // Create the DXGI Surface Render Target.
        FLOAT dpiX;
        FLOAT dpiY;
        m_pD2DFactory-&gt;GetDesktopDpi(&amp;dpiX, &amp;dpiY);

        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                dpiX,
                dpiY
                );

        // Create a Direct2D render target which can draw into the surface in the swap chain
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>        hr = m_pD2DFactory-&gt;CreateDxgiSurfaceRenderTarget(
            pBackBuffer,
            &amp;props,
            &amp;m_pBackBufferRT
            );

    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/27680714-dc68-44eb-ab16-2cae3529b352">Direct2D and Direct3D Interoperability Overview</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

