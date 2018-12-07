---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetStreamStereoFormat
title: ID3D11VideoContext::VideoProcessorGetStreamStereoFormat
author: windows-sdk-content
description: Gets the stereo 3D format for an input stream on the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetstreamstereoformat.htm
tech.root: medfound
ms.assetid: FCEE6C95-C631-4268-9B06-686B8AC7D80C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FALSE, ID3D11VideoContext interface [Media Foundation],VideoProcessorGetStreamStereoFormat method, ID3D11VideoContext.VideoProcessorGetStreamStereoFormat, ID3D11VideoContext::VideoProcessorGetStreamStereoFormat, TRUE, VideoProcessorGetStreamStereoFormat, VideoProcessorGetStreamStereoFormat method [Media Foundation], VideoProcessorGetStreamStereoFormat method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetStreamStereoFormat, mf.id3d11videocontext_videoprocessorgetstreamstereoformat
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
 - ID3D11VideoContext.VideoProcessorGetStreamStereoFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorGetStreamStereoFormat


## -description


Gets the stereo 3D format for an input stream on the video processor


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pEnable [out]

Receives the value <b>TRUE</b> if stereo 3D is enabled for this stream, or <b>FALSE</b> otherwise. If the value is <b>FALSE</b>, ignore the remaining parameters.


### -param pFormat [out]

Receives a <a href="https://msdn.microsoft.com/77832DF2-821E-465C-80B6-46DDB2433791">D3D11_VIDEO_PROCESSOR_STEREO_FORMAT</a> value that specifies the layout of the two stereo views in memory.


### -param pLeftViewFrame0 [out]

Receives a Boolean value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Frame 0 contains the left view.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Frame 0 contains the right view.

</td>
</tr>
</table>
 


### -param pBaseViewFrame0 [out]

Receives a Boolean value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Frame 0 contains the base view.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Frame 1 contains the base view.

</td>
</tr>
</table>
 


### -param pFlipMode [out]

Receives a <a href="https://msdn.microsoft.com/2BCC3190-BD27-465D-B9D6-346FAD5E01AF">D3D11_VIDEO_PROCESSOR_STEREO_FLIP_MODE</a> value. This value specifies whether one of the views is flipped.



### -param MonoOffset [out]

Receives the pixel offset used for <b>D3D11_VIDEO_PROCESSOR_STEREO_FORMAT_MONO_OFFSET</b> format. This parameter is ignored for other stereo formats.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

