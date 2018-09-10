---
UID: NF:d3d9.IDirect3DDevice9.SetRenderTarget
title: IDirect3DDevice9::SetRenderTarget
author: windows-sdk-content
description: Sets a new color buffer for the device.
old-location: direct3d9\idirect3ddevice9__setrendertarget.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setrendertarget.htm
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: 8a35c59a-95b2-ac1b-0fde-a907c6a0b520, IDirect3DDevice9 interface [Direct3D 9],SetRenderTarget method, IDirect3DDevice9.SetRenderTarget, IDirect3DDevice9::SetRenderTarget, SetRenderTarget, SetRenderTarget method [Direct3D 9], SetRenderTarget method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetRenderTarget, direct3d9.idirect3ddevice9__setrendertarget
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.SetRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9::SetRenderTarget


## -description


Sets a new color buffer for the device.


## -parameters




### -param RenderTargetIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Index of the render target. See Remarks.


### -param pRenderTarget [in]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>*</b>

Pointer to a new color buffer. If <b>NULL</b>, the color buffer for the corresponding RenderTargetIndex is disabled. Devices always must be associated with a color buffer.
 The new render-target surface must have at least D3DUSAGE_RENDERTARGET specified.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 This method will return D3DERR_INVALIDCALL if either:


<ul>
<li>pRenderTarget = <b>NULL</b> and RenderTargetIndex = 0</li>
<li>pRenderTarget is != <b>NULL</b> and the render target is invalid.</li>
</ul>



## -remarks



The device can support multiple render targets. The number of render targets supported by a device is contained in the NumSimultaneousRTs member of <a href="https://msdn.microsoft.com/44457b7b-a1f7-4019-b971-8ec2334d3313">D3DCAPS9</a>. See <a href="https://msdn.microsoft.com/ae48c5ce-b7f5-4189-8b04-880836be3fe0">Multiple Render Targets (Direct3D 9)</a>.

Setting a new render target will cause the viewport (see <a href="https://msdn.microsoft.com/eddadaa1-9181-47fa-8530-44aa46fea286">Viewports and Clipping (Direct3D 9)</a>) to be set to the full size of the new render target.

Some hardware tests the compatibility of the depth stencil buffer with the color buffer. If this is done, it is only done in a debug build.

Restrictions for using this method include the following:

<ul>
<li>The multisample type must be the same for the render target and the depth stencil surface.</li>
<li>The formats must be compatible for the render target and the depth stencil surface. See <a href="https://msdn.microsoft.com/f6c68511-7c5a-4b1b-b0b7-4102474f7dcd">IDirect3D9::CheckDepthStencilMatch</a>.</li>
<li>The size of the depth stencil surface must be greater than or equal to the size of the render target.</li>
</ul>
These restrictions are validated only when using the debug runtime when any of the <a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>Draw methods are called.

Cube textures differ from other surfaces in that they are collections of surfaces. To call <b>IDirect3DDevice9::SetRenderTarget</b> with a cube texture, you must select an individual face using <a href="https://msdn.microsoft.com/3ba6ad27-b8e8-400d-a3af-e69cdf53087a">IDirect3DCubeTexture9::GetCubeMapSurface</a> and pass the resulting surface to <b>IDirect3DDevice9::SetRenderTarget</b>.
    





## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>
 

 

