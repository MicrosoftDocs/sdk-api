---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamFrameFormat
title: ID3D11VideoContext::VideoProcessorSetStreamFrameFormat (d3d11.h)
author: windows-sdk-content
description: Specifies whether an input stream on the video processor contains interlaced or progressive frames.
old-location: mf\id3d11videocontext_videoprocessorsetstreamframeformat.htm
tech.root: medfound
ms.assetid: 248BE244-23A9-4F4E-95F7-D3DB678B2D9F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamFrameFormat method, ID3D11VideoContext.VideoProcessorSetStreamFrameFormat, ID3D11VideoContext::VideoProcessorSetStreamFrameFormat, VideoProcessorSetStreamFrameFormat, VideoProcessorSetStreamFrameFormat method [Media Foundation], VideoProcessorSetStreamFrameFormat method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamFrameFormat, mf.id3d11videocontext_videoprocessorsetstreamframeformat
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

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param FrameFormat

A <a href="https://msdn.microsoft.com/D0C0C58C-8BBC-4C2C-BD0B-4244211E7E06">D3D11_VIDEO_FRAME_FORMAT</a> value that specifies the interlacing.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

