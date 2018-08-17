---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamDestRect
title: ID3D11VideoContext::VideoProcessorSetStreamDestRect
author: windows-sdk-content
description: Sets the destination rectangle for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreamdestrect.htm
old-project: medfound
ms.assetid: F3C77812-9096-4D65-9D6C-082133C873A7
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamDestRect method, ID3D11VideoContext.VideoProcessorSetStreamDestRect, ID3D11VideoContext::VideoProcessorSetStreamDestRect, VideoProcessorSetStreamDestRect, VideoProcessorSetStreamDestRect method [Media Foundation], VideoProcessorSetStreamDestRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamDestRect, mf.id3d11videocontext_videoprocessorsetstreamdestrect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorSetStreamDestRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorSetStreamDestRect


## -description


Sets the destination rectangle for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable [in]

Specifies whether to apply the destination rectangle.


### -param pRect [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the destination rectangle. If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored.


## -returns



This method does not return a value.




## -remarks



The destination rectangle is the portion of the output surface that receives the blit for this stream. The destination rectangle is given in pixel coordinates, relative to the output surface.

The default destination rectangle is an empty rectangle (0, 0, 0, 0). If this method is never called, or if the <i>Enable</i> parameter is <b>FALSE</b>, no data is written from this stream. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

