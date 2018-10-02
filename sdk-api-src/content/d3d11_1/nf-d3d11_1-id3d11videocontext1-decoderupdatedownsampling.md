---
UID: NF:d3d11_1.ID3D11VideoContext1.DecoderUpdateDownsampling
title: ID3D11VideoContext1::DecoderUpdateDownsampling
author: windows-sdk-content
description: Updates the decoder downsampling parameters.
old-location: mf\id3d11videocontext1_decoderupdatedownsampling.htm
tech.root: MedFound
ms.assetid: A55D652B-9295-42E4-9A83-CAC467BEE68E
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: DecoderUpdateDownsampling, DecoderUpdateDownsampling method [Media Foundation], DecoderUpdateDownsampling method [Media Foundation],ID3D11VideoContext1 interface, ID3D11VideoContext1 interface [Media Foundation],DecoderUpdateDownsampling method, ID3D11VideoContext1.DecoderUpdateDownsampling, ID3D11VideoContext1::DecoderUpdateDownsampling, d3d11_1/ID3D11VideoContext1::DecoderUpdateDownsampling, mf.id3d11videocontext1_decoderupdatedownsampling
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
 - ID3D11VideoContext1.DecoderUpdateDownsampling
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext1::DecoderUpdateDownsampling


## -description


Updates the decoder downsampling parameters.


## -parameters




### -param pDecoder [in]

Type: <b>ID3D11VideoDecoder*</b>

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface.


### -param pOutputDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/3B6BF76A-6566-4C58-AD26-5B13E6D040CA">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

The resolution, format, and colorspace of the output/display frames.  This is the destination resolution and format of the downsample operation.


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
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is insufficient memory to complete the operation.</td>
</tr>
</table>
 




## -remarks



This method can only be called after decode downsampling is enabled by calling <a href="https://msdn.microsoft.com/0BE7E6EC-E090-4A13-9D18-108BDBBC211A">DecoderEnableDownsampling</a>. This method is only supported if the <a href="https://msdn.microsoft.com/8E3C86A4-5F73-4E6F-8F93-5564EA0BC113">D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE_DYNAMIC</a> capability is reported.




## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

