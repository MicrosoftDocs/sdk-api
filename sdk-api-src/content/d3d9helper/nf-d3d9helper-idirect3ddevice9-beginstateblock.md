---
UID: NF:d3d9helper.IDirect3DDevice9.BeginStateBlock
title: IDirect3DDevice9::BeginStateBlock (d3d9helper.h)
description: The IDirect3DDevice9::BeginStateBlock method (d3d9.h) signals Direct3D to begin recording a device-state block.
helpviewer_keywords: ["01991d00-eca6-e8db-e657-6432fe3184f2","BeginStateBlock","BeginStateBlock method [Direct3D 9]","BeginStateBlock method [Direct3D 9]","IDirect3DDevice9 interface","IDirect3DDevice9 interface [Direct3D 9]","BeginStateBlock method","IDirect3DDevice9.BeginStateBlock","IDirect3DDevice9::BeginStateBlock","d3d9helper/IDirect3DDevice9::BeginStateBlock","direct3d9.idirect3ddevice9__beginstateblock"]
old-location: direct3d9\idirect3ddevice9__beginstateblock.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__beginstateblock.htm
ms.date: 08/11/2022
ms.keywords: 01991d00-eca6-e8db-e657-6432fe3184f2, BeginStateBlock, BeginStateBlock method [Direct3D 9], BeginStateBlock method [Direct3D 9],IDirect3DDevice9 interface, IDirect3DDevice9 interface [Direct3D 9],BeginStateBlock method, IDirect3DDevice9.BeginStateBlock, IDirect3DDevice9::BeginStateBlock, d3d9helper/IDirect3DDevice9::BeginStateBlock, direct3d9.idirect3ddevice9__beginstateblock
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
 - IDirect3DDevice9::BeginStateBlock
 - d3d9helper/IDirect3DDevice9::BeginStateBlock
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
 - IDirect3DDevice9.BeginStateBlock
---

# IDirect3DDevice9::BeginStateBlock


## -description

Signals Direct3D to begin recording a device-state block.



## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be one of the following: D3DERR_INVALIDCALL, E_OUTOFMEMORY.

## -remarks

Applications can ensure that all recorded states are valid by calling the <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-validatedevice">IDirect3DDevice9::ValidateDevice</a> method prior to calling this method.

The following methods can be recorded in a state block, after calling <b>IDirect3DDevice9::BeginStateBlock</b> and before <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endstateblock">IDirect3DDevice9::EndStateBlock</a>. 

<ul>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-lightenable">IDirect3DDevice9::LightEnable</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setclipplane">IDirect3DDevice9::SetClipPlane</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setcurrenttexturepalette">IDirect3DDevice9::SetCurrentTexturePalette</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setfvf">IDirect3DDevice9::SetFVF</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setindices">IDirect3DDevice9::SetIndices</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight">IDirect3DDevice9::SetLight</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial">IDirect3DDevice9::SetMaterial</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode">IDirect3DDevice9::SetNPatchMode</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader">IDirect3DDevice9::SetPixelShader</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb">IDirect3DDevice9::SetPixelShaderConstantB</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf">IDirect3DDevice9::SetPixelShaderConstantF</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti">IDirect3DDevice9::SetPixelShaderConstantI</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate">IDirect3DDevice9::SetRenderState</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate">IDirect3DDevice9::SetSamplerState</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setscissorrect">IDirect3DDevice9::SetScissorRect</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource">IDirect3DDevice9::SetStreamSource</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq">IDirect3DDevice9::SetStreamSourceFreq</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture">IDirect3DDevice9::SetTexture</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate">IDirect3DDevice9::SetTextureStageState</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform">IDirect3DDevice9::SetTransform</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setviewport">IDirect3DDevice9::SetViewport</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration">IDirect3DDevice9::SetVertexDeclaration</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader">IDirect3DDevice9::SetVertexShader</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb">IDirect3DDevice9::SetVertexShaderConstantB</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf">IDirect3DDevice9::SetVertexShaderConstantF</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti">IDirect3DDevice9::SetVertexShaderConstantI</a>
</li>
</ul>
The ordering of state changes in a state block is not guaranteed. If the same state is specified multiple times in a state block, only the last value is used.

## -see-also

<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-createstateblock">IDirect3DDevice9::CreateStateBlock</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endstateblock">IDirect3DDevice9::EndStateBlock</a>
