---
UID: NF:d3d10effect.ID3D10Effect.GetConstantBufferByIndex
title: ID3D10Effect::GetConstantBufferByIndex (d3d10effect.h)
author: windows-sdk-content
description: Get a constant buffer by index.
old-location: direct3d10\id3d10effect_getconstantbufferbyindex.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effect_getconstantbufferbyindex.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 6e59189f-e563-27f9-5003-f6af77fe5eb9, GetConstantBufferByIndex, GetConstantBufferByIndex method [Direct3D 10], GetConstantBufferByIndex method [Direct3D 10],ID3D10Effect interface, ID3D10Effect interface [Direct3D 10],GetConstantBufferByIndex method, ID3D10Effect.GetConstantBufferByIndex, ID3D10Effect::GetConstantBufferByIndex, d3d10effect/ID3D10Effect::GetConstantBufferByIndex, direct3d10.id3d10effect_getconstantbufferbyindex
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
 - ID3D10Effect.GetConstantBufferByIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Effect::GetConstantBufferByIndex


## -description


Get a constant buffer by index.


## -parameters




### -param Index [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based index.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectconstantbuffer">ID3D10EffectConstantBuffer</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectconstantbuffer">ID3D10EffectConstantBuffer Interface</a>.




## -remarks



An effect that contains a variable that will be read/written by an application requires at least one constant buffer. For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect">ID3D10Effect Interface</a>
 

 

