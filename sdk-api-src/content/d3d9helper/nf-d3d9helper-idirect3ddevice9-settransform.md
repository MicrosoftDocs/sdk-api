---
UID: NF:d3d9helper.IDirect3DDevice9.SetTransform
title: IDirect3DDevice9::SetTransform (d3d9helper.h)
description: The IDirect3DDevice9::SetTransform method (d3d9helper.h) sets a single device transformation-related state.
helpviewer_keywords: ["25042e52-3212-5250-0bac-ab23f76aaeb1","IDirect3DDevice9 interface [Direct3D 9]","SetTransform method","IDirect3DDevice9.SetTransform","IDirect3DDevice9::SetTransform","SetTransform","SetTransform method [Direct3D 9]","SetTransform method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetTransform","direct3d9.idirect3ddevice9__settransform"]
old-location: direct3d9\idirect3ddevice9__settransform.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__settransform.htm
ms.date: 08/11/2022
ms.keywords: 25042e52-3212-5250-0bac-ab23f76aaeb1, IDirect3DDevice9 interface [Direct3D 9],SetTransform method, IDirect3DDevice9.SetTransform, IDirect3DDevice9::SetTransform, SetTransform, SetTransform method [Direct3D 9], SetTransform method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetTransform, direct3d9.idirect3ddevice9__settransform
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
 - IDirect3DDevice9::SetTransform
 - d3d9helper/IDirect3DDevice9::SetTransform
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
 - IDirect3DDevice9.SetTransform
---

# IDirect3DDevice9::SetTransform


## -description

Sets a single device transformation-related state.

## -parameters

### -param State [in]

Type: <b><a href="/windows/desktop/direct3d9/d3dtransformstatetype">D3DTRANSFORMSTATETYPE</a></b>

Device-state variable that is being modified. This parameter can be any member of the <a href="/windows/desktop/direct3d9/d3dtransformstatetype">D3DTRANSFORMSTATETYPE</a> enumerated type, or the <a href="/windows/desktop/direct3d9/d3dts-worldmatrix">D3DTS_WORLDMATRIX</a> macro.

### -param pMatrix [in]

Type: <b>const <a href="/windows/desktop/direct3d9/d3dmatrix">D3DMATRIX</a>*</b>

Pointer to a <a href="/windows/desktop/direct3d9/d3dmatrix">D3DMATRIX</a> structure that modifies the current transformation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. D3DERR_INVALIDCALL is returned if one of the arguments is invalid.

## -see-also

<a href="/windows/desktop/direct3d9/d3dts-world">D3DTS_WORLD</a>



<a href="/windows/desktop/direct3d9/d3dts-worldmatrix">D3DTS_WORLDMATRIX</a>



<a href="/windows/desktop/direct3d9/d3dts-worldn">D3DTS_WORLDn</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettransform">IDirect3DDevice9::GetTransform</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate">IDirect3DDevice9::SetRenderState</a>
