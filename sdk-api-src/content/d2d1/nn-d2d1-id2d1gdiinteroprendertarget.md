---
UID: NN:d2d1.ID2D1GdiInteropRenderTarget
title: ID2D1GdiInteropRenderTarget (d2d1.h)
author: windows-sdk-content
description: Provides access to an device context that can accept GDI drawing commands.
old-location: direct2d\ID2D1GdiInteropRenderTarget.htm
tech.root: Direct2D
ms.assetid: cb992ddd-21b2-4eba-b7c4-e391bdd23a9d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID2D1GdiInteropRenderTarget, ID2D1GdiInteropRenderTarget interface [Direct2D], ID2D1GdiInteropRenderTarget interface [Direct2D],described, d2d1/ID2D1GdiInteropRenderTarget, direct2d.ID2D1GdiInteropRenderTarget
ms.topic: interface
f1_keywords: ["d2d1/ID2D1GdiInteropRenderTarget"]
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - ID2D1GdiInteropRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1GdiInteropRenderTarget interface


## -description


Provides access to an device context that can accept GDI drawing commands.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GdiInteropRenderTarget</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1GdiInteropRenderTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GdiInteropRenderTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc">GetDC</a>
</td>
<td align="left" width="63%">
Retrieves the device context associated with this render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc">ReleaseDC</a>
</td>
<td align="left" width="63%">
Indicates that drawing with the device context retrieved using the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc">GetDC</a> method is finished. 

</td>
</tr>
</table> 


## -remarks



You don't create an <b>ID2D1GdiInteropRenderTarget</b> object directly; instead, you use the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of an existing render target instance to provide an <b>ID2D1GdiInteropRenderTarget</b> version of that render target. 

Not all render targets support the <b>ID2D1GdiInteropRenderTarget</b> interface. The render target must be GDI-compatible (the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage">D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE</a> flag was specified when creating the render target), use the <a href="https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a> pixel format, and use  the <a href="https://docs.microsoft.com/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_PREMULTIPLIED</a> or <b>D2D1_ALPHA_MODE_IGNORE</b>  alpha mode.

Note that the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method always succeeds; if the render target doesn't support the <b>ID2D1GdiInteropRenderTarget</b> interface, calling <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc">GetDC</a> will fail. (For render targets created through the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)">CreateCompatibleRenderTarget</a> method, the render target that created it must have these settings.) 

To test whether a given render target supports the <b>ID2D1GdiInteropRenderTarget</b> interface, create a <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES </a>that specifies GDI compatibility and the appropriate pixel format, then call the render target's <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties_)">IsSupported</a> method to see whether the render target is GDI-compatible. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-and-gdi-interoperation-overview">Direct2D and GDI Interoperability Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

