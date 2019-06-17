---
UID: NF:d3d10effect.ID3D10EffectPass.GetPixelShaderDesc
title: ID3D10EffectPass::GetPixelShaderDesc (d3d10effect.h)
author: windows-sdk-content
description: Get a pixel-shader description.
old-location: direct3d10\id3d10effectpass_getpixelshaderdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_getpixelshaderdesc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetPixelShaderDesc, GetPixelShaderDesc method [Direct3D 10], GetPixelShaderDesc method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],GetPixelShaderDesc method, ID3D10EffectPass.GetPixelShaderDesc, ID3D10EffectPass::GetPixelShaderDesc, d3d10effect/ID3D10EffectPass::GetPixelShaderDesc, direct3d10.id3d10effectpass_getpixelshaderdesc, e9a087a4-34ef-3b9b-ee16-34ff7080b051
ms.topic: method
f1_keywords: ["d3d10effect/ID3D10EffectPass.GetPixelShaderDesc"]
req.header: d3d10effect.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectPass.GetPixelShaderDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectPass::GetPixelShaderDesc


## -description


Get a pixel-shader description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/ns-d3d10effect-_d3d10_pass_shader_desc">D3D10_PASS_SHADER_DESC</a>*</b>

A pointer to a pixel-shader description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/ns-d3d10effect-_d3d10_pass_shader_desc">D3D10_PASS_SHADER_DESC</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



An effect pass can contain render state assignments and shader object assignments.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectpass">ID3D10EffectPass</a>
 

 

