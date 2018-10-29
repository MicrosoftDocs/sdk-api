---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputAlphaFillMode
title: ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode
author: windows-sdk-content
description: Gets the current alpha fill mode for the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetoutputalphafillmode.htm
tech.root: medfound
ms.assetid: 23F37D9C-3D33-4A07-AC54-5273A09BF540
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputAlphaFillMode method, ID3D11VideoContext.VideoProcessorGetOutputAlphaFillMode, ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode, VideoProcessorGetOutputAlphaFillMode, VideoProcessorGetOutputAlphaFillMode method [Media Foundation], VideoProcessorGetOutputAlphaFillMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode, mf.id3d11videocontext_videoprocessorgetoutputalphafillmode
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
 - ID3D11VideoContext.VideoProcessorGetOutputAlphaFillMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetOutputAlphaFillMode


## -description


Gets the current alpha fill mode for the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pAlphaFillMode [out]

Receives the alpha fill mode, as a <a href="https://msdn.microsoft.com/185B71C5-1B27-4F7B-B842-CA04898F5DC1">D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE</a> value.


### -param pStreamIndex [out]

If the alpha fill mode is <b>D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_SOURCE_STREAM</b>, this parameter receives the zero-based index of an input stream. The input stream provides the alpha values for the alpha fill.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

