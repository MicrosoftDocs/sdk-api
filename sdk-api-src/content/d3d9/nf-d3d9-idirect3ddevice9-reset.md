---
UID: NF:d3d9.IDirect3DDevice9.Reset
title: IDirect3DDevice9::Reset method
author: windows-driver-content
description: Resets the type, size, and format of the swap chain.
old-location: direct3d9\idirect3ddevice9__reset.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__reset.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IDirect3DDevice9, IDirect3DDevice9 interface [Direct3D 9], Reset method, IDirect3DDevice9::Reset, Reset method [Direct3D 9], Reset method [Direct3D 9], IDirect3DDevice9 interface, Reset,IDirect3DDevice9.Reset, b7f53ca7-1a26-5bf8-890b-5a4f26b3c249, d3d9helper/IDirect3DDevice9::Reset, direct3d9.idirect3ddevice9__reset
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
-	IDirect3DDevice9.Reset
product: Windows
targetos: Windows
req.lib: D3D9.lib
req.dll: 
req.irql: 
---

# IDirect3DDevice9::Reset method


## -description


Resets the type, size, and format of the swap chain.


## -parameters




### -param pPresentationParameters [in, out]

Type: <b><a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structure, describing the new presentation parameters. This value cannot be <b>NULL</b>. 
    


When switching to full-screen mode, Direct3D will try to find a desktop format that matches the back buffer format, so that back buffer and front buffer formats will be identical (to eliminate the need for color conversion).

When this method returns:

<ul>
<li>BackBufferCount, BackBufferWidth, and BackBufferHeight are set to zero.</li>
<li>BackBufferFormat is set to <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_UNKNOWN</a> for windowed mode only; a full-screen mode must specify a format.</li>
</ul>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Possible return values include: D3D_OK, D3DERR_DEVICELOST, D3DERR_DEVICEREMOVED, D3DERR_DRIVERINTERNALERROR, or D3DERR_OUTOFVIDEOMEMORY (see <a href="https://msdn.microsoft.com/4a9daa05-74f3-4173-b63d-53767feea7e2">D3DERR</a>).




## -remarks



If a call to <b>IDirect3DDevice9::Reset</b> fails, the device will be placed in the "lost" state (as indicated by a return value of D3DERR_DEVICELOST from a call to <a href="https://msdn.microsoft.com/da2ac8dd-0df8-4661-995f-9c3e6ccb62d2">IDirect3DDevice9::TestCooperativeLevel</a>) unless it is already in the "not reset" state (as indicated by a return value of D3DERR_DEVICENOTRESET from a call to <b>IDirect3DDevice9::TestCooperativeLevel</b>). Refer to <b>IDirect3DDevice9::TestCooperativeLevel</b> and <a href="https://msdn.microsoft.com/dc4326ba-2ebc-4bca-8fba-02d8db739b8f">Lost Devices (Direct3D 9)</a> for further information concerning the use of <b>IDirect3DDevice9::Reset</b> in the context of lost devices.

Calling <b>IDirect3DDevice9::Reset</b> causes all texture memory surfaces to be lost, managed textures to be flushed from video memory, and all state information to be lost. Before calling the <b>IDirect3DDevice9::Reset</b> method for a device, an application should release any explicit render targets, depth stencil surfaces, additional swap chains, state blocks, and D3DPOOL_DEFAULT resources associated with the device.

There are two different types of swap chains: full-screen or windowed. If the new swap chain is full-screen, the adapter will be placed in the display mode that matches the new size.

Direct3D 9 applications can expect messages to be sent to them during this call (for example, before this call is returned); applications should take precautions not to call into Direct3D at this time. In addition, when <b>IDirect3DDevice9::Reset</b> fails, the only valid methods that can be called are <b>IDirect3DDevice9::Reset</b>, <a href="https://msdn.microsoft.com/da2ac8dd-0df8-4661-995f-9c3e6ccb62d2">IDirect3DDevice9::TestCooperativeLevel</a>, and the various Release member functions. Calling any other method can result in an exception.

A call to <b>IDirect3DDevice9::Reset</b> will fail if called on a different thread than that used to create the device being reset.

Pixel shaders and vertex shaders survive <b>IDirect3DDevice9::Reset</b> calls for Direct3D 9. They do not need to be re-created explicitly by the application.


<a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFMT_UNKNOWN</a> can be specified for the windowed mode back buffer format when calling <a href="https://msdn.microsoft.com/22ad1d16-c1cc-4591-8311-daf6cf9924bb">IDirect3D9::CreateDevice</a>, <b>IDirect3DDevice9::Reset</b>, and <a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">IDirect3DDevice9::CreateAdditionalSwapChain</a>. This means the application does not have to query the current desktop format before calling <b>IDirect3D9::CreateDevice</b> for windowed mode. For full-screen mode, the back buffer format must be specified. Setting BackBufferCount equal to zero  (BackBufferCount = 0) results in one back buffer.

When trying to reset more than one display adapter in a group, set pPresentationParameters to point to an array of <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structures, one for each display in the adapter group.

If a multihead device was created with <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE_ADAPTERGROUP_DEVICE</a>, <b>IDirect3DDevice9::Reset</b> requires an array of <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structures wherein each structure must specify a full-screen display. To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.




## -see-also




<a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>



<a href="https://msdn.microsoft.com/522a5f71-3ad9-4cfc-a899-e25b9b721b1b">D3DSWAPEFFECT</a>



<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/47e67956-7ab4-4e05-bf05-685bdc094cf2">IDirect3DDevice9::Present</a>



<a href="https://msdn.microsoft.com/f741cdb4-2eb6-42e9-81ea-a8c677e07582">Multihead (Direct3D 9)</a>
 

 

