---
UID: NF:d3d10effect.ID3D10EffectShaderVariable.GetInputSignatureElementDesc
title: ID3D10EffectShaderVariable::GetInputSignatureElementDesc
author: windows-sdk-content
description: Get an input-signature description.
old-location: direct3d10\id3d10effectshadervariable_getinputsignatureelementdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectshadervariable_getinputsignatureelementdesc.htm
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: 22632913-ab5d-3124-504e-d04b7e203897, GetInputSignatureElementDesc, GetInputSignatureElementDesc method [Direct3D 10], GetInputSignatureElementDesc method [Direct3D 10],ID3D10EffectShaderVariable interface, ID3D10EffectShaderVariable interface [Direct3D 10],GetInputSignatureElementDesc method, ID3D10EffectShaderVariable.GetInputSignatureElementDesc, ID3D10EffectShaderVariable::GetInputSignatureElementDesc, d3d10effect/ID3D10EffectShaderVariable::GetInputSignatureElementDesc, direct3d10.id3d10effectshadervariable_getinputsignatureelementdesc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10effect.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D10_DEVICE_STATE_TYPES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectShaderVariable.GetInputSignatureElementDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectShaderVariable::GetInputSignatureElementDesc


## -description


Get an input-signature description.


## -parameters




### -param ShaderIndex [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based shader index.


### -param Element [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based shader-element index.


### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb172446(v=VS.85).aspx">D3D10_SIGNATURE_PARAMETER_DESC</a>*</b>

A pointer to a parameter description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172446(v=VS.85).aspx">D3D10_SIGNATURE_PARAMETER_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



An effect contains one or more shaders; each shader has an input and output signature; each signature contains one or more elements (or parameters). The shader index identifies the shader and the element index identifies the element (or parameter) in the shader signature.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173693(v=VS.85).aspx">ID3D10EffectShaderResourceVariable Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173698(v=VS.85).aspx">ID3D10EffectShaderVariable</a>
 

 

