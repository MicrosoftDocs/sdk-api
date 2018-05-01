---
UID: NF:d3d11_1.ID3D11VideoDevice1.CheckVideoDecoderDownsampling
title: ID3D11VideoDevice1::CheckVideoDecoderDownsampling method
author: windows-driver-content
description: Indicates whether the video decoder supports downsampling with the specified input format, and whether real-time downsampling is supported.
old-location: mf\id3d11videodevice1_checkvideodecoderdownsampling.htm
old-project: medfound
ms.assetid: EB05C2F7-AC7A-42BD-A661-5101641A920C
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: CheckVideoDecoderDownsampling method [Media Foundation], CheckVideoDecoderDownsampling method [Media Foundation], ID3D11VideoDevice1 interface, CheckVideoDecoderDownsampling,ID3D11VideoDevice1.CheckVideoDecoderDownsampling, ID3D11VideoDevice1, ID3D11VideoDevice1 interface [Media Foundation], CheckVideoDecoderDownsampling method, ID3D11VideoDevice1::CheckVideoDecoderDownsampling, d3d11_1/ID3D11VideoDevice1::CheckVideoDecoderDownsampling, mf.id3d11videodevice1_checkvideodecoderdownsampling
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: D3D11_VIDEO_PROCESSOR_BEHAVIOR_HINTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11_1.h
api_name:
-	ID3D11VideoDevice1.CheckVideoDecoderDownsampling
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoDevice1::CheckVideoDecoderDownsampling method


## -description


Indicates whether the video decoder supports downsampling with the specified input format, and whether real-time downsampling is supported.


## -parameters




### -param pInputDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/668D994C-B875-4666-B940-1052A6DE6AA1">D3D11_VIDEO_DECODER_DESC</a>*</b>

An object describing the decoding profile, the resolution, and format of the input stream.  This is the resolution and format to be downsampled.


### -param InputColorSpace [in]

Type: <b><a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a></b>

A  <a href="https://msdn.microsoft.com/E25C933F-0DB3-4BC4-9755-9361B2B9B9CB">DXGI_COLOR_SPACE_TYPE</a> value that specifies the colorspace of the reference frame data.


### -param pInputConfig [in]

Type: <b>const <a href="https://msdn.microsoft.com/AB963FAD-F16C-47F6-8C78-FF4C234FBC60">D3D11_VIDEO_DECODER_CONFIG</a>*</b>

The configuration data associated with the decode profile.


### -param pFrameRate [in]

Type: <b>const <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a>*</b>

The frame rate of the video content. This is used by the driver to determine whether the video can be decoded in real-time. 


### -param pOutputDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/3B6BF76A-6566-4C58-AD26-5B13E6D040CA">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

An object describing the resolution, format, and colorspace of the output frames.  This is the destination resolution and format of the downsample operation.


### -param pSupported [out]

Type: <b>BOOL*</b>

Pointer to a boolean value set by the driver that indicates if downsampling is supported with the specified input data. True if the driver supports the requested downsampling;  otherwise, false.


### -param pRealTimeHint [out]

Type: <b>BOOL*</b>

Pointer to a boolean value set by the driver that indicates if real-time decoding is supported with the specified input data. True if the driver supports the requested real-time decoding;  otherwise, false. Note that the returned value is based on the current configuration of the video decoder and does not guarantee that real-time decoding will be supported for future downsampling operations.


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
 

 

