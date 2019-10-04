---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamAutoProcessingMode
title: ID3D11VideoContext::VideoProcessorGetStreamAutoProcessingMode (d3d11.h)
author: windows-sdk-content
description: Queries whether automatic processing features of the video processor are enabled.
old-location: mf\id3d11videocontext_videoprocessorgetstreamautoprocessingmode.htm
tech.root: medfound
ms.assetid: FD7B20C2-5418-4CA5-A64E-FA84D4070A10
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamAutoProcessingMode method, ID3D11VideoContext.VideoProcessorGetStreamAutoProcessingMode, ID3D11VideoContext::VideoProcessorGetStreamAutoProcessingMode, VideoProcessorGetStreamAutoProcessingMode, VideoProcessorGetStreamAutoProcessingMode method [Media Foundation], VideoProcessorGetStreamAutoProcessingMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamAutoProcessingMode, mf.id3d11videocontext_videoprocessorgetstreamautoprocessingmode
ms.topic: method
f1_keywords: 
 - "d3d11/ID3D11VideoContext.VideoProcessorGetStreamAutoProcessingMode"
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
 - ID3D11VideoContext.VideoProcessorGetStreamAutoProcessingMode
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::VideoProcessorGetStreamAutoProcessingMode


## -description


Queries whether automatic processing features of the video processor are enabled.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pEnabled [out]

Receives the value <b>TRUE</b> if automatic processing features are enabled, or <b>FALSE</b> otherwise.


## -returns



This method does not return a value.




## -remarks



Automatic processing  refers to additional image processing that drivers might have performed on the image data prior to the application receiving the data.   




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

