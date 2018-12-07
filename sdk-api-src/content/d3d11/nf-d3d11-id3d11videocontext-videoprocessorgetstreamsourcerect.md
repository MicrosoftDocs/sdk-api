---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamSourceRect
title: ID3D11VideoContext::VideoProcessorGetStreamSourceRect
author: windows-sdk-content
description: Gets the source rectangle for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreamsourcerect.htm
tech.root: medfound
ms.assetid: 52AFE959-695B-4797-ABCF-B8264046E4BE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamSourceRect method, ID3D11VideoContext.VideoProcessorGetStreamSourceRect, ID3D11VideoContext::VideoProcessorGetStreamSourceRect, VideoProcessorGetStreamSourceRect, VideoProcessorGetStreamSourceRect method [Media Foundation], VideoProcessorGetStreamSourceRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamSourceRect, mf.id3d11videocontext_videoprocessorgetstreamsourcerect
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
 - ID3D11VideoContext.VideoProcessorGetStreamSourceRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetStreamSourceRect


## -description


Gets the source rectangle for an input stream on the video processor.




## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pEnabled [out]

Receives the value <b>TRUE</b> if the source rectangle is enabled, or <b>FALSE</b> otherwise.


### -param pRect [out]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the source rectangle.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

