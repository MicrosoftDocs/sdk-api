---
UID: NF:d3d9.IDirect3DDevice9Ex.PresentEx
title: IDirect3DDevice9Ex::PresentEx (d3d9.h)
description: Swap the swapchain's next buffer with the front buffer.
helpviewer_keywords: ["8af2bbce-d370-576f-a879-e996430d3295","IDirect3DDevice9Ex interface [Direct3D 9]","PresentEx method","IDirect3DDevice9Ex.PresentEx","IDirect3DDevice9Ex::PresentEx","PresentEx","PresentEx method [Direct3D 9]","PresentEx method [Direct3D 9]","IDirect3DDevice9Ex interface","d3d9/IDirect3DDevice9Ex::PresentEx","direct3d9.idirect3ddevice9ex_presentex"]
old-location: direct3d9\idirect3ddevice9ex_presentex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_presentex.htm
ms.date: 12/05/2018
ms.keywords: 8af2bbce-d370-576f-a879-e996430d3295, IDirect3DDevice9Ex interface [Direct3D 9],PresentEx method, IDirect3DDevice9Ex.PresentEx, IDirect3DDevice9Ex::PresentEx, PresentEx, PresentEx method [Direct3D 9], PresentEx method [Direct3D 9],IDirect3DDevice9Ex interface, d3d9/IDirect3DDevice9Ex::PresentEx, direct3d9.idirect3ddevice9ex_presentex
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9Ex::PresentEx
 - d3d9/IDirect3DDevice9Ex::PresentEx
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
 - IDirect3DDevice9Ex.PresentEx
---

# IDirect3DDevice9Ex::PresentEx


## -description

Swap the swapchain's next buffer with the front buffer.

## -parameters

### -param pSourceRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure indicating region on the source surface to copy in window client coordinates. Only applies when the swapchain was created with the <a href="/windows/desktop/direct3d9/d3dswapeffect">D3DSWAPEFFECT_COPY</a> flag. If <b>NULL</b>, the entire source surface is presented. If the rectangle exceeds the source surface, it is clipped to the source surface.

### -param pDestRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure indicating the target region on the destination surface in window client coordinates. Only applies when the swapchain was created with the <a href="/windows/desktop/direct3d9/d3dswapeffect">D3DSWAPEFFECT_COPY</a> flag. If <b>NULL</b>, the entire client area is filled. If the rectangle exceeds the destination client area, it is clipped to the destination client area.

### -param hDestWindowOverride [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Pointer to a destination window whose client area is taken as the target for this presentation. If this value is <b>NULL</b>, the runtime uses the <b>hDeviceWindow</b> member of <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> for the presentation.

<div class="alert"><b>Note</b>  If you create a swap chain with D3DSWAPEFFECT_FLIPEX, you must pass <b>NULL</b> to <i>hDestWindowOverride</i></div>
<div> </div>

### -param pDirtyRegion [in]

Type: <b>const <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a>*</b>

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a> structure indicating the smallest set of pixels that need to be transferred. This value must be <b>NULL</b> unless the swapchain was created with the <a href="/windows/desktop/direct3d9/d3dswapeffect">D3DSWAPEFFECT_COPY</a> flag. For more information about swapchains, see <a href="/windows/desktop/direct3d9/flipping-surfaces">Flipping Surfaces (Direct3D 9)</a>.

If this value is non-<b>NULL</b>, the contained region is expressed in back buffer coordinates. The method takes these rectangles into account when optimizing the presentation by copying only the pixels within the region, or some suitably expanded set of rectangles. This is an aid to optimization only, and the application should not rely on the region being copied exactly. The implementation can choose to copy the whole source rectangle.

### -param dwFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Allows the application to request that the method return immediately when the driver reports that it cannot schedule a presentation. Valid values are 0, or any combination of <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT</a> flags.



<ul>
<li>If dwFlags = 0, this method behaves as it did prior to Direct3D 9. Present will spin until the hardware is free, without returning an error.</li>
<li>If dwFlags = <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT_DONOTFLIP</a> the display driver is called with the front buffer as both the source and target surface. The driver responds by scheduling a frame synch, but not changing the displayed surface. This flag is only available in full-screen mode or when using D3DSWAPEFFECT_FLIPEX in windowed mode.</li>
<li>If dwFlags = <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT_DONOTWAIT</a>, and the hardware is busy processing or waiting for a vertical sync interval, the method will return D3DERR_WASSTILLDRAWING.</li>
<li>If dwFlags = <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT_FORCEIMMEDIATE</a>, D3DPRESENT_INTERVAL_IMMEDIATE is enforced on this Present call. This flag can only be specified when using D3DSWAPEFFECT_FLIPEX. This behavior is the same for windowed and full-screen modes.</li>
<li>If dwFlags = <a href="/windows/desktop/direct3d9/d3dpresent">D3DPRESENT_LINEAR_CONTENT</a>, gamma correction is performed from linear space to sRGB for windowed swap chains. This flag will take effect only when the driver exposes <a href="/windows/desktop/direct3d9/d3dcaps3">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</a> (see <a href="/windows/desktop/direct3d9/gamma">Gamma (Direct3D 9)</a>).</li>
</ul>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: S_OK, D3DERR_DEVICELOST, D3DERR_DEVICEHUNG, D3DERR_DEVICEREMOVED, or D3DERR_OUTOFVIDEOMEMORY (see <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a>) or S_PRESENT_OCCLUDED, or S_PRESENT_MODE_CHANGED (see <a href="/windows/win32/direct3d9/device-state-return-codes">S_PRESENT</a>). See <a href="/windows/desktop/direct3d9/dx9lh">Lost Device Behavior Changes</a> for more information about lost, hung, and removed devices.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 9Ex:

<a href="/windows/desktop/direct3d9/d3dswapeffect">D3DSWAPEFFECT_FLIPEX</a> is only available in Direct3D9Ex running on Windows 7 (or more current operating system).

</td>
</tr>
</table>

## -remarks

Similar to the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">IDirect3DDevice9::Present</a> Method, PresentEx adds a dwflags parameter.

When the swapchain is created with <a href="/windows/desktop/direct3d9/d3dswapeffect">D3DSWAPEFFECT_FLIPEX</a> flag, <b>pSourceRect</b>, <b>pDestRect</b> and <b>pDirtyRegion</b> values must be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>
