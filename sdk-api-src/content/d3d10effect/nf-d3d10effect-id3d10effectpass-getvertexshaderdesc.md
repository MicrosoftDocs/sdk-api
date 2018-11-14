---
UID: NF:d3d10effect.ID3D10EffectPass.GetVertexShaderDesc
title: ID3D10EffectPass::GetVertexShaderDesc
author: windows-sdk-content
description: Get a vertex-shader description.
old-location: direct3d10\id3d10effectpass_getvertexshaderdesc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_getvertexshaderdesc.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetVertexShaderDesc, GetVertexShaderDesc method [Direct3D 10], GetVertexShaderDesc method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],GetVertexShaderDesc method, ID3D10EffectPass.GetVertexShaderDesc, ID3D10EffectPass::GetVertexShaderDesc, b37921cf-8046-f37a-5f59-51591614b4d3, d3d10effect/ID3D10EffectPass::GetVertexShaderDesc, direct3d10.id3d10effectpass_getvertexshaderdesc
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D10EffectPass.GetVertexShaderDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10effect.h
: 
- ID3D10EffectPass.GetVertexShaderDesc
: 
---

# ID3D10EffectPass::GetVertexShaderDesc


## -description


Get a vertex-shader description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205331(v=VS.85).aspx">D3D10_PASS_SHADER_DESC</a>*</b>

A pointer to a vertex-shader description (see <a href="https://msdn.microsoft.com/en-us/library/Bb205331(v=VS.85).aspx">D3D10_PASS_SHADER_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



An effect pass can contain render state assignments and shader object assignments.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173656(v=VS.85).aspx">ID3D10EffectPass</a>
 

 

