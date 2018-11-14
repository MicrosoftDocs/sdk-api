---
UID: NF:d3d11_1.ID3D11VideoContext1.VideoProcessorSetOutputShaderUsage
title: ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage
author: windows-sdk-content
description: Sets a value indicating whether the output surface from a call to ID3D11VideoContext::VideoProcessorBlt will be read by Direct3D shaders.
old-location: mf\id3d11videocontext1_videoprocessorsetoutputshaderusage.htm
tech.root: medfound
ms.assetid: 84901282-D4FF-4084-B016-50A66910D0A2
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ID3D11VideoContext1 interface [Media Foundation],VideoProcessorSetOutputShaderUsage method, ID3D11VideoContext1.VideoProcessorSetOutputShaderUsage, ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage, VideoProcessorSetOutputShaderUsage, VideoProcessorSetOutputShaderUsage method [Media Foundation], VideoProcessorSetOutputShaderUsage method [Media Foundation],ID3D11VideoContext1 interface, d3d11_1/ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage, mf.id3d11videocontext1_videoprocessorsetoutputshaderusage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D11VideoContext1.VideoProcessorSetOutputShaderUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d11_1.h
: 
- ID3D11VideoContext1.VideoProcessorSetOutputShaderUsage
: 
---

# ID3D11VideoContext1::VideoProcessorSetOutputShaderUsage


## -description


Sets a value indicating whether the output surface from a call to <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a> will be read by Direct3D shaders.


## -parameters




### -param pVideoProcessor [in]

Type: <b>ID3D11VideoProcessor*</b>

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface.


### -param ShaderUsage [in]

Type: <b>BOOL</b>

True if the surface rendered using <a href="https://msdn.microsoft.com/D526BB31-A4B9-4BBD-BAE3-43FDFF58A32A">ID3D11VideoContext::VideoProcessorBlt</a> will be read by Direct3D shaders; otherwise, false. This may be set to false when multi-plane overlay hardware is supported.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

