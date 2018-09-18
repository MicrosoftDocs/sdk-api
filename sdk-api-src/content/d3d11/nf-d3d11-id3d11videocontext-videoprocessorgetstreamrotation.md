---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamRotation
title: ID3D11VideoContext::VideoProcessorGetStreamRotation
author: windows-sdk-content
description: Gets the stream rotation for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreamrotation.htm
tech.root: medfound
ms.assetid: 6593d829-7f33-408e-aac1-f13e59f7b4bd
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamRotation method, ID3D11VideoContext.VideoProcessorGetStreamRotation, ID3D11VideoContext::VideoProcessorGetStreamRotation, VideoProcessorGetStreamRotation, VideoProcessorGetStreamRotation method [Media Foundation], VideoProcessorGetStreamRotation method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamRotation, mf.id3d11videocontext_videoprocessorgetstreamrotation
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
 - ID3D11VideoContext.VideoProcessorGetStreamRotation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetStreamRotation


## -description


Gets the stream rotation  for an input stream on the video processor.


## -parameters




### -param pVideoProcessor

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pEnable

Specifies if the stream is rotated. 


### -param pRotation

Specifies the rotation of the stream in a clockwise orientation.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

