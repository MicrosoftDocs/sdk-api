---
UID: NF:d3d9.IDirect3DDevice9.SetTexture
title: IDirect3DDevice9::SetTexture (d3d9.h)
description: The IDirect3DDevice9::SetTexture method (d3d9helper.h) assigns a texture to a stage for a device. 
helpviewer_keywords: ["30fa2907-7b07-b99a-b9b6-50d38166ea7d","IDirect3DDevice9 interface [Direct3D 9]","SetTexture method","IDirect3DDevice9.SetTexture","IDirect3DDevice9::SetTexture","SetTexture","SetTexture method [Direct3D 9]","SetTexture method [Direct3D 9]","IDirect3DDevice9 interface","d3d9helper/IDirect3DDevice9::SetTexture","direct3d9.idirect3ddevice9__settexture"]
old-location: direct3d9\idirect3ddevice9__settexture.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9__settexture.htm
ms.date: 08/11/2022
ms.keywords: 30fa2907-7b07-b99a-b9b6-50d38166ea7d, IDirect3DDevice9 interface [Direct3D 9],SetTexture method, IDirect3DDevice9.SetTexture, IDirect3DDevice9::SetTexture, SetTexture, SetTexture method [Direct3D 9], SetTexture method [Direct3D 9],IDirect3DDevice9 interface, d3d9helper/IDirect3DDevice9::SetTexture, direct3d9.idirect3ddevice9__settexture
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
 - IDirect3DDevice9::SetTexture
 - d3d9/IDirect3DDevice9::SetTexture
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
 - IDirect3DDevice9.SetTexture
---

# IDirect3DDevice9::SetTexture


## -description

Assigns a texture to a stage for a device.

## -parameters

### -param Stage [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Zero based sampler number.  Textures are bound to samplers; samplers define sampling state such as the filtering mode and the address wrapping mode. Textures are referenced differently by the programmable and the fixed function pipeline:
    


<ul>
<li>Programmable shaders reference textures using the sampler number. The number of samplers available to a programmable shader is dependent on the shader version. For vertex shaders, see <a href="/windows/desktop/direct3dhlsl/dx9-graphics-reference-asm-vs-registers-sampler">Sampler (Direct3D 9 asm-vs)</a>. For pixel shaders see <a href="/windows/desktop/direct3dhlsl/dx9-graphics-reference-asm-ps-registers-sampler">Sampler (Direct3D 9 asm-ps)</a>.</li>
<li>The fixed function pipeline on the other hand, references textures by texture stage number. The maximum number of samplers is determined from two caps: MaxSimultaneousTextures and MaxTextureBlendStages of the <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9">D3DCAPS9</a> structure.</li>
</ul>
There are two other special cases for stage/sampler numbers.

<ul>
<li>A special number called D3DDMAPSAMPLER is used for <a href="/windows/desktop/direct3d9/displacement-mapping">Displacement Mapping (Direct3D 9)</a>.</li>
<li>A programmable vertex shader uses a special number defined by a <a href="/windows/desktop/direct3d9/d3dvertextexturesampler">D3DVERTEXTEXTURESAMPLER</a> when accessing <a href="/windows/desktop/direct3d9/vertex-textures-in-vs-3-0">Vertex Textures in vs_3_0 (DirectX HLSL)</a>.</li>
</ul>

### -param pTexture [in]

Type: <b><a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a>*</b>

Pointer to an <a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9">IDirect3DBaseTexture9</a> interface, representing the texture being set.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.

## -remarks

<b>SetTexture</b> is not allowed if the texture is created with a pool type of D3DPOOL_SCRATCH. <b>SetTexture</b> is not allowed with a pool type of D3DPOOL_SYSTEMMEM texture unless DevCaps is set with D3DDEVCAPS_TEXTURESYSTEMMEMORY.

## -see-also

<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexture">GetTexture</a>



<a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate">GetTextureStageState</a>



<a href="/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3ddevice9">IDirect3DDevice9</a>



<a href="/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate">SetTextureStageState</a>
