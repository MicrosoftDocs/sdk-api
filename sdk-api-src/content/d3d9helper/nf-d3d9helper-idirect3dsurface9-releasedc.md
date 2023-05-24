---
UID: NF:d3d9helper.IDirect3DSurface9.ReleaseDC
title: IDirect3DSurface9::ReleaseDC (d3d9helper.h)
description: The IDirect3DSurface9::ReleaseDC method (d3d9helper.h) releases a device context handle.
helpviewer_keywords: ["IDirect3DSurface9 interface [Direct3D 9]","ReleaseDC method","IDirect3DSurface9.ReleaseDC","IDirect3DSurface9::ReleaseDC","ReleaseDC","ReleaseDC method [Direct3D 9]","ReleaseDC method [Direct3D 9]","IDirect3DSurface9 interface","c9032355-5437-491b-97b3-727d5c94fbfa","d3d9helper/IDirect3DSurface9::ReleaseDC","direct3d9.idirect3dsurface9__releasedc"]
old-location: direct3d9\idirect3dsurface9__releasedc.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3dsurface9__releasedc.htm
ms.date: 08/11/2022
ms.keywords: IDirect3DSurface9 interface [Direct3D 9],ReleaseDC method, IDirect3DSurface9.ReleaseDC, IDirect3DSurface9::ReleaseDC, ReleaseDC, ReleaseDC method [Direct3D 9], ReleaseDC method [Direct3D 9],IDirect3DSurface9 interface, c9032355-5437-491b-97b3-727d5c94fbfa, d3d9helper/IDirect3DSurface9::ReleaseDC, direct3d9.idirect3dsurface9__releasedc
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
 - IDirect3DSurface9::ReleaseDC
 - d3d9helper/IDirect3DSurface9::ReleaseDC
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
 - IDirect3DSurface9.ReleaseDC
---

# IDirect3DSurface9::ReleaseDC


## -description

Release a device context handle.

## -parameters

### -param hdc [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

Handle to a device context.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if the argument is invalid.

## -remarks

An hdc is a Windows resource. It must be released after use so Windows can return it to the pool of available resources.

This method will release only the device context returned by <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc">IDirect3DSurface9::GetDC</a>. Otherwise, this method will fail.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dsurface9">IDirect3DSurface9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc">IDirect3DSurface9::GetDC</a>
