---
UID: NF:d3d9helper.IDirect3DDevice9.GetDirect3D
title: IDirect3DDevice9::GetDirect3D (d3d9helper.h)
description: The IDirect3DDevice9::GetDirect3D method (d3d9.h) returns an interface to the instance of the Direct3D object that created the device.
helpviewer_keywords: ["81502735-fdf2-3d9f-7157-db6ecffe07a9","GetDirect3D","GetDirect3D method [Direct3D 9]","GetDirect3D method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetDirect3D method","IDirect3DDevice9.GetDirect3D","IDirect3DDevice9::GetDirect3D","d3d9helper/IDirect3DDevice9::GetDirect3D","direct3d9.idirect3ddevice9__getdirect3d"]
old-location: direct3d9\idirect3ddevice9__getdirect3d.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getdirect3d.htm
ms.date: 08/11/2022
ms.keywords: 81502735-fdf2-3d9f-7157-db6ecffe07a9, GetDirect3D, GetDirect3D method [Direct3D 9], GetDirect3D method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetDirect3D method, IDirect3DDevice9.GetDirect3D, IDirect3DDevice9::GetDirect3D, d3d9helper/IDirect3DDevice9::GetDirect3D, direct3d9.idirect3ddevice9__getdirect3d
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
 - IDirect3DDevice9::GetDirect3D
 - d3d9helper/IDirect3DDevice9::GetDirect3D
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
 - IDirect3DDevice9.GetDirect3D
---

# IDirect3DDevice9::GetDirect3D


## -description

Returns an interface to the instance of the Direct3D object that created the device.

## -parameters

### -param ppD3D9 [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a>**</b>

Address of a pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a> interface, representing the interface of the Direct3D object that created the device.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

Calling <b>IDirect3DDevice9::GetDirect3D</b> will increase the internal reference count on the <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3d9">IDirect3D9</a> interface. Failure to call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> when finished using this <b>IDirect3D9</b> interface results in a memory leak.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
