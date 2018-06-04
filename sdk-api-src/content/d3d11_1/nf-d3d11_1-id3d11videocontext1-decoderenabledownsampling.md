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

# ID3D11VideoContext1::DecoderEnableDownsampling


## -description


Indicates that decoder downsampling will be used and that the driver should allocate the appropriate reference frames.  


## -parameters




### -param pDecoder [in]

Type: <b>ID3D11VideoDecoder*</b>

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface.


### -param InputColorSpace [in]

Type: <b>DXGI_COLOR_SPACE_TYPE</b>

The color space information of the reference frame data.


### -param pOutputDesc [in]

Type: <b>const <a href="https://msdn.microsoft.com/3B6BF76A-6566-4C58-AD26-5B13E6D040CA">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

The resolution, format, and colorspace of the output/display frames.  This is the destination resolution and format of the downsample operation.


### -param ReferenceFrameCount [in]

Type: <b>UINT</b>

The number of reference frames to be used in the operation.


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



This function can only be called once for a specific <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. This method must be called prior to the first call to <a href="https://msdn.microsoft.com/395B06D8-1BCF-44F2-9F69-A183C30E36B7">DecoderBeginFrame</a>. To update the downsampling parameters, use <a href="https://msdn.microsoft.com/A55D652B-9295-42E4-9A83-CAC467BEE68E">DecoderUpdateDownsampling</a>.




## -see-also




<a href="https://msdn.microsoft.com/64D12F68-C2AA-4C1D-9608-5F97CF7AD430">ID3D11VideoContext1</a>
 

 

