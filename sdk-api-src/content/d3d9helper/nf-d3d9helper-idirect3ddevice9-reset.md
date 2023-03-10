---
UID: NF:d3d9helper.IDirect3DDevice9.Reset
title: IDirect3DDevice9::Reset (d3d9helper.h)
description: The IDirect3DDevice9::Reset method (d3d9.h) resets the type, size, and format of the swap chain.
helpviewer_keywords: ["IDirect3DDevice9 interface [Direct3D 9]","Reset method","IDirect3DDevice9.Reset","IDirect3DDevice9::Reset","Reset","Reset method [Direct3D 9]","Reset method [Direct3D 9]","IDirect3DDevice9 interface","b7f53ca7-1a26-5bf8-890b-5a4f26b3c249","d3d9helper/IDirect3DDevice9::Reset","direct3d9.idirect3ddevice9__reset"]
old-location: direct3d9\idirect3ddevice9__reset.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__reset.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DDevice9 interface [Direct3D 9],Reset method, IDirect3DDevice9.Reset, IDirect3DDevice9::Reset, Reset, Reset method [Direct3D 9], Reset method [Direct3D 9],IDirect3DDevice9 interface, b7f53ca7-1a26-5bf8-890b-5a4f26b3c249, d3d9helper/IDirect3DDevice9::Reset, direct3d9.idirect3ddevice9__reset
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
 - IDirect3DDevice9::Reset
 - d3d9helper/IDirect3DDevice9::Reset
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
 - IDirect3DDevice9.Reset
---

# IDirect3DDevice9::Reset


## -description

Resets the type, size, and format of the swap chain.

## -parameters

### -param pPresentationParameters [in, out]

Type: <b><a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structure, describing the new presentation parameters. This value cannot be <b>NULL</b>. 
    


When switching to full-screen mode, Direct3D will try to find a desktop format that matches the back buffer format, so that back buffer and front buffer formats will be identical (to eliminate the need for color conversion).

When this method returns:

<ul>
<li>BackBufferCount, BackBufferWidth, and BackBufferHeight are set to zero.</li>
<li>BackBufferFormat is set to <a href="/windows/desktop/direct3d9/d3dformat">D3DFMT_UNKNOWN</a> for windowed mode only; a full-screen mode must specify a format.</li>
</ul>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Possible return values include: D3D_OK, D3DERR_DEVICELOST, D3DERR_DEVICEREMOVED, D3DERR_DRIVERINTERNALERROR, or D3DERR_OUTOFVIDEOMEMORY (see <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a>).

## -remarks

If a call to <b>IDirect3DDevice9::Reset</b> fails, the device will be placed in the "lost" state (as indicated by a return value of D3DERR_DEVICELOST from a call to <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel">IDirect3DDevice9::TestCooperativeLevel</a>) unless it is already in the "not reset" state (as indicated by a return value of D3DERR_DEVICENOTRESET from a call to <b>IDirect3DDevice9::TestCooperativeLevel</b>). Refer to <b>IDirect3DDevice9::TestCooperativeLevel</b> and <a href="/windows/desktop/direct3d9/lost-devices">Lost Devices (Direct3D 9)</a> for further information concerning the use of <b>IDirect3DDevice9::Reset</b> in the context of lost devices.

Calling <b>IDirect3DDevice9::Reset</b> causes all texture memory surfaces to be lost, managed textures to be flushed from video memory, and all state information to be lost. Before calling the <b>IDirect3DDevice9::Reset</b> method for a device, an application should release any explicit render targets, depth stencil surfaces, additional swap chains, state blocks, and D3DPOOL_DEFAULT resources associated with the device.

There are two different types of swap chains: full-screen or windowed. If the new swap chain is full-screen, the adapter will be placed in the display mode that matches the new size.

Direct3D 9 applications can expect messages to be sent to them during this call (for example, before this call is returned); applications should take precautions not to call into Direct3D at this time. In addition, when <b>IDirect3DDevice9::Reset</b> fails, the only valid methods that can be called are <b>IDirect3DDevice9::Reset</b>, <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel">IDirect3DDevice9::TestCooperativeLevel</a>, and the various Release member functions. Calling any other method can result in an exception.

A call to <b>IDirect3DDevice9::Reset</b> will fail if called on a different thread than that used to create the device being reset.

Pixel shaders and vertex shaders survive <b>IDirect3DDevice9::Reset</b> calls for Direct3D 9. They do not need to be re-created explicitly by the application.


<a href="/windows/desktop/direct3d9/d3dformat">D3DFMT_UNKNOWN</a> can be specified for the windowed mode back buffer format when calling <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a>, <b>IDirect3DDevice9::Reset</b>, and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createadditionalswapchain">IDirect3DDevice9::CreateAdditionalSwapChain</a>. This means the application does not have to query the current desktop format before calling <b>IDirect3D9::CreateDevice</b> for windowed mode. For full-screen mode, the back buffer format must be specified. Setting BackBufferCount equal to zero  (BackBufferCount = 0) results in one back buffer.

When trying to reset more than one display adapter in a group, set pPresentationParameters to point to an array of <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structures, one for each display in the adapter group.

If a multihead device was created with <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE_ADAPTERGROUP_DEVICE</a>, <b>IDirect3DDevice9::Reset</b> requires an array of <a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a> structures wherein each structure must specify a full-screen display. To switch back to windowed mode, the application must destroy the device and re-create a non-multihead device in windowed mode.

## -see-also

<a href="/windows/desktop/direct3d9/d3dpresent-parameters">D3DPRESENT_PARAMETERS</a>



<a href="/windows/desktop/direct3d9/d3dswapeffect">D3DSWAPEFFECT</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-present">IDirect3DDevice9::Present</a>



<a href="/windows/desktop/direct3d9/multihead">Multihead (Direct3D 9)</a>
