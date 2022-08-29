---
UID: NF:d3d9helper.IDirect3DDevice9.SetVertexShader
title: IDirect3DDevice9::SetVertexShader (d3d9helper.h)
description: The IDirect3DDevice9::SetVertexShader method (d3d9helper.h) sets the vertex shader.
helpviewer_keywords: ["4fecc980-501f-804d-d212-782bd9df73d4","IDirect3DDevice9 interface [Direct3D 9]","SetVertexShader method","IDirect3DDevice9.SetVertexShader","IDirect3DDevice9::SetVertexShader","SetVertexShader","SetVertexShader method [Direct3D 9]","SetVertexShader method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetVertexShader","direct3d9.idirect3ddevice9__setvertexshader"]
old-location: direct3d9\idirect3ddevice9__setvertexshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__setvertexshader.htm
ms.date: 08/11/2022
ms.keywords: 4fecc980-501f-804d-d212-782bd9df73d4, IDirect3DDevice9 interface [Direct3D 9],SetVertexShader method, IDirect3DDevice9.SetVertexShader, IDirect3DDevice9::SetVertexShader, SetVertexShader, SetVertexShader method [Direct3D 9], SetVertexShader method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetVertexShader, direct3d9.idirect3ddevice9__setvertexshader
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
 - IDirect3DDevice9::SetVertexShader
 - d3d9helper/IDirect3DDevice9::SetVertexShader
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
 - IDirect3DDevice9.SetVertexShader
---

# IDirect3DDevice9::SetVertexShader


## -description

Sets the vertex shader.

## -parameters

### -param pShader [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9">IDirect3DVertexShader9</a>*</b>

Vertex shader interface. For more information, see <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9">IDirect3DVertexShader9</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

To set a fixed-function vertex shader (after having set a programmable vertex shader), call <b>IDirect3DDevice9::SetVertexShader</b>(NULL) to release the programmable shader, and then call <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf">IDirect3DDevice9::SetFVF</a> with the fixed-function vertex format.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshader">IDirect3DDevice9::GetVertexShader</a>
