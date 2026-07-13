---
UID: NF:d3d9helper.IDirect3DDevice9.GetFrontBufferData
title: IDirect3DDevice9::GetFrontBufferData (d3d9helper.h)
description: The IDirect3DDevice9::GetFrontBufferData method (d3d9.h) generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application.
helpviewer_keywords: ["GetFrontBufferData","GetFrontBufferData method [Direct3D 9]","GetFrontBufferData method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetFrontBufferData method","IDirect3DDevice9.GetFrontBufferData","IDirect3DDevice9::GetFrontBufferData","b122af3c-c0ea-2cbb-1c39-139ab45eff11","d3d9helper/IDirect3DDevice9::GetFrontBufferData","direct3d9.idirect3ddevice9__getfrontbufferdata"]
old-location: direct3d9\idirect3ddevice9__getfrontbufferdata.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getfrontbufferdata.htm
ms.date: 08/11/2022
ms.keywords: GetFrontBufferData, GetFrontBufferData method [Direct3D 9], GetFrontBufferData method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetFrontBufferData method, IDirect3DDevice9.GetFrontBufferData, IDirect3DDevice9::GetFrontBufferData, b122af3c-c0ea-2cbb-1c39-139ab45eff11, d3d9helper/IDirect3DDevice9::GetFrontBufferData, direct3d9.idirect3ddevice9__getfrontbufferdata
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
 - IDirect3DDevice9::GetFrontBufferData
 - d3d9helper/IDirect3DDevice9::GetFrontBufferData
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
 - IDirect3DDevice9.GetFrontBufferData
---

# IDirect3DDevice9::GetFrontBufferData


## -description

Generates a copy of the device's front buffer and places that copy in a system memory buffer provided by the application.

## -parameters

### -param iSwapChain [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

An unsigned integer specifying the swap chain.

### -param pDestSurface [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a> interface that will receive a copy of the contents of the front buffer. The data is returned in successive rows with no intervening space, starting from the vertically highest row on the device's output to the lowest.



For windowed mode, the size of the destination surface should be the size of the desktop. For full-screen mode, the size of the destination surface should be the screen size.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_DRIVERINTERNALERROR, D3DERR_DEVICELOST, D3DERR_INVALIDCALL

## -remarks

The buffer pointed to by pDestSurface will be filled with a representation of the front buffer, converted to the standard 32 bits per pixel format D3DFMT_A8R8G8B8. 

This method is the only way to capture an antialiased screen shot.

This function is very slow, by design, and should not be used in any performance-critical path.

For more information, see <a href="/windows/desktop/direct3d9/lost-devices">Lost Devices and Retrieved Data</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
