---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputTargetRect
title: ID3D11VideoContext::VideoProcessorSetOutputTargetRect (d3d11.h)
author: windows-sdk-content
description: Sets the target rectangle for the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetoutputtargetrect.htm
tech.root: medfound
ms.assetid: D49EED28-E26E-48B5-A050-8EB568A3D31A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputTargetRect method, ID3D11VideoContext.VideoProcessorSetOutputTargetRect, ID3D11VideoContext::VideoProcessorSetOutputTargetRect, VideoProcessorSetOutputTargetRect, VideoProcessorSetOutputTargetRect method [Media Foundation], VideoProcessorSetOutputTargetRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputTargetRect, mf.id3d11videocontext_videoprocessorsetoutputtargetrect
ms.topic: method
f1_keywords: 
 - "d3d11/ID3D11VideoContext.VideoProcessorSetOutputTargetRect"
dev_langs:
 - c++
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
 - ID3D11VideoContext.VideoProcessorSetOutputTargetRect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::VideoProcessorSetOutputTargetRect


## -description


Sets the target rectangle for the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param Enable [in]

Specifies whether to apply the target rectangle.


### -param pRect [in]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162897(v=vs.85)">RECT</a> structure that specifies the target rectangle.  If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored.


## -returns



This method does not return a value.




## -remarks



The target rectangle is the area within the destination surface where the output will be drawn. The target rectangle is given in pixel coordinates, relative to the destination surface.

If this method is never called, or if the <i>Enable</i> parameter is <b>FALSE</b>, the video processor writes to the entire destination surface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

