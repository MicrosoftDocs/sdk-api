---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputAlphaFillMode
title: ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode
author: windows-sdk-content
description: Sets the alpha fill mode for data that the video processor writes to the render target.
old-location: mf\id3d11videocontext_videoprocessorsetoutputalphafillmode.htm
tech.root: medfound
ms.assetid: 898604FA-B857-4D84-AA0D-3BC517F75A36
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputAlphaFillMode method, ID3D11VideoContext.VideoProcessorSetOutputAlphaFillMode, ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode, VideoProcessorSetOutputAlphaFillMode, VideoProcessorSetOutputAlphaFillMode method [Media Foundation], VideoProcessorSetOutputAlphaFillMode method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode, mf.id3d11videocontext_videoprocessorsetoutputalphafillmode
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
 - ID3D11VideoContext.VideoProcessorSetOutputAlphaFillMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode


## -description


Sets the alpha fill mode for data that the video processor writes to the render target.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param AlphaFillMode [in]

The alpha fill mode, specified as a <a href="https://msdn.microsoft.com/185B71C5-1B27-4F7B-B842-CA04898F5DC1">D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE</a> value.


### -param StreamIndex [in]

The zero-based index of an input stream. This parameter is used if <i>AlphaFillMode</i> is <b>D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_SOURCE_STREAM</b>. Otherwise, the parameter is ignored.


## -returns



This method does not return a value.




## -remarks



To find out which fill modes the device supports, call the <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> method. If the driver reports the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_FILL</b> capability, the driver supports all of the fill modes. Otherwise, the <i>AlphaFillMode</i> parameter must be <b>D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_OPAQUE</b>.



The default fill mode is <b>D3D11_VIDEO_PROCESSOR_ALPHA_FILL_MODE_OPAQUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

