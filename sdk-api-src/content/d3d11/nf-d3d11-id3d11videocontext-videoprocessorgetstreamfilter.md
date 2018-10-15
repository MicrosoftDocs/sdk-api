---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamFilter
title: ID3D11VideoContext::VideoProcessorGetStreamFilter
author: windows-sdk-content
description: Gets the image filter settings for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreamfilter.htm
tech.root: medfound
ms.assetid: E18146E9-FBF4-4A1E-AC6C-7500CDA9DC59
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamFilter method, ID3D11VideoContext.VideoProcessorGetStreamFilter, ID3D11VideoContext::VideoProcessorGetStreamFilter, VideoProcessorGetStreamFilter, VideoProcessorGetStreamFilter method [Media Foundation], VideoProcessorGetStreamFilter method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamFilter, mf.id3d11videocontext_videoprocessorgetstreamfilter
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
 - ID3D11VideoContext.VideoProcessorGetStreamFilter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetStreamFilter


## -description


Gets the image filter settings for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Filter [in]

The filter to query, specified as a <a href="https://msdn.microsoft.com/87CF9A1A-E196-4B5A-BAAE-DD948A5468C2">D3D11_VIDEO_PROCESSOR_FILTER</a> value.




### -param pEnabled [out]

Receives the value <b>TRUE</b> if the image filter is enabled, or <b>FALSE</b> otherwise.


### -param pLevel [out]

Receives the filter level.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

