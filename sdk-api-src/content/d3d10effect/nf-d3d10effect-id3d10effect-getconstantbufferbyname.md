---
UID: NF:d3d10effect.ID3D10Effect.GetConstantBufferByName
title: ID3D10Effect::GetConstantBufferByName
author: windows-sdk-content
description: Get a constant buffer by name.
old-location: direct3d10\id3d10effect_getconstantbufferbyname.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getconstantbufferbyname.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetConstantBufferByName, GetConstantBufferByName method [Direct3D 10], GetConstantBufferByName method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetConstantBufferByName method, ID3D10Effect.GetConstantBufferByName, ID3D10Effect::GetConstantBufferByName, d3d10effect/ID3D10Effect::GetConstantBufferByName, direct3d10.id3d10effect_getconstantbufferbyname, ee9f35f2-1d6f-f921-a7a3-825ac2b49866
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
 - ID3D10Effect.GetConstantBufferByName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Effect::GetConstantBufferByName


## -description


Get a constant buffer by name.


## -parameters




### -param Name [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

The constant-buffer name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/ab75de06-dbcd-42bb-9879-8602df7f558f">ID3D10EffectConstantBuffer</a>*</b>

A pointer to the constant buffer indicated by the Name. See <a href="https://msdn.microsoft.com/ab75de06-dbcd-42bb-9879-8602df7f558f">ID3D10EffectConstantBuffer</a>.




## -remarks



An effect that contains a variable that will be read/written by an application requires at least one constant buffer. For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.




## -see-also




<a href="https://msdn.microsoft.com/3525d559-11e4-4c38-acfe-5dc560264c31">ID3D10Effect Interface</a>
 

 

