---
UID: NF:d3d9.IDirect3DDevice9Ex.ResetEx
title: IDirect3DDevice9Ex::ResetEx
author: windows-sdk-content
description: Resets the type, size, and format of the swap chain with all other surfaces persistent.
old-location: direct3d9\idirect3ddevice9ex_resetex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_resetex.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirect3DDevice9Ex interface [Direct3D 9],ResetEx method, IDirect3DDevice9Ex.ResetEx, IDirect3DDevice9Ex::ResetEx, ResetEx, ResetEx method [Direct3D 9], ResetEx method [Direct3D 9],IDirect3DDevice9Ex interface, a1ff1bc9-55df-22e8-e64e-5ba6de2759f4, d3d9/IDirect3DDevice9Ex::ResetEx, direct3d9.idirect3ddevice9ex_resetex
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
 - IDirect3DDevice9Ex.ResetEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirect3DDevice9Ex::ResetEx


## -description


Resets the type, size, and format of the swap chain with all other surfaces persistent.


## -parameters




### -param pPresentationParameters [in, out]

Type: <b><a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structure, describing the new presentation parameters. This value cannot be <b>NULL</b>. 
    


When switching to full-screen mode, Direct3D will try to find a desktop format that matches the back buffer format, so that back buffer and front buffer formats will be identical (to eliminate the need for color conversion).

When this method returns:

<ul>
<li>BackBufferCount, BackBufferWidth, and BackBufferHeight are set to zero.</li>
<li>BackBufferFormat is set to <a href="https://msdn.microsoft.com/a222e3bb-310c-4019-93ee-6a2da2a46ded">D3DFORMAT</a> for windowed mode only; a full-screen mode must specify a format.</li>
</ul>

### -param pFullscreenDisplayMode [in, out]

Type: <b><a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/df9d12b9-7acb-435b-9d54-0b095c871f0e">D3DDISPLAYMODEEX</a> structure that describes the properties of the desired display mode. This value must be provided for fullscreen applications, but can be <b>NULL</b> for windowed applications.
		


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

The method can return: D3D_OK, D3DERR_DEVICELOST or D3DERR_DEVICEHUNG (see <a href="https://msdn.microsoft.com/4a9daa05-74f3-4173-b63d-53767feea7e2">D3DERR</a>).



If this method returns D3DERR_DEVICELOST or D3DERR_DEVICEHUNG then the application can only call <b>IDirect3DDevice9Ex::ResetEx</b>, <a href="https://msdn.microsoft.com/89a9b112-5f0a-4e57-9b8e-48b3a76a09ce">IDirect3DDevice9Ex::CheckDeviceState</a> or release the interface pointer; any other API call will cause an exception.




## -remarks



If a call to <b>IDirect3DDevice9Ex::ResetEx</b> fails, the device will be placed in the lost state (as indicated by a return value of D3DERR_DEVICELOST from a call to <a href="https://msdn.microsoft.com/89a9b112-5f0a-4e57-9b8e-48b3a76a09ce">IDirect3DDevice9Ex::CheckDeviceState</a>). Refer to <b>IDirect3DDevice9Ex::CheckDeviceState</b> and <a href="https://msdn.microsoft.com/3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5">Lost Device Behavior Changes</a> for further information concerning the use of <b>IDirect3DDevice9Ex::ResetEx</b> in the context of lost devices.

Unlike previous versions of DirectX, calling <b>IDirect3DDevice9Ex::ResetEx</b> does not cause surfaces, textures or state information to be lost.

Pixel shaders and vertex shaders survive <b>IDirect3DDevice9Ex::ResetEx</b> calls for Direct3D 9. They do not need to be re-created explicitly by the application.

There are two different types of swap chains: full-screen or windowed. If the new swap chain is full-screen, the adapter will be placed in the display mode that matches the new size.

Applications can expect messages to be sent to them during this call (for example, before this call is returned); applications should take precautions not to call into Direct3D at this time.

A call to <b>IDirect3DDevice9Ex::ResetEx</b> will fail if called on a different thread than that used to create the device being reset.

D3DFMT_UNKNOWN can be specified for the windowed mode back buffer format when calling <a href="https://msdn.microsoft.com/7182c5ea-40ca-4cf8-a33e-b22984fc9349">IDirect3D9Ex::CreateDeviceEx</a>, <b>IDirect3DDevice9Ex::ResetEx</b>, and <a href="https://msdn.microsoft.com/d41b36f6-8481-47f8-bd38-8f51bc9ff9b8">IDirect3DDevice9::CreateAdditionalSwapChain</a>. This means the application does not have to query the current desktop format before calling <b>IDirect3D9Ex::CreateDeviceEx</b> for windowed mode. For full-screen mode, the back buffer format must be specified. Setting BackBufferCount equal to zero (BackBufferCount = 0) results in one back buffer.

When trying to reset more than one display adapter in a group, set pPresentationParameters to point to an array of <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structures, one for each display in the adapter group.

If a multihead device was created with <a href="https://msdn.microsoft.com/91387a2d-3927-4285-a09b-9ce247e6bfdd">D3DCREATE_ADAPTERGROUP_DEVICE</a>, <b>IDirect3DDevice9Ex::ResetEx</b> requires an array of <a href="https://msdn.microsoft.com/d677aeb7-a188-4ddc-b8c9-48e13676e9c8">D3DPRESENT_PARAMETERS</a> structures wherein each structure must specify a full-screen display. To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.




## -see-also




<a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>
 

 

