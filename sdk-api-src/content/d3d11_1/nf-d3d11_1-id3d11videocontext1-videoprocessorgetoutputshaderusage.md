---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorGetOutputShaderUsage
title: ID3D11VideoContext1::VideoProcessorGetOutputShaderUsage (d3d11_1.h)
author: windows-sdk-content
description: Gets a value indicating whether the output surface from a call to ID3D11VideoContext::VideoProcessorBlt can be read by Direct3D shaders.
old-location: mf\id3d11videocontext1_videoprocessorgetoutputshaderusage.htm
tech.root: medfound
ms.assetid: B75BDC83-3065-41F8-B552-B38BCB4BFC66
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorGetOutputShaderUsage method, ID3D11VideoContext1.VideoProcessorGetOutputShaderUsage, ID3D11VideoContext1::VideoProcessorGetOutputShaderUsage, VideoProcessorGetOutputShaderUsage, VideoProcessorGetOutputShaderUsage method [Media Foundation], VideoProcessorGetOutputShaderUsage method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorGetOutputShaderUsage, mf.id3d11videocontext1_videoprocessorgetoutputshaderusage
ms.topic: method
f1_keywords: ["d3d11_1/ID3D11VideoContext1.VideoProcessorGetOutputShaderUsage"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.VideoProcessorGetOutputShaderUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext1::VideoProcessorGetOutputShaderUsage


## -description


Gets a value indicating whether the output surface from a call to <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> can be read by Direct3D shaders.


## -parameters




### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface.


### -param pShaderUsage [out]

Type: <b>BOOL*</b>

A pointer to a boolean value indicating if the output surface can be read by Direct3D shaders. True if the surface rendered using <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-videoprocessorblt">ID3D11VideoContext::VideoProcessorBlt</a> can be read by Direct3D shaders; otherwise, false.


## -returns



This method does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>
 

 

