---
UID: NF:d3d9helper.IDirect3DDevice9.Present
title: IDirect3DDevice9::Present (d3d9helper.h)
description: The IDirect3DDevice9::Present method (d3d9.h) presents the contents of the next buffer in the sequence of back buffers owned by the device.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","Present method","IDirect3DDevice9.Present","IDirect3DDevice9::Present","Present","Present method [Direct3D 9]","Present method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::Present","dec6b9d2-0577-093b-3855-599ed58adc87","direct3d9.idirect3ddevice9__present"]
old-location: direct3d9\idirect3ddevice9__present.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__present.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],Present method, IDirect3DDevice9.Present, IDirect3DDevice9::Present, Present, Present method [Direct3D 9], Present method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::Present, dec6b9d2-0577-093b-3855-599ed58adc87, direct3d9.idirect3ddevice9__present
req.header: d3d9helper.h
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
 - IDirect3DDevice9::Present
 - d3d9helper/IDirect3DDevice9::Present
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
 - IDirect3DDevice9.Present
---

# IDirect3DDevice9::Present


## -description

Presents the contents of the next buffer in the sequence of back buffers owned by the device.

## -parameters

### -param pSourceRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a value that must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. pSourceRect is a pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the source rectangle. If <b>NULL</b>, the entire source surface is presented. If the rectangle exceeds the source surface, the rectangle is clipped to the source surface.

### -param pDestRect [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a value that must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. pDestRect is a pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the destination rectangle, in window client coordinates. If <b>NULL</b>, the entire client area is filled. If the rectangle exceeds the destination client area, the rectangle is clipped to the destination client area.

### -param hDestWindowOverride [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Pointer to a destination window whose client area is taken as the target for this presentation. If this value is <b>NULL</b>, the runtime uses the <b>hDeviceWindow</b> member of <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> for the presentation.

### -param pDirtyRegion [in]

Type: <b>const <a href="/windows/desktop/api/wingdi/ns-wingdi-rgndata">RGNDATA</a>*</b>

Value must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. For more information about swap chains, see <a href="/windows/desktop/direct3d9/flipping-surfaces">Flipping Surfaces (Direct3D 9)</a> and <a href="/windows/desktop/direct3d9/d3dswapeffect">D3DSWAPEFFECT</a>. If this value is non-<b>NULL</b>, the contained region is expressed in back buffer coordinates. The rectangles within the region are the minimal set of pixels that need to be updated. This method takes these rectangles into account when optimizing the presentation by copying only the pixels within the region, or some suitably expanded set of rectangles. This is an aid to optimization only, and the application should not rely on the region being copied exactly. The implementation can choose to copy the whole source rectangle.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: D3D_OK or D3DERR_DEVICEREMOVED (see <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a>).

## -remarks

If necessary, a stretch operation is applied to transfer the pixels within the source rectangle to the destination rectangle in the client area of the target window. 

<b>Present</b> will fail, returning D3DERR_INVALIDCALL, if called between BeginScene and EndScene pairs unless the render target is not the current render target (such as the back buffer you get from creating an additional swap chain). This is a new behavior for Direct3D 9.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/direct3d9/lost-devices">Lost Devices (Direct3D 9)</a>



<a href="/windows/desktop/direct3d9/multihead">Multihead (Direct3D 9)</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-reset">Reset</a>
