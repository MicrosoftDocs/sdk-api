---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamAutoProcessingMode
title: ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode (d3d11.h)
description: Enables or disables automatic processing features on the video processor.
helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorSetStreamAutoProcessingMode method","ID3D11VideoContext.VideoProcessorSetStreamAutoProcessingMode","ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode","VideoProcessorSetStreamAutoProcessingMode","VideoProcessorSetStreamAutoProcessingMode method [Media Foundation]","VideoProcessorSetStreamAutoProcessingMode method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode","mf.id3d11videocontext_videoprocessorsetstreamautoprocessingmode"]
old-location: mf\id3d11videocontext_videoprocessorsetstreamautoprocessingmode.htm
tech.root: mf
ms.assetid: 92579A03-AA8A-4D9B-8150-F5FDDBAFC1C1
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamAutoProcessingMode method, ID3D11VideoContext.VideoProcessorSetStreamAutoProcessingMode, ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode, VideoProcessorSetStreamAutoProcessingMode, VideoProcessorSetStreamAutoProcessingMode method [Media Foundation], VideoProcessorSetStreamAutoProcessingMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode, mf.id3d11videocontext_videoprocessorsetstreamautoprocessingmode
f1_keywords:
- d3d11/ID3D11VideoContext.VideoProcessorSetStreamAutoProcessingMode
dev_langs:
- c++
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- d3d11.h
api_name:
- ID3D11VideoContext.VideoProcessorSetStreamAutoProcessingMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode


## -description


Enables or disables automatic processing features on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable [in]

If <b>TRUE</b>, automatic processing features are enabled. If <b>FALSE</b>, the driver disables any  extra video processing that it might be performing.


## -remarks



By default, the driver might perform certain processing tasks automatically during the video processor blit. This method enables the application to disable these extra video processing features. For example, if you provide your own pixel  shader for the video processor, you might want to disable the driver's automatic processing.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

