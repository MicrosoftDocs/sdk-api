---
UID: NF:d3d9helper.IDirect3DDevice9.GetDeviceCaps
title: IDirect3DDevice9::GetDeviceCaps (d3d9helper.h)
description: The IDirect3DDevice9::GetDeviceCaps method (d3d9.h) retrieves the capabilities of the rendering device.
helpviewer_keywords: ["1ca27ef9-f4c4-dcea-6966-4bbfcf987b8e","GetDeviceCaps","GetDeviceCaps method [Direct3D 9]","GetDeviceCaps method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetDeviceCaps method","IDirect3DDevice9.GetDeviceCaps","IDirect3DDevice9::GetDeviceCaps","d3d9helper/IDirect3DDevice9::GetDeviceCaps","direct3d9.idirect3ddevice9__getdevicecaps"]
old-location: direct3d9\idirect3ddevice9__getdevicecaps.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getdevicecaps.htm
ms.date: 08/11/2022
ms.keywords: 1ca27ef9-f4c4-dcea-6966-4bbfcf987b8e, GetDeviceCaps, GetDeviceCaps method [Direct3D 9], GetDeviceCaps method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetDeviceCaps method, IDirect3DDevice9.GetDeviceCaps, IDirect3DDevice9::GetDeviceCaps, d3d9helper/IDirect3DDevice9::GetDeviceCaps, direct3d9.idirect3ddevice9__getdevicecaps
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
 - IDirect3DDevice9::GetDeviceCaps
 - d3d9helper/IDirect3DDevice9::GetDeviceCaps
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
 - IDirect3DDevice9.GetDeviceCaps
---

# IDirect3DDevice9::GetDeviceCaps


## -description

Retrieves the capabilities of the rendering device.

## -parameters

### -param pCaps [out]

Type: <b><a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure, describing the returned device.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

<b>IDirect3DDevice9::GetDeviceCaps</b> retrieves the software vertex pipeline capabilities when the device is being used in software vertex processing mode.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
