---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputStereoMode
title: ID3D11VideoContext::VideoProcessorGetOutputStereoMode
author: windows-sdk-content
description: Queries whether the video processor produces stereo video frames.
old-location: mf\id3d11videocontext_videoprocessorgetoutputstereomode.htm
tech.root: medfound
ms.assetid: E7BDB9DA-2760-416D-BD51-F73A035B790A
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputStereoMode method, ID3D11VideoContext.VideoProcessorGetOutputStereoMode, ID3D11VideoContext::VideoProcessorGetOutputStereoMode, VideoProcessorGetOutputStereoMode, VideoProcessorGetOutputStereoMode method [Media Foundation], VideoProcessorGetOutputStereoMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputStereoMode, mf.id3d11videocontext_videoprocessorgetoutputstereomode
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
 - ID3D11VideoContext.VideoProcessorGetOutputStereoMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetOutputStereoMode


## -description


Queries whether the video processor produces stereo video frames.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pEnabled [out]

Receives the value <b>TRUE</b> if stereo output is enabled, or <b>FALSE</b> otherwise.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

