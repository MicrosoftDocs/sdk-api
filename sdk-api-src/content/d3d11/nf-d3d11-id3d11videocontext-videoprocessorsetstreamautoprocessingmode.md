---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamAutoProcessingMode
title: ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode
author: windows-sdk-content
description: Enables or disables automatic processing features on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreamautoprocessingmode.htm
tech.root: medfound
ms.assetid: 92579A03-AA8A-4D9B-8150-F5FDDBAFC1C1
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamAutoProcessingMode method, ID3D11VideoContext.VideoProcessorSetStreamAutoProcessingMode, ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode, VideoProcessorSetStreamAutoProcessingMode, VideoProcessorSetStreamAutoProcessingMode method [Media Foundation], VideoProcessorSetStreamAutoProcessingMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode, mf.id3d11videocontext_videoprocessorsetstreamautoprocessingmode
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
 - ID3D11VideoContext.VideoProcessorSetStreamAutoProcessingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetStreamAutoProcessingMode


## -description


Enables or disables automatic processing features on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable [in]

If <b>TRUE</b>, automatic processing features are enabled. If <b>FALSE</b>, the driver disables any  extra video processing that it might be performing.


## -returns



This method does not return a value.




## -remarks



By default, the driver might perform certain processing tasks automatically during the video processor blit. This method enables the application to disable these extra video processing features. For example, if you provide your own pixel  shader for the video processor, you might want to disable the driver's automatic processing.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

