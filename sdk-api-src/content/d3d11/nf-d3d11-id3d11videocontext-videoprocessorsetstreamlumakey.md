---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamLumaKey
title: ID3D11VideoContext::VideoProcessorSetStreamLumaKey (d3d11.h)
author: windows-sdk-content
description: Sets the luma key for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreamlumakey.htm
tech.root: medfound
ms.assetid: DAFDAF7C-BBE2-41AA-9E44-C1BD28CE03FE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamLumaKey method, ID3D11VideoContext.VideoProcessorSetStreamLumaKey, ID3D11VideoContext::VideoProcessorSetStreamLumaKey, VideoProcessorSetStreamLumaKey, VideoProcessorSetStreamLumaKey method [Media Foundation], VideoProcessorSetStreamLumaKey method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamLumaKey, mf.id3d11videocontext_videoprocessorsetstreamlumakey
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
 - ID3D11VideoContext.VideoProcessorSetStreamLumaKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetStreamLumaKey


## -description


Sets the luma key for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable [in]

Specifies whether luma keying is enabled.


### -param Lower [in]

The lower bound for the luma key. The valid range is [0…1]. If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored.


### -param Upper [in]

The upper bound for the luma key. The valid range is [0…1]. If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored.


## -returns



This method does not return a value.




## -remarks



To use this feature, the driver must support luma keying, indicated by the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_LUMA_KEY</b> capability flag. To query for this capability, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>. In addition, if the input format is RGB, the device must support the <b>D3D11_VIDEO_PROCESSOR_FORMAT_CAPS_RGB_LUMA_KEY</b> capability.

The values of <i>Lower</i> and <i>Upper</i> give the lower and upper bounds of the luma key, using a nominal range of [0...1]. Given a format with <i>n</i> bits per channel, these values are converted to luma values as follows:

<code>val = f * ((1 &lt;&lt; n)-1)</code>

Any pixel whose luma value falls within the upper and lower bounds (inclusive) is treated as transparent.

For example, if the pixel format uses 8-bit luma, the upper bound is calculated as follows:

<code>BYTE Y = BYTE(max(min(1.0, Upper), 0.0) * 255.0)</code>

Note that the value is clamped to the range [0...1] before multiplying by 255.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

