---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamSourceRect
title: ID3D11VideoContext::VideoProcessorSetStreamSourceRect
author: windows-sdk-content
description: Sets the source rectangle for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreamsourcerect.htm
tech.root: medfound
ms.assetid: A2771C8A-13AB-4AFA-87A1-1390B582342A
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamSourceRect method, ID3D11VideoContext.VideoProcessorSetStreamSourceRect, ID3D11VideoContext::VideoProcessorSetStreamSourceRect, VideoProcessorSetStreamSourceRect, VideoProcessorSetStreamSourceRect method [Media Foundation], VideoProcessorSetStreamSourceRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamSourceRect, mf.id3d11videocontext_videoprocessorsetstreamsourcerect
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
 - ID3D11VideoContext.VideoProcessorSetStreamSourceRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetStreamSourceRect


## -description


Sets the source rectangle for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable [in]

Specifies whether to apply the source rectangle.


### -param pRect [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that specifies the source rectangle. If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored.


## -returns



This method does not return a value.




## -remarks



The source rectangle is the portion of the input surface that is  blitted to the destination surface. The source rectangle is given in pixel coordinates, relative to the input surface.

If this method is never called, or if the <i>Enable</i> parameter is <b>FALSE</b>, the video processor reads from the entire input surface.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

