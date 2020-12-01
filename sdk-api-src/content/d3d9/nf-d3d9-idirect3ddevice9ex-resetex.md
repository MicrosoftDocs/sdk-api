---
UID: NF:d3d9.IDirect3DDevice9Ex.ResetEx
title: IDirect3DDevice9Ex::ResetEx (d3d9.h)
description: Resets the type, size, and format of the swap chain with all other surfaces persistent.
helpviewer_keywords: ["IDirect3DDevice9Ex interface [Direct3D 9]","ResetEx method","IDirect3DDevice9Ex.ResetEx","IDirect3DDevice9Ex::ResetEx","ResetEx","ResetEx method [Direct3D 9]","ResetEx method [Direct3D 9]","IDirect3DDevice9Ex interface","a1ff1bc9-55df-22e8-e64e-5ba6de2759f4","d3d9/IDirect3DDevice9Ex::ResetEx","direct3d9.idirect3ddevice9ex_resetex"]
old-location: direct3d9\idirect3ddevice9ex_resetex.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_resetex.htm
ms.date: 12/05/2018
ms.keywords: IDirect3DDevice9Ex interface [Direct3D 9],ResetEx method, IDirect3DDevice9Ex.ResetEx, IDirect3DDevice9Ex::ResetEx, ResetEx, ResetEx method [Direct3D 9], ResetEx method [Direct3D 9],IDirect3DDevice9Ex interface, a1ff1bc9-55df-22e8-e64e-5ba6de2759f4, d3d9/IDirect3DDevice9Ex::ResetEx, direct3d9.idirect3ddevice9ex_resetex
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
 - IDirect3DDevice9Ex::ResetEx
 - d3d9/IDirect3DDevice9Ex::ResetEx
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
 - IDirect3DDevice9Ex.ResetEx
---

# IDirect3DDevice9Ex::ResetEx


## -description

Resets the type, size, and format of the swap chain with all other surfaces persistent.

## -parameters

### -param pPresentationParameters [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structure, describing the new presentation parameters. This value cannot be <b>NULL</b>. 
    


When switching to full-screen mode, Direct3D will try to find a desktop format that matches the back buffer format, so that back buffer and front buffer formats will be identical (to eliminate the need for color conversion).

When this method returns:

<ul>
<li>BackBufferCount, BackBufferWidth, and BackBufferHeight are set to zero.</li>
<li>BackBufferFormat is set to <a href="/windows/desktop/direct3d9/d3dformat">D3DFORMAT</a> for windowed mode only; a full-screen mode must specify a format.</li>
</ul>

### -param pFullscreenDisplayMode [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3ddisplaymodeex">D3DDISPLAYMODEEX</a> structure that describes the properties of the desired display mode. This value must be provided for fullscreen applications, but can be <b>NULL</b> for windowed applications.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

The method can return: D3D_OK, D3DERR_DEVICELOST or D3DERR_DEVICEHUNG (see <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a>).



If this method returns D3DERR_DEVICELOST or D3DERR_DEVICEHUNG then the application can only call <b>IDirect3DDevice9Ex::ResetEx</b>, <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate">IDirect3DDevice9Ex::CheckDeviceState</a> or release the interface pointer; any other API call will cause an exception.

## -remarks

If a call to <b>IDirect3DDevice9Ex::ResetEx</b> fails, the device will be placed in the lost state (as indicated by a return value of D3DERR_DEVICELOST from a call to <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-checkdevicestate">IDirect3DDevice9Ex::CheckDeviceState</a>). Refer to <b>IDirect3DDevice9Ex::CheckDeviceState</b> and <a href="/windows/desktop/direct3d9/dx9lh">Lost Device Behavior Changes</a> for further information concerning the use of <b>IDirect3DDevice9Ex::ResetEx</b> in the context of lost devices.

Unlike previous versions of DirectX, calling <b>IDirect3DDevice9Ex::ResetEx</b> does not cause surfaces, textures or state information to be lost.

Pixel shaders and vertex shaders survive <b>IDirect3DDevice9Ex::ResetEx</b> calls for Direct3D 9. They do not need to be re-created explicitly by the application.

There are two different types of swap chains: full-screen or windowed. If the new swap chain is full-screen, the adapter will be placed in the display mode that matches the new size.

Applications can expect messages to be sent to them during this call (for example, before this call is returned); applications should take precautions not to call into Direct3D at this time.

A call to <b>IDirect3DDevice9Ex::ResetEx</b> will fail if called on a different thread than that used to create the device being reset.

D3DFMT_UNKNOWN can be specified for the windowed mode back buffer format when calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex">IDirect3D9Ex::CreateDeviceEx</a>, <b>IDirect3DDevice9Ex::ResetEx</b>, and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createadditionalswapchain">IDirect3DDevice9::CreateAdditionalSwapChain</a>. This means the application does not have to query the current desktop format before calling <b>IDirect3D9Ex::CreateDeviceEx</b> for windowed mode. For full-screen mode, the back buffer format must be specified. Setting BackBufferCount equal to zero (BackBufferCount = 0) results in one back buffer.

When trying to reset more than one display adapter in a group, set pPresentationParameters to point to an array of <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structures, one for each display in the adapter group.

If a multihead device was created with <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE_ADAPTERGROUP_DEVICE</a>, <b>IDirect3DDevice9Ex::ResetEx</b> requires an array of <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structures wherein each structure must specify a full-screen display. To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.

## -see-also

<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex">IDirect3DDevice9Ex</a>