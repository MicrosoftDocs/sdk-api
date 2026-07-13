---
UID: NF:d3d9.IDirect3DSwapChain9.Present
title: IDirect3DSwapChain9::Present (d3d9.h)
description: The IDirect3DSwapChain9::Present (d3d9.h) method presents the contents of the next buffer in the sequence of back buffers owned by the swap chain.
helpviewer_keywords: ["0765aea9-8fd8-8d38-bcaf-184610e8d81e","IDirect3DSwapChain9 interface [Direct3D 9]","Present method","IDirect3DSwapChain9.Present","IDirect3DSwapChain9::Present","Present","Present method [Direct3D 9]","Present method [Direct3D 9]","IDirect3DSwapChain9 interface","d3d9helper/IDirect3DSwapChain9::Present","direct3d9.idirect3dswapchain9__present"]
old-location: direct3d9\idirect3dswapchain9__present.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9__present.htm
ms.date: 08/11/2022
ms.keywords: 0765aea9-8fd8-8d38-bcaf-184610e8d81e, IDirect3DSwapChain9 interface [Direct3D 9],Present method, IDirect3DSwapChain9.Present, IDirect3DSwapChain9::Present, Present, Present method [Direct3D 9], Present method [Direct3D 9],IDirect3DSwapChain9 interface, d3d9helper/IDirect3DSwapChain9::Present, direct3d9.idirect3dswapchain9__present
req.header: d3d9.h
req.include-header: D3D9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DSwapChain9::Present
 - d3d9/IDirect3DSwapChain9::Present
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DSwapChain9.Present
---

# IDirect3DSwapChain9::Present


## -description

Presents the contents of the next buffer in the sequence of back buffers owned by the swap chain.

## -parameters

### -param pSourceRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to the source rectangle (see <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>). Use <b>NULL</b> to present the entire surface. This value must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. If the rectangle exceeds the source surface, the rectangle is clipped to the source surface.

### -param pDestRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to the destination rectangle in client coordinates (see <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>). This value must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. Use <b>NULL</b> to fill the entire client area. If the rectangle exceeds the destination client area, the rectangle is clipped to the destination client area.

### -param hDestWindowOverride [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Destination window whose client area is taken as the target for this presentation. If this value is <b>NULL</b>, the runtime uses the <b>hDeviceWindow</b> member of <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> for the presentation.

### -param pDirtyRegion [in]

Type: <b>const <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a>*</b>

This value must be <b>NULL</b> unless the swap chain was created with <a href="/windows/desktop/direct3d9/d3dswapeffect">D3DSWAPEFFECT_COPY</a>. See <a href="/windows/desktop/direct3d9/flipping-surfaces">Flipping Surfaces (Direct3D 9)</a>.
    
 If this value is non-<b>NULL</b>, the contained region is expressed in back buffer coordinates. The rectangles within the region are the minimal set of pixels that need to be updated. This method takes these rectangles into account when optimizing the presentation by copying only the pixels within the region, or some suitably expanded set of rectangles. This is an aid to optimization only, and the application should not rely on the region being copied exactly. The implementation may choose to copy the whole source rectangle.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Allows the application to request that the method return immediately when the driver reports that it cannot schedule a presentation. Valid values are 0, or any combination of <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT_DONOTWAIT</a> or <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT_LINEAR_CONTENT</a>.
    


<ul>
<li>If dwFlags = 0, this method behaves as it did prior to Direct3D 9. Present will spin until the hardware is free, without returning an error.</li>
<li>If dwFlags = <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT_DONOTWAIT</a>, and the hardware is busy processing or waiting for a vertical sync interval, the method will return D3DERR_WASSTILLDRAWING.</li>
<li>If dwFlags = <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT_LINEAR_CONTENT</a>, gamma correction is performed from linear space to sRGB for windowed swap chains. This flag will take effect only when the driver exposes <a href="/windows/desktop/direct3d9/d3dcaps3">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</a> (see <a href="/windows/desktop/direct3d9/gamma">Gamma (Direct3D 9)</a>). Applications should specify this flag if the backbuffer format is 16-bit floating point in order to match windowed mode present to fullscreen gamma behavior.</li>
</ul>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_DEVICELOST, D3DERR_DRIVERINTERNALERROR, D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -remarks

The <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">Present</a> method is a shortcut to Present. Present has been updated to take a flag allowing the application to request that the method return immediately when the driver reports that it cannot schedule a presentation.

If necessary, a stretch operation is applied to transfer the pixels within the source rectangle to the destination rectangle in the client area of the target window.

Present will fail if called between <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-beginscene">BeginScene</a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene">EndScene</a> pairs unless the render target is not the current render target (such as the back buffer you get from creating an additional swap chain). This is a new behavior for Direct3D 9.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dswapchain9">IDirect3DSwapChain9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-reset">Reset</a>
