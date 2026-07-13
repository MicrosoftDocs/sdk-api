---
UID: NF:d3d9helper.IDirect3DDevice9.GetVertexShader
title: IDirect3DDevice9::GetVertexShader (d3d9helper.h)
description: The IDirect3DDevice9::GetVertexShader method (d3d9.h) retrieves the currently set vertex shader.
helpviewer_keywords: ["GetVertexShader","GetVertexShader method [Direct3D 9]","GetVertexShader method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","GetVertexShader method","IDirect3DDevice9.GetVertexShader","IDirect3DDevice9::GetVertexShader","ce5c5bb1-c3dc-79d2-8932-365b84538ce0","d3d9helper/IDirect3DDevice9::GetVertexShader","direct3d9.idirect3ddevice9__getvertexshader"]
old-location: direct3d9\idirect3ddevice9__getvertexshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__getvertexshader.htm
ms.date: 08/11/2022
ms.keywords: GetVertexShader, GetVertexShader method [Direct3D 9], GetVertexShader method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],GetVertexShader method, IDirect3DDevice9.GetVertexShader, IDirect3DDevice9::GetVertexShader, ce5c5bb1-c3dc-79d2-8932-365b84538ce0, d3d9helper/IDirect3DDevice9::GetVertexShader, direct3d9.idirect3ddevice9__getvertexshader
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
 - IDirect3DDevice9::GetVertexShader
 - d3d9helper/IDirect3DDevice9::GetVertexShader
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
 - IDirect3DDevice9.GetVertexShader
---

# IDirect3DDevice9::GetVertexShader


## -description

Retrieves the currently set vertex shader.

## -parameters

### -param ppShader [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9">IDirect3DVertexShader9</a>**</b>

Pointer to a vertex shader interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.
 If ppShader is invalid, D3DERR_INVALIDCALL is returned.

## -remarks

Typically, methods that return state will not work on a device that is created using D3DCREATE_PUREDEVICE. This method however, will work even on a pure device because it returns an interface.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader">IDirect3DDevice9::SetVertexShader</a>
