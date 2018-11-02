---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputTargetRect
title: ID3D11VideoContext::VideoProcessorGetOutputTargetRect
author: windows-sdk-content
description: Gets the current target rectangle for the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetoutputtargetrect.htm
tech.root: medfound
ms.assetid: 5D59822A-B322-4E79-A543-A89C2232C62F
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputTargetRect method, ID3D11VideoContext.VideoProcessorGetOutputTargetRect, ID3D11VideoContext::VideoProcessorGetOutputTargetRect, VideoProcessorGetOutputTargetRect, VideoProcessorGetOutputTargetRect method [Media Foundation], VideoProcessorGetOutputTargetRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputTargetRect, mf.id3d11videocontext_videoprocessorgetoutputtargetrect
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
 - ID3D11VideoContext.VideoProcessorGetOutputTargetRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetOutputTargetRect


## -description


Gets the current target rectangle for the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param Enabled [out]

Receives the value <b>TRUE</b> if the target rectangle was explicitly set using the <a href="https://msdn.microsoft.com/en-us/library/Hh447752(v=VS.85).aspx">ID3D11VideoContext::VideoProcessorSetOutputTargetRect</a> method. Receives the value FALSE if the target rectangle was disabled or was never set.


### -param pRect [out]

If <i>Enabled</i> receives the value <b>TRUE</b>, this parameter receives the target rectangle. Otherwise, this parameter is ignored.  


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

