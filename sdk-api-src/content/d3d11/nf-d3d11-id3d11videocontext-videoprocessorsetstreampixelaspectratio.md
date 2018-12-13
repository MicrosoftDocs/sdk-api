---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamPixelAspectRatio
title: ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio
author: windows-sdk-content
description: Sets the pixel aspect ratio for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreampixelaspectratio.htm
tech.root: medfound
ms.assetid: 4205F6F0-4AF3-42B1-8636-64FCFC865856
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamPixelAspectRatio method, ID3D11VideoContext.VideoProcessorSetStreamPixelAspectRatio, ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio, VideoProcessorSetStreamPixelAspectRatio, VideoProcessorSetStreamPixelAspectRatio method [Media Foundation], VideoProcessorSetStreamPixelAspectRatio method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio, mf.id3d11videocontext_videoprocessorsetstreampixelaspectratio
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
 - ID3D11VideoContext.VideoProcessorSetStreamPixelAspectRatio
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetStreamPixelAspectRatio


## -description


Sets the pixel aspect ratio for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable [in]

Specifies whether the <i>pSourceAspectRatio</i> and <i>pDestinationAspectRatio</i> parameters contain valid values. Otherwise, the pixel aspect ratios are unspecified.


### -param pSourceAspectRatio [in]

A pointer to a <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure that contains the pixel aspect ratio of the source rectangle. If <i>Enable</i> is <b>FALSE</b>, this parameter can be <b>NULL</b>.


### -param pDestinationAspectRatio [in]

A pointer to a <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure that contains the pixel aspect ratio of the destination rectangle. If <i>Enable</i> is <b>FALSE</b>, this parameter can be <b>NULL</b>.


## -returns



This method does not return a value.




## -remarks



This function can only be called if the driver reports the     <a href="https://msdn.microsoft.com/A40E33D4-E8F3-4348-9135-DD56BABBFA85">D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_PIXEL_ASPECT_RATIO</a>  capability. If this capability is not set, this function will have no effect.

Pixel aspect ratios of the form 0/n and n/0 are not valid.

The default pixel aspect ratio is 1:1 (square pixels).




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>



<a href="https://msdn.microsoft.com/384bdeaa-5360-42af-9f95-b791af2dcafc">Picture Aspect Ratio</a>
 

 

