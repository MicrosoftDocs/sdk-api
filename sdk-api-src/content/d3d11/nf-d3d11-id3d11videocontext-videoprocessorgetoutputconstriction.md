---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputConstriction
title: ID3D11VideoContext::VideoProcessorGetOutputConstriction (d3d11.h)
author: windows-sdk-content
description: Gets the current level of downsampling that is performed by the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetoutputconstriction.htm
tech.root: medfound
ms.assetid: 40F7D380-C385-4C1C-90E5-E362CA54CD41
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputConstriction method, ID3D11VideoContext.VideoProcessorGetOutputConstriction, ID3D11VideoContext::VideoProcessorGetOutputConstriction, VideoProcessorGetOutputConstriction, VideoProcessorGetOutputConstriction method [Media Foundation], VideoProcessorGetOutputConstriction method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputConstriction, mf.id3d11videocontext_videoprocessorgetoutputconstriction
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
 - ID3D11VideoContext.VideoProcessorGetOutputConstriction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::VideoProcessorGetOutputConstriction


## -description


Gets the current level of downsampling that is performed by the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pEnabled [out]

Receives the value <b>TRUE</b> if downsampling was explicitly enabled using the <a href="https://msdn.microsoft.com/EA61A4B8-0853-4F17-B634-70A896DCF5F7">ID3D11VideoContext::VideoProcessorSetOutputConstriction</a> method. Receives the value <b>FALSE</b> if the downsampling was disabled or was never set.


### -param pSize [out]

If <i>Enabled</i> receives the value <b>TRUE</b>, this parameter receives the downsampling size. Otherwise, this parameter is ignored.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

