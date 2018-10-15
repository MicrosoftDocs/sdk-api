---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamFrameFormat
title: ID3D11VideoContext::VideoProcessorSetStreamFrameFormat
author: windows-sdk-content
description: Specifies whether an input stream on the video processor contains interlaced or progressive frames.
old-location: mf\id3d11videocontext_videoprocessorsetstreamframeformat.htm
tech.root: medfound
ms.assetid: 248BE244-23A9-4F4E-95F7-D3DB678B2D9F
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamFrameFormat method, ID3D11VideoContext.VideoProcessorSetStreamFrameFormat, ID3D11VideoContext::VideoProcessorSetStreamFrameFormat, VideoProcessorSetStreamFrameFormat, VideoProcessorSetStreamFrameFormat method [Media Foundation], VideoProcessorSetStreamFrameFormat method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamFrameFormat, mf.id3d11videocontext_videoprocessorsetstreamframeformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D11VideoContext.VideoProcessorSetStreamFrameFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetStreamFrameFormat


## -description


Specifies whether an input stream on the video processor contains interlaced or progressive frames.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param FrameFormat

A <a href="https://msdn.microsoft.com/en-us/library/Hh447647(v=VS.85).aspx">D3D11_VIDEO_FRAME_FORMAT</a> value that specifies the interlacing.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

