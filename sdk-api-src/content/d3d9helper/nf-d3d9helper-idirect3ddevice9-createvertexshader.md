---
UID: NF:d3d9helper.IDirect3DDevice9.CreateVertexShader
title: IDirect3DDevice9::CreateVertexShader (d3d9helper.h)
description: The IDirect3DDevice9::CreateVertexShader method (d3d9helper.h) creates a vertex shader.
helpviewer_keywords: ["42a56eab-a68f-232a-b21e-cc24c0b7b58d","CreateVertexShader","CreateVertexShader method [Direct3D 9]","CreateVertexShader method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","CreateVertexShader method","IDirect3DDevice9.CreateVertexShader","IDirect3DDevice9::CreateVertexShader","d3d9helper/IDirect3DDevice9::CreateVertexShader","direct3d9.idirect3ddevice9__createvertexshader"]
old-location: direct3d9\idirect3ddevice9__createvertexshader.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__createvertexshader.htm
ms.date: 08/11/2022
ms.keywords: 42a56eab-a68f-232a-b21e-cc24c0b7b58d, CreateVertexShader, CreateVertexShader method [Direct3D 9], CreateVertexShader method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],CreateVertexShader method, IDirect3DDevice9.CreateVertexShader, IDirect3DDevice9::CreateVertexShader, d3d9helper/IDirect3DDevice9::CreateVertexShader, direct3d9.idirect3ddevice9__createvertexshader
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
 - IDirect3DDevice9::CreateVertexShader
 - d3d9helper/IDirect3DDevice9::CreateVertexShader
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
 - IDirect3DDevice9.CreateVertexShader
---

# IDirect3DDevice9::CreateVertexShader


## -description

Creates a vertex shader.

## -parameters

### -param pFunction [in]

Type: <b>const <a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

Pointer to an array of tokens that represents the vertex shader, including any embedded debug and symbol table information. 
    


<ul>
<li>Use a function such as <a href="/windows/desktop/direct3d9/d3dxcompileshader">D3DXCompileShader</a> to create the array from a HLSL shader.</li>
<li>Use a function like <a href="/windows/desktop/direct3d9/d3dxassembleshader">D3DXAssembleShader</a> to create the token array from an assembly language shader.</li>
<li>Use a function like <a href="/windows/desktop/direct3d9/id3dxeffectcompiler--compileshader">ID3DXEffectCompiler::CompileShader</a> to create the array from an effect.</li>
</ul>

### -param ppShader [out, retval]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9">IDirect3DVertexShader9</a>**</b>

Pointer to the returned vertex shader interface (see <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9">IDirect3DVertexShader9</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, D3DERR_OUTOFVIDEOMEMORY, E_OUTOFMEMORY.

## -remarks

When a device is created, <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice">IDirect3D9::CreateDevice</a> uses the behavior flag to determine whether to process vertices in hardware or software. There are three possibilities:

<ul>
<li>Process vertices in hardware by setting D3DCREATE_HARDWARE_VERTEXPROCESSING.</li>
<li>Process vertices in software by setting D3DCREATE_SOFTWARE_VERTEXPROCESSING.</li>
<li>Process vertices in either hardware or software by setting D3DCREATE_MIXED_VERTEXPROCESSING. To switch a mixed-mode device between software and hardware processing, use <a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing">IDirect3DDevice9::SetSoftwareVertexProcessing</a>.</li>
</ul>
For an example using <a href="/windows/desktop/direct3d9/d3dxcompileshader">D3DXCompileShader</a>, see <a href="https://msdn.microsoft.com/library/Ee417786(v=VS.85).aspx">HLSLwithoutEffects Sample</a>.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>
