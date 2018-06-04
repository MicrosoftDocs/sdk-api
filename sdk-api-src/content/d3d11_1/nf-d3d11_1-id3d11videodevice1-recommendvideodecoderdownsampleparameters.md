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

Type: <b>const <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a>*</b>

The frame rate of the video content. This is used by the driver to determine whether the video can be decoded in real-time. 


### -param pRecommendedOutputDesc [out]

Type: <b><a href="https://msdn.microsoft.com/3B6BF76A-6566-4C58-AD26-5B13E6D040CA">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/3B6BF76A-6566-4C58-AD26-5B13E6D040CA">D3D11_VIDEO_SAMPLE_DESC</a> structure that the driver populates with the recommended output buffer parameters for a downsample operation. The driver will attempt to recommend parameters that can support real-time decoding. If it is unable to do so, the driver will recommend values that are as close to the real-time solution as possible.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

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
 

 

