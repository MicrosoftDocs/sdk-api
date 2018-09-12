---
UID: NF:d3d9helper.IDirect3DSwapChain9.Present
title: IDirect3DSwapChain9::Present
author: windows-sdk-content
description: Presents the contents of the next buffer in the sequence of back buffers owned by the swap chain.
old-location: direct3d9\idirect3dswapchain9__present.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dswapchain9__present.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 0765aea9-8fd8-8d38-bcaf-184610e8d81e, IDirect3DSwapChain9 interface [Direct3D 9],Present method, IDirect3DSwapChain9.Present, IDirect3DSwapChain9::Present, Present, Present method [Direct3D 9], Present method [Direct3D 9],IDirect3DSwapChain9 interface, d3d9helper/IDirect3DSwapChain9::Present, direct3d9.idirect3dswapchain9__present
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DSwapChain9::Present


## -description


Presents the contents of the next buffer in the sequence of back buffers owned by the swap chain.


## -parameters




### -param pSourceRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to the source rectangle (see <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>). Use <b>NULL</b> to present the entire surface. This value must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. If the rectangle exceeds the source surface, the rectangle is clipped to the source surface. 


### -param pDestRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to the destination rectangle in client coordinates (see <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>). This value must be <b>NULL</b> unless the swap chain was created with D3DSWAPEFFECT_COPY. Use <b>NULL</b> to fill the entire client area. If the rectangle exceeds the destination client area, the rectangle is clipped to the destination client area. 


### -param hDestWindowOverride [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Destination window whose client area is taken as the target for this presentation. If this value is <b>NULL</b>, the runtime uses the <b>hDeviceWindow</b> member of <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> for the presentation. 


### -param pDirtyRegion [in]

Type: <b>const <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a>*</b>

This value must be <b>NULL</b> unless the swap chain was created with <a href="https://msdn.microsoft.com/522a5f71-3ad9-4cfc-a899-e25b9b721b1b">D3DSWAPEFFECT_COPY</a>. See <a href="https://msdn.microsoft.com/4ca9a845-f433-4d4a-939e-4b9ab2983927">Flipping Surfaces (Direct3D 9)</a>.
    
 If this value is non-<b>NULL</b>, the contained region is expressed in back buffer coordinates. The rectangles within the region are the minimal set of pixels that need to be updated. This method takes these rectangles into account when optimizing the presentation by copying only the pixels within the region, or some suitably expanded set of rectangles. This is an aid to optimization only, and the application should not rely on the region being copied exactly. The implementation may choose to copy the whole source rectangle.


### -param dwFlags [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Allows the application to request that the method return immediately when the driver reports that it cannot schedule a presentation. Valid values are 0, or any combination of <a href="d3dpresent.htm">D3DPRESENT_DONOTWAIT</a> or <a href="d3dpresent.htm">D3DPRESENT_LINEAR_CONTENT</a>.
    


<ul>
<li>If dwFlags = 0, this method behaves as it did prior to Direct3D 9. Present will spin until the hardware is free, without returning an error.</li>
<li>If dwFlags = <a href="d3dpresent.htm">D3DPRESENT_DONOTWAIT</a>, and the hardware is busy processing or waiting for a vertical sync interval, the method will return D3DERR_WASSTILLDRAWING.</li>
<li>If dwFlags = <a href="d3dpresent.htm">D3DPRESENT_LINEAR_CONTENT</a>, gamma correction is performed from linear space to sRGB for windowed swap chains. This flag will take effect only when the driver exposes <a href="https://msdn.microsoft.com/d9cd7388-3413-472d-aacb-0b8c9c60031a">D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</a> (see <a href="https://msdn.microsoft.com/d076140d-3e91-412a-b099-9baa52f8d7d8">Gamma (Direct3D 9)</a>). Appliations should specify this flag if the backbuffer format is 16-bit floating point in order to match windowed mode present to fullscreen gamma behavior.</li>
</ul>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_DEVICELOST, D3DERR_DRIVERINTERNALERROR, D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -remarks



The <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">Present</a> method is a shortcut to Present. Present has been updated to take a flag allowing the application to request that the method return immediately when the driver reports that it cannot schedule a presentation.

If necessary, a stretch operation is applied to transfer the pixels within the source rectangle to the destination rectangle in the client area of the target window.

Present will fail if called between <a href="https://msdn.microsoft.com/7fc1375d-b2de-4762-9963-8428938e499f">BeginScene</a> and <a href="https://msdn.microsoft.com/9ff1e40e-9e19-4168-ae29-6f7d204ab236">EndScene</a> pairs unless the render target is not the current render target (such as the back buffer you get from creating an additional swap chain). This is a new behavior for Direct3D 9.




## -see-also




<a href="https://msdn.microsoft.com/df3fe9a0-cef9-4416-9287-4a1dd98b264d">IDirect3DSwapChain9</a>



<a href="https://msdn.microsoft.com/6d672f22-9843-4ff7-ae79-4903f56cd1e9">Reset</a>
 

 

