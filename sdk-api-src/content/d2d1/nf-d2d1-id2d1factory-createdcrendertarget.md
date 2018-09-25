---
UID: NF:d2d1.ID2D1Factory.CreateDCRenderTarget
title: ID2D1Factory::CreateDCRenderTarget
author: windows-sdk-content
description: Creates a render target that draws to a Windows Graphics Device Interface (GDI) device context.
old-location: direct2d\ID2D1Factory_CreateDCRenderTarget.htm
tech.root: direct2d
ms.assetid: de062068-d2b5-4576-a475-a0e2c9840506
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: CreateDCRenderTarget, CreateDCRenderTarget method [Direct2D], CreateDCRenderTarget method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateDCRenderTarget method, ID2D1Factory.CreateDCRenderTarget, ID2D1Factory::CreateDCRenderTarget, d2d1/ID2D1Factory::CreateDCRenderTarget, direct2d.ID2D1Factory_CreateDCRenderTarget
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
 - ID2D1Factory.CreateDCRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateDCRenderTarget


## -description


Creates a render target that draws to a Windows Graphics Device Interface (GDI) device context.


## -parameters




### -param renderTargetProperties [in]

Type: <b>const <a href="https://msdn.microsoft.com/360900bd-1353-4a92-865c-ad34d5e98123">D2D1_RENDER_TARGET_PROPERTIES</a>*</b>

The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering.  To enable the device context (DC) render target to work with GDI, set the DXGI format to <a href="http://msdn.microsoft.com/en-us/library/bb173059(VS.85).aspx">DXGI_FORMAT_B8G8R8A8_UNORM</a> and the alpha mode to <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE_PREMULTIPLIED</a> or <b>D2D1_ALPHA_MODE_IGNORE</b>. For more information about pixel formats, see  <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel  Formats and Alpha Modes</a>.


### -param dcRenderTarget [out]

Type: <b><a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a>**</b>

When this method returns, <i>dcRenderTarget</i> contains the address of the pointer to the  <a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a> created by the method.


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before you can render with a DC render target, you must use the render target's <a href="https://msdn.microsoft.com/a5e98470-9a9f-4a85-b00f-afb2ead3fb31">BindDC</a> method to associate it with a GDI DC.  Do this for each different DC and whenever there is a change in the size of the area you want to draw to.

To enable the DC render target to work with GDI, set the render target's DXGI format to <a href="http://msdn.microsoft.com/en-us/library/bb173059(VS.85).aspx">DXGI_FORMAT_B8G8R8A8_UNORM</a> and alpha mode to <a href="https://msdn.microsoft.com/f1b1e735-2e89-4dc1-9fee-dfb4626ef453">D2D1_ALPHA_MODE_PREMULTIPLIED</a> or <b>D2D1_ALPHA_MODE_IGNORE</b>.

Your application should create render targets once and hold on to them for the life of the application or until the render target's  <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> method returns the <a href="https://msdn.microsoft.com/018bfca5-6ef4-497c-a4b6-8502c3cdac1b">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, recreate the render target (and any resources it created).


#### Examples

The following code creates a DC render target.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory-&gt;CreateDCRenderTarget(&amp;props, &amp;m_pDCRT);
</pre>
</td>
</tr>
</table></span></div>
In the preceding code, <i>m_pD2DFactory</i> is a  pointer to an <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>, and <i>m_pDCRT</i> is a pointer to an <a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a>. 

The next code example binds a DC to the <a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DemoApp::OnRender(const PAINTSTRUCT &amp;ps)
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
<pre>// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &amp;rc);
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Bind the DC to the DC render target.
hr = m_pDCRT-&gt;BindDC(ps.hdc, &amp;rc);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/182df2dc-2574-4d8f-a7e1-30d70da1740a">Direct2D and GDI Interoperation Overview</a>



<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>



<a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel  Formats and Alpha Modes</a>
 

 

