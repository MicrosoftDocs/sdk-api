---
UID: NF:d3d10effect.ID3D10EffectPass.GetPixelShaderDesc
title: ID3D10EffectPass::GetPixelShaderDesc
author: windows-sdk-content
description: Get a pixel-shader description.
old-location: direct3d10\id3d10effectpass_getpixelshaderdesc.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectpass_getpixelshaderdesc.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPixelShaderDesc, GetPixelShaderDesc method [Direct3D 10], GetPixelShaderDesc method [Direct3D 10],ID3D10EffectPass interface, ID3D10EffectPass interface [Direct3D 10],GetPixelShaderDesc method, ID3D10EffectPass.GetPixelShaderDesc, ID3D10EffectPass::GetPixelShaderDesc, d3d10effect/ID3D10EffectPass::GetPixelShaderDesc, direct3d10.id3d10effectpass_getpixelshaderdesc, e9a087a4-34ef-3b9b-ee16-34ff7080b051
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
 - ID3D10EffectPass.GetPixelShaderDesc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10EffectPass::GetPixelShaderDesc


## -description


Get a pixel-shader description.


## -parameters




### -param pDesc [in]

Type: <b><a href="https://msdn.microsoft.com/29dcb056-fc2c-4032-9e43-ac076e07b0a1">D3D10_PASS_SHADER_DESC</a>*</b>

A pointer to a pixel-shader description (see <a href="https://msdn.microsoft.com/29dcb056-fc2c-4032-9e43-ac076e07b0a1">D3D10_PASS_SHADER_DESC</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



An effect pass can contain render state assignments and shader object assignments.




## -see-also




<a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a>



<a href="https://msdn.microsoft.com/50407b6a-a05b-41e3-90a9-b0165378b177">ID3D10EffectPass</a>
 

 

