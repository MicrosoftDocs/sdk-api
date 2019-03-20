---
UID: NF:d3d11_1.ID3D11VideoDevice1.RecommendVideoDecoderDownsampleParameters
title: ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters (d3d11_1.h)
author: windows-sdk-content
description: Allows the driver to recommend optimal output downsample parameters from the input parameters.
old-location: mf\id3d11videodevice1_recommendvideodecoderdownsampleparameters.htm
tech.root: medfound
ms.assetid: DD1C1273-C069-4C46-933F-3450F9DDAFBD
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D11VideoDevice1 interface [Media Foundation],RecommendVideoDecoderDownsampleParameters method, ID3D11VideoDevice1.RecommendVideoDecoderDownsampleParameters, ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters, RecommendVideoDecoderDownsampleParameters, RecommendVideoDecoderDownsampleParameters method [Media Foundation], RecommendVideoDecoderDownsampleParameters method [Media Foundation],ID3D11VideoDevice1 interface, d3d11_1/ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters, mf.id3d11videodevice1_recommendvideodecoderdownsampleparameters
ms.topic: method
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - d3d11_1.h
api_name:
 - ID3D11VideoDevice1.RecommendVideoDecoderDownsampleParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters


## -description


Allows the driver to recommend optimal output downsample parameters from the input parameters.


## -parameters




### -param pInputDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/668D994C-B875-4666-B940-1052A6DE6AA1">D3D11_VIDEO_DECODER_DESC</a>*</b>

A <a href="https://msdn.microsoft.com/668D994C-B875-4666-B940-1052A6DE6AA1">D3D11_VIDEO_DECODER_DESC</a> object describing the decoding profile, the resolution, and format of the input stream.  This is the resolution and format to be downsampled.


### -param InputColorSpace [in]

Type: <b><a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a></b>

A  <a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a> value that specifies the colorspace of the reference frame data.


### -param pInputConfig [in]

Type: <b>const <a href="https://msdn.microsoft.com/AB963FAD-F16C-47F6-8C78-FF4C234FBC60">D3D11_VIDEO_DECODER_CONFIG</a>*</b>

The configuration data associated with the decode profile.


### -param pFrameRate [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/Bb173069(v=VS.85).aspx">DXGI_RATIONAL</a>*</b>

The frame rate of the video content. This is used by the driver to determine whether the video can be decoded in real-time. 


### -param pRecommendedOutputDesc [out]

Type: <b><a href="https://msdn.microsoft.com/3B6BF76A-6566-4C58-AD26-5B13E6D040CA">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/3B6BF76A-6566-4C58-AD26-5B13E6D040CA">D3D11_VIDEO_SAMPLE_DESC</a> structure that the driver populates with the recommended output buffer parameters for a downsample operation. The driver will attempt to recommend parameters that can support real-time decoding. If it is unable to do so, the driver will recommend values that are as close to the real-time solution as possible.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed or this function was called using an invalid calling pattern.</td>
</tr>
</table>
 




## -remarks



You  should call <a href="https://msdn.microsoft.com/9F978BE5-568E-440C-B9B2-0972893FD970">GetVideoDecoderCaps</a> to determine whether decoder downsampling is supported before checking support for a  specific configuration.




## -see-also




<a href="https://msdn.microsoft.com/10E68945-6103-491D-8846-3B7C880FEAFD">ID3D11VideoDevice1</a>
 

 

