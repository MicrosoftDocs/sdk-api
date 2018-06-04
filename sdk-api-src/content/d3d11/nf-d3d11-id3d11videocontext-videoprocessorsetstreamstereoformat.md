---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ID3D11VideoContext::VideoProcessorSetStreamStereoFormat


## -description


Enables or disables stereo 3D video for an input stream on the video processor. In addition, this method specifies the layout of the video frames in memory.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param Enable [in]

Specifies whether stereo 3D is enabled for this stream. If the value is <b>FALSE</b>, the remaining parameters of this method are ignored.


### -param Format [in]

Specifies the layout of the two stereo views in memory, as a <a href="https://msdn.microsoft.com/77832DF2-821E-465C-80B6-46DDB2433791">D3D11_VIDEO_PROCESSOR_STEREO_FORMAT</a> value.


### -param LeftViewFrame0 [in]

If <b>TRUE</b>, frame 0 contains the left view. Otherwise, frame 0 contains the right view. 

This parameter is ignored for the following stereo formats:

<ul>
<li><b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO </b></li>
<li><b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b></li>
</ul>

### -param BaseViewFrame0 [in]

If <b>TRUE</b>, frame 0 contains the base view. Otherwise, frame 1 contains the base view.

This parameter is ignored for the following stereo formats:

<ul>
<li><b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO </b></li>
<li><b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b></li>
<li>When <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_SEPARATE</b> is used and the application wants to convert the stereo data to mono, it can either:<ul>
<li>Specify the base view as a mono input.</li>
<li>Specify both resources and allow the driver to do the conversion from the base view.  In this case, <a href="https://msdn.microsoft.com/B861D00B-2FF2-4F8F-AD40-0EE6A9706A0C">D3D11_VIDEO_PROCESSOR_STREAM.hInputSurface</a> is considered frame 0 and <b>D3D11_VIDEO_PROCESSOR_STREAM.hInputSurfaceRight</b> is considered frame 1.</li>
</ul>
</li>
</ul>

### -param FlipMode [in]

A flag from the  <a href="https://msdn.microsoft.com/2BCC3190-BD27-465D-B9D6-346FAD5E01AF">D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE</a> enumeration, specifying whether one of the views is flipped.


### -param MonoOffset [in]

For <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b> format, this parameter specifies how to generate the left and right views:  

<ul>
<li>If <i>MonoOffset</i> is positive, the right view is shifted to the right by that many pixels, and the left view is shifted to the left by the same amount. </li>
<li>If <i>MonoOffset</i> is negative, the right view is shifted to the left by that many pixels, and the left view is shifted to right by the same amount.</li>
</ul>
If <i>Format</i> is not <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b>, this parameter must be zero.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

