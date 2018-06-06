---
UID: NF:d3d9helper.IDirect3DDevice9.CreateDepthStencilSurface
title: IDirect3DDevice9::CreateDepthStencilSurface
author: windows-sdk-content
description: Creates a depth-stencil resource.
old-location: direct3d9\idirect3ddevice9__createdepthstencilsurface.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createdepthstencilsurface.htm
ms.author: windowssdkdev
ms.date: 04/10/2018
ms.keywords: 16f106bf-8b42-ad75-370e-e0ecffdfcea5, CreateDepthStencilSurface, CreateDepthStencilSurface method [Direct3D 9], CreateDepthStencilSurface method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateDepthStencilSurface method, IDirect3DDevice9.CreateDepthStencilSurface, IDirect3DDevice9::CreateDepthStencilSurface, d3d9helper/IDirect3DDevice9::CreateDepthStencilSurface, direct3d9.idirect3ddevice9__createdepthstencilsurface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3DVSHADERCAPS2_0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9.CreateDepthStencilSurface
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::CreateDepthStencilSurface


## -description


Creates a depth-stencil resource.


## -parameters




### -param Width [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the depth-stencil surface, in pixels. 


### -param Height [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the depth-stencil surface, in pixels. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the format of the depth-stencil surface. This value must be one of the enumerated depth-stencil formats for this device.


### -param MultiSample [in]

Type: <b><a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a> enumerated type, describing the multisampling buffer type. This value must be one of the allowed multisample types. When this surface is passed to <a href="https://msdn.microsoft.com/e0ffb4fc-6428-44b1-9f9d-88a5fa88d712">IDirect3DDevice9::SetDepthStencilSurface</a>, its multisample type must be the same as that of the render target set by <a href="https://msdn.microsoft.com/e194af98-492a-4650-acca-68ebe0cd759c">IDirect3DDevice9::SetRenderTarget</a>.


### -param MultisampleQuality [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Quality level. The valid range is between zero and one less than the level returned by pQualityLevels used by  <a href="https://msdn.microsoft.com/82f1f1f6-0d9b-497b-b532-0d2aabbd0314">IDirect3D9::CheckDeviceMultiSampleType</a>. Passing a larger value returns the error D3DERR_INVALIDCALL. The MultisampleQuality values of paired render targets, depth stencil surfaces, and the MultiSample type must all match.


### -param Discard [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Set this flag to <b>TRUE</b> to enable z-buffer discarding, and <b>FALSE</b> otherwise.				
If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">IDirect3DDevice9::Present</a> or <a href="https://msdn.microsoft.com/e0ffb4fc-6428-44b1-9f9d-88a5fa88d712">IDirect3DDevice9::SetDepthStencilSurface</a> with a different depth surface.

This flag has the same behavior as the constant,  D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL, in <a href="https://msdn.microsoft.com/1294171e-b3f6-4264-8411-b69427cefe7b">D3DPRESENTFLAG</a>.


### -param ppSurface [out, retval]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface, representing the created depth-stencil surface resource. 


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">share resources</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_NOTAVAILABLE, D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -remarks



The memory class of the depth-stencil buffer is always D3DPOOL_DEFAULT.




## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/303a4224-9c5d-4fc6-a7c5-168f18166e3c">IDirect3DDevice9::UpdateSurface</a>
 

 

