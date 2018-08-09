---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputTargetRect
title: ID3D11VideoContext::VideoProcessorGetOutputTargetRect
author: windows-sdk-content
description: Gets the current target rectangle for the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetoutputtargetrect.htm
old-project: medfound
ms.assetid: 5D59822A-B322-4E79-A543-A89C2232C62F
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputTargetRect method, ID3D11VideoContext.VideoProcessorGetOutputTargetRect, ID3D11VideoContext::VideoProcessorGetOutputTargetRect, VideoProcessorGetOutputTargetRect, VideoProcessorGetOutputTargetRect method [Media Foundation], VideoProcessorGetOutputTargetRect method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputTargetRect, mf.id3d11videocontext_videoprocessorgetoutputtargetrect
ms.prod: windows
ms.technology: windows-sdk
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
 - ID3D11VideoContext.VideoProcessorGetOutputTargetRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorGetOutputTargetRect


## -description


Gets the current target rectangle for the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param Enabled [out]

Receives the value <b>TRUE</b> if the target rectangle was explicitly set using the <a href="https://msdn.microsoft.com/D49EED28-E26E-48B5-A050-8EB568A3D31A">ID3D11VideoContext::VideoProcessorSetOutputTargetRect</a> method. Receives the value FALSE if the target rectangle was disabled or was never set.


### -param pRect [out]

If <i>Enabled</i> receives the value <b>TRUE</b>, this parameter receives the target rectangle. Otherwise, this parameter is ignored.  


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

