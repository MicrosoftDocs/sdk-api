---
UID: NF:d3d9.IDirect3DDevice9.GetTransform
title: IDirect3DDevice9::GetTransform (d3d9.h)
description: The IDirect3DDevice9::GetTransform method (d3d9.h) retrieves a matrix describing a transformation state.
helpviewer_keywords: ["GetTransform","GetTransform method [Direct3D 9]","GetTransform method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetTransform method","IDirect3DDevice9.GetTransform","IDirect3DDevice9::GetTransform","a6b5ae1d-9cec-460e-5acb-c2e1bd7566e6","d3d9helper/IDirect3DDevice9::GetTransform","direct3d9.idirect3ddevice9__gettransform"]
old-location: direct3d9\idirect3ddevice9__gettransform.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__gettransform.htm
ms.date: 08/11/2022
ms.keywords: GetTransform, GetTransform method [Direct3D 9], GetTransform method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetTransform method, IDirect3DDevice9.GetTransform, IDirect3DDevice9::GetTransform, a6b5ae1d-9cec-460e-5acb-c2e1bd7566e6, d3d9helper/IDirect3DDevice9::GetTransform, direct3d9.idirect3ddevice9__gettransform
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirect3DDevice9::GetTransform
 - d3d9/IDirect3DDevice9::GetTransform
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
 - IDirect3DDevice9.GetTransform
---

# IDirect3DDevice9::GetTransform


## -description

Retrieves a matrix describing a transformation state.

## -parameters

### -param State [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dtransformstatetype">D3DTRANSFORMSTATETYPE</a></b>

Device state variable that is being modified. This parameter can be any member of the <a href="/windows/desktop/direct3d9/d3dtransformstatetype">D3DTRANSFORMSTATETYPE</a> enumerated type, or the <a href="/windows/desktop/direct3d9/d3dts-worldmatrix">D3DTS_WORLDMATRIX</a> macro.

### -param pMatrix [out]

Type: <b><a href="/windows/desktop/direct3d9/d3dmatrix">D3DMATRIX</a>*</b>

Pointer to a 
    <a href="/windows/desktop/direct3d9/d3dmatrix">D3DMATRIX</a> structure, describing the returned transformation state.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL if one of the arguments is invalid.

## -remarks

This method will not return device state for a device that is created using D3DCREATE_PUREDEVICE. If you want to use this method, you must create your device with any of the other flag values in <a href="/windows/desktop/direct3d9/d3dcreate">D3DCREATE</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform">IDirect3DDevice9::SetTransform</a>
