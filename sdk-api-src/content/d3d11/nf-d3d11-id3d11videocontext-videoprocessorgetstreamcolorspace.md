---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamColorSpace
title: ID3D11VideoContext::VideoProcessorGetStreamColorSpace (d3d11.h)
author: windows-sdk-content
description: Gets the color space for an input stream of the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreamcolorspace.htm
tech.root: medfound
ms.assetid: 4D66147C-D4FC-40BC-B406-B40B6EA24D94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamColorSpace method, ID3D11VideoContext.VideoProcessorGetStreamColorSpace, ID3D11VideoContext::VideoProcessorGetStreamColorSpace, VideoProcessorGetStreamColorSpace, VideoProcessorGetStreamColorSpace method [Media Foundation], VideoProcessorGetStreamColorSpace method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamColorSpace, mf.id3d11videocontext_videoprocessorgetstreamcolorspace
ms.topic: method
f1_keywords: ["d3d11/ID3D11VideoContext.VideoProcessorGetStreamColorSpace"]
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
 - ID3D11VideoContext.VideoProcessorGetStreamColorSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::VideoProcessorGetStreamColorSpace


## -description


Gets the color space for an input stream of the video processor.




## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pColorSpace [out]

Receives a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_color_space">D3D11_VIDEO_PROCESSOR_COLOR_SPACE</a> value that specifies the color space.


## -returns



This method does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

