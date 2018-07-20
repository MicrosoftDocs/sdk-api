---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamRotation
title: ID3D11VideoContext::VideoProcessorSetStreamRotation
author: windows-sdk-content
description: Sets the stream rotation for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreamrotation.htm
old-project: medfound
ms.assetid: f94d283c-5eea-4248-8c06-46ef66e86b22
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamRotation method, ID3D11VideoContext.VideoProcessorSetStreamRotation, ID3D11VideoContext::VideoProcessorSetStreamRotation, VideoProcessorSetStreamRotation, VideoProcessorSetStreamRotation method [Media Foundation], VideoProcessorSetStreamRotation method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamRotation, mf.id3d11videocontext_videoprocessorsetstreamrotation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ID3D11VideoContext.VideoProcessorSetStreamRotation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorSetStreamRotation


## -description


Sets the stream rotation for an input stream on the video processor.


## -parameters




### -param pVideoProcessor

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable

Specifies if the stream is to be rotated in a clockwise orientation. 


### -param Rotation

Specifies the rotation of the stream.


## -returns



This method does not return a value.




## -remarks



This is an optional state and the application should only use it if    <a href="https://msdn.microsoft.com/A40E33D4-E8F3-4348-9135-DD56BABBFA85">D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ROTATION</a> is reported in  <a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS.FeatureCaps</a>.

The stream source rectangle will be specified in the pre-rotation coordinates (typically landscape) and the stream destination rectangle will be specified in the post-rotation coordinates (typically portrait).   The application must update the stream destination rectangle correctly when using a rotation value other than 0° and 180°.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

