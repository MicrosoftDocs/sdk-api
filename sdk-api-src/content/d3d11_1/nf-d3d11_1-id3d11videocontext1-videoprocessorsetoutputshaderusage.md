---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorSetOutputShaderUsage
title: ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage (d3d11_1.h)
description: Sets a value indicating whether the output surface from a call to ID3D11VideoContext::VideoProcessorBlt will be read by Direct3D shaders.
helpviewer_keywords: ["ID3D11VideoContext1 interface [Media Foundation]","VideoProcessorSetOutputShaderUsage method","ID3D11VideoContext1.VideoProcessorSetOutputShaderUsage","ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage","VideoProcessorSetOutputShaderUsage","VideoProcessorSetOutputShaderUsage method [Media Foundation]","VideoProcessorSetOutputShaderUsage method [Media Foundation]","ID3D11VideoContext1 interface","d3d11_1/ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage","mf.id3d11videocontext1_videoprocessorsetoutputshaderusage"]
old-location: mf\id3d11videocontext1_videoprocessorsetoutputshaderusage.htm
tech.root: mf
ms.assetid: 84901282-D4FF-4084-B016-50A66910D0A2
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorSetOutputShaderUsage method, ID3D11VideoContext1.VideoProcessorSetOutputShaderUsage, ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage, VideoProcessorSetOutputShaderUsage, VideoProcessorSetOutputShaderUsage method [Media Foundation], VideoProcessorSetOutputShaderUsage method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage, mf.id3d11videocontext1_videoprocessorsetoutputshaderusage
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage
 - d3d11_1/ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.VideoProcessorSetOutputShaderUsage
---

# ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage


## -description

Sets a value indicating whether the output surface from a call to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> will be read by Direct3D shaders.

## -parameters

### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.

### -param ShaderUsage [in]

Type: <b>BOOL</b>

True if the surface rendered using <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> will be read by Direct3D shaders; otherwise, false. This may be set to false when multi-plane overlay hardware is supported.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>