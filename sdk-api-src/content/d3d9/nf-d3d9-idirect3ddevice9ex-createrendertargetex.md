---
UID: NF:d3d9.IDirect3DDevice9Ex.CreateRenderTargetEx
title: IDirect3DDevice9Ex::CreateRenderTargetEx method
author: windows-driver-content
description: Creates a render-target surface.
old-location: direct3d9\idirect3ddevice9ex_createrendertargetex.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_createrendertargetex.htm
ms.author: windowsdriverdev
ms.date: 4/10/2018
ms.keywords: 78a5ebad-c705-e895-65b2-37612b0e204e, CreateRenderTargetEx method [Direct3D 9], CreateRenderTargetEx method [Direct3D 9], IDirect3DDevice9Ex interface, CreateRenderTargetEx,IDirect3DDevice9Ex.CreateRenderTargetEx, IDirect3DDevice9Ex, IDirect3DDevice9Ex interface [Direct3D 9], CreateRenderTargetEx method, IDirect3DDevice9Ex::CreateRenderTargetEx, d3d9/IDirect3DDevice9Ex::CreateRenderTargetEx, direct3d9.idirect3ddevice9ex_createrendertargetex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: D3D12_SIGNATURE_PARAMETER_DESC
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D9.lib
-	D3D9.dll
api_name:
-	IDirect3DDevice9Ex.CreateRenderTargetEx
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9Ex::CreateRenderTargetEx method


## -description


Creates a render-target surface.


## -parameters




### -param Width [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Width of the render-target surface, in pixels. 


### -param Height [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Height of the render-target surface, in pixels. 


### -param Format [in]

Type: <b><a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a></b>

Member of the <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> enumerated type, describing the format of the render target. 


### -param MultiSample [in]

Type: <b><a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a></b>

Member of the <a href="https://msdn.microsoft.com/1a3c1efe-f5b1-47a1-a5f5-ac49d318f3b8">D3DMULTISAMPLE_TYPE</a> enumerated type, which describes the multisampling buffer type. This parameter specifies the antialiasing type for this render target. When this surface is passed to <a href="https://msdn.microsoft.com/e194af98-492a-4650-acca-68ebe0cd759c">IDirect3DDevice9::SetRenderTarget</a>, its multisample type must be the same as that of the depth-stencil set by <a href="https://msdn.microsoft.com/e0ffb4fc-6428-44b1-9f9d-88a5fa88d712">IDirect3DDevice9::SetDepthStencilSurface</a>. 


### -param MultisampleQuality [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Quality level. The valid range is between zero and one less than the level returned by pQualityLevels used by  <a href="https://msdn.microsoft.com/82f1f1f6-0d9b-497b-b532-0d2aabbd0314">IDirect3D9::CheckDeviceMultiSampleType</a>. Passing a larger value returns the error, D3DERR_INVALIDCALL. The MultisampleQuality values of paired render targets, depth stencil surfaces, and the multisample type must all match.


### -param Lockable [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Render targets are not lockable unless the application specifies <b>TRUE</b> for Lockable.

Note that lockable render targets reduce performance on some graphics hardware. The readback performance (moving data from video memory to system memory) depends on the type of hardware used (AGP vs. PCI Express) and is usually far lower than upload performance (moving data from system to video memory). If you need read access to render targets, use <a href="https://msdn.microsoft.com/9fc6121c-3da8-49d8-9bd6-c8654ce90100">GetRenderTargetData</a> instead of lockable render targets.


### -param ppSurface [out, retval]

Type: <b><a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/312eee39-6a5c-46b6-b145-78d5f0f9eecd">IDirect3DSurface9</a> interface. 


### -param pSharedHandle [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/hh973215">HANDLE</a>*</b>

Reserved. Set this parameter to <b>NULL</b>. This parameter can be used in Direct3D 9 for Windows Vista to <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">share resources</a>.


### -param Usage [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Combination of one or more <a href="https://msdn.microsoft.com/c8823c39-8f17-441c-a42b-de3d7ec02f75">D3DUSAGE</a> constants which can be OR'd together. Value of 0 indicates no usage.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_NOTAVAILABLE, D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.




## -remarks



Render-target surfaces are placed in the D3DPOOL_DEFAULT memory class.

The creation of lockable, multisampled render targets is not supported.




## -see-also




<a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>
 

 

