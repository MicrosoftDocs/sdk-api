---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetOutputSignatureElementDesc
title: ID3D10EffectShaderVariable::GetOutputSignatureElementDesc (d3d10effect.h)
author: windows-sdk-content
description: Get an output-signature description.
old-location: direct3d10\id3d10effectshadervariable_getoutputsignatureelementdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getoutputsignatureelementdesc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 099e180b-e0ef-fb4c-2ecb-2e42899814e8, GetOutputSignatureElementDesc, GetOutputSignatureElementDesc method [Direct3D 10], GetOutputSignatureElementDesc method [Direct3D 10],ID3D10EffectShaderVariable interface, ID3D10EffectShaderVariable interface [Direct3D 10],GetOutputSignatureElementDesc method, ID3D10EffectShaderVariable.GetOutputSignatureElementDesc, ID3D10EffectShaderVariable::GetOutputSignatureElementDesc, d3d10effect/ID3D10EffectShaderVariable::GetOutputSignatureElementDesc, direct3d10.id3d10effectshadervariable_getoutputsignatureelementdesc
ms.topic: method
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
 - ID3D10EffectShaderVariable.GetOutputSignatureElementDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10EffectShaderVariable::GetOutputSignatureElementDesc


## -description


Get an output-signature description.


## -parameters




### -param ShaderIndex [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based shader index.


### -param Element [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based element index.


### -param pDesc [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/ns-d3d10shader-_d3d10_signature_parameter_desc">D3D10_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a parameter description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10shader/ns-d3d10shader-_d3d10_signature_parameter_desc">D3D10_SIGNATURE_PARAMETER_DESC</a>).


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

Returns one of the following <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.




## -remarks



An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters). The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshaderresourcevariable">ID3D10EffectShaderResourceVariable Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshadervariable">ID3D10EffectShaderVariable</a>
 

 

