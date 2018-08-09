---
UID: NF:d3d10effect.ID3D10EffectPass.GetGeometryShaderDesc
title: ID3D10EffectPass::GetGeometryShaderDesc
author: windows-sdk-content
description: Get a geometry-shader description.
old-location: direct3d10\id3d10effectpass_getgeometryshaderdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_getgeometryshaderdesc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 1f200fc8-f573-7b6c-75f4-5b7cf7a95eb1, GetGeometryShaderDesc, GetGeometryShaderDesc method [Direct3D 10], GetGeometryShaderDesc method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],GetGeometryShaderDesc method, ID3D10EffectPass.GetGeometryShaderDesc, ID3D10EffectPass::GetGeometryShaderDesc, d3d10effect/ID3D10EffectPass::GetGeometryShaderDesc, direct3d10.id3d10effectpass_getgeometryshaderdesc
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D10EffectPass.GetGeometryShaderDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectPass::GetGeometryShaderDesc


## -description


Get a geometry-shader description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb205331(v=VS.85).aspx">D3D10_PASS_SHADER_DESC</a>*</b>

A pointer to a geometry-shader description (see <a href="https://msdn.microsoft.com/en-us/library/Bb205331(v=VS.85).aspx">D3D10_PASS_SHADER_DESC</a>).


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



An effect pass can contain render state assignments and shader object assignments.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173630(v=VS.85).aspx">ID3D10Effect Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb173656(v=VS.85).aspx">ID3D10EffectPass</a>
 

 

