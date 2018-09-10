---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamAlpha
title: ID3D11VideoContext::VideoProcessorSetStreamAlpha
author: windows-sdk-content
description: Sets the planar alpha for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorsetstreamalpha.htm
tech.root: medfound
ms.assetid: DA869E3F-25BB-4794-B7AE-A3C2DA968800
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamAlpha method, ID3D11VideoContext.VideoProcessorSetStreamAlpha, ID3D11VideoContext::VideoProcessorSetStreamAlpha, VideoProcessorSetStreamAlpha, VideoProcessorSetStreamAlpha method [Media Foundation], VideoProcessorSetStreamAlpha method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamAlpha, mf.id3d11videocontext_videoprocessorsetstreamalpha
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
 - ID3D11VideoContext.VideoProcessorSetStreamAlpha
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetStreamAlpha


## -description


Sets the planar alpha for an input stream on the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable [in]

Specifies whether alpha blending is enabled.


### -param Alpha [in]

The planar alpha value. The value can range from 0.0 (transparent) to 1.0 (opaque). 
 If <i>Enable</i> is <b>FALSE</b>, this parameter is ignored.


## -returns



This method does not return a value.




## -remarks



To use this feature, the driver must support stereo video, indicated by the  <a href="https://msdn.microsoft.com/en-us/library/Hh447650(v=VS.85).aspx">D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALHPA_STREAM</a> capability flag. To query for this  capability, call <a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a>.

Alpha blending is disabled by default. 
        

For each pixel, the destination color value is computed as follows:

<code>Cd = Cs * (As * Ap * Ae) + Cd * (1.0 - As * Ap * Ae)</code>

where:

<ul>
<li><code>Cd</code> = The color value of the destination pixel</li>
<li><code>Cs</code> = The color value of the source pixel</li>
<li><code>As</code> = The per-pixel source alpha</li>
<li><code>Ap</code> = The planar alpha value</li>
<li><code>Ae</code> = The palette-entry alpha value, or 1.0 (see Note)</li>
</ul>
<div class="alert"><b>Note</b>  Palette-entry alpha values apply only to palettized color formats, and only when the device supports the <b>D3D11_VIDEO_PROCESSOR_FEATURE_CAPS_ALPHA_PALETTE</b> capability. Otherwise, this factor equals 1.0. </div>
<div> </div>
The destination alpha value is computed according to the alpha fill mode. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Hh447746(v=VS.85).aspx">ID3D11VideoContext::VideoProcessorSetOutputAlphaFillMode</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

