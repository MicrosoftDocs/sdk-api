---
UID: NF:wincodec.IWICPlanarBitmapFrameEncode.WritePixels
title: IWICPlanarBitmapFrameEncode::WritePixels (wincodec.h)
author: windows-sdk-content
description: Writes lines from the source planes to the encoded format.
old-location: wic\iwicplanarbitmapframeencode_writepixels.htm
tech.root: wic
ms.assetid: 57DB1340-9BE4-46ED-9ADE-9B91657F09B7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICPlanarBitmapFrameEncode interface [Windows Imaging Component],WritePixels method, IWICPlanarBitmapFrameEncode.WritePixels, IWICPlanarBitmapFrameEncode::WritePixels, WritePixels, WritePixels method [Windows Imaging Component], WritePixels method [Windows Imaging Component],IWICPlanarBitmapFrameEncode interface, wic.iwicplanarbitmapframeencode_writepixels, wincodec/IWICPlanarBitmapFrameEncode::WritePixels
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICPlanarBitmapFrameEncode.WritePixels
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICPlanarBitmapFrameEncode::WritePixels


## -description


Writes lines from the source planes to the encoded format.


## -parameters




### -param lineCount

Type: <b>UINT</b>

The number of lines to encode.  See the Remarks section for WIC Jpeg specific line count restrictions.


### -param pPlanes [in]

Type: <b><a href="https://msdn.microsoft.com/4E988284-DE71-48B2-BF77-D616FAA2A3B1">WICBitmapPlane</a>*</b>

Specifies the source buffers for each component plane encoded.  


### -param cPlanes

Type: <b>UINT</b>

The number of component planes specified by the <i>pPlanes</i> parameter.


## -returns



Type: <b>HRESULT</b>

If the planes and source rectangle do not meet the requirements, this method fails with <b>WINCODEC_ERR_IMAGESIZEOUTOFRANGE</b>.

If the <a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a> format does not meet the encoder requirements, this method fails with <b>WINCODEC_ERR_UNSUPPORTEDPIXELFORMAT</b>.





## -remarks



Successive <b>WritePixels</b> calls are assumed sequentially add scanlines to the output image.  <a href="https://msdn.microsoft.com/0EEF6940-627A-4615-90C0-196AAB36843E">IWICBitmapFrameEncode::Initialize</a>, <a href="https://msdn.microsoft.com/e21e1a66-b1fa-4700-a14e-dc382b5404f7">IWICBitmapFrameEncode::SetSize</a> and <a href="https://msdn.microsoft.com/9327b5dd-18a3-40c6-8bb4-245fcc7fb582">IWICBitmapFrameEncode::SetPixelFormat</a> must be called before this method or it will fail.

The interleaved pixel format set via <a href="https://msdn.microsoft.com/9327b5dd-18a3-40c6-8bb4-245fcc7fb582">IWICBitmapFrameEncode::SetPixelFormat</a> and the codec specific encode parameters determine the supported planar formats.


WIC JPEG Encoder:
QueryInterface can be used to obtain this interface from the WIC JPEG <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> implementation.  When using this method to encode Y’CbCr data with the WIC JPEG encoder, chroma subsampling can be configured with encoder options during frame creation.  See the <a href="https://msdn.microsoft.com/e1e3a9d9-209b-46a6-92da-5570476507cf">Encoding Overview</a> and <a href="https://msdn.microsoft.com/1c48f603-e7be-4b0c-a262-0dd01308e868">IWICBitmapEncoder::CreateNewFrame</a> for more details.  
 


Depending upon the configured chroma subsampling, the lineCount parameter has the following restrictions:


<table>
<tr>
<th>Chroma Subsampling</th>
<th>Line Count Restriction</th>
<th>Chroma Plane Width</th>
<th>Chroma  Plane Height</th>
</tr>
<tr>
<td>4:2:0</td>
<td>Multiple of 2, unless the call covers the last scanline of the image</td>
<td>lumaWidth / 2 Rounded up to the nearest integer.</td>
<td>lumaHeight / 2 Rounded up to the nearest integer.</td>
</tr>
<tr>
<td>4:2:2</td>
<td>Any</td>
<td>lumaWidth / 2 Rounded up to the nearest integer.</td>
<td>Any</td>
</tr>
<tr>
<td>4:4:4</td>
<td>Any</td>
<td>Any</td>
<td>Any</td>
</tr>
<tr>
<td>4:4:0</td>
<td>Multiple of 2, unless the call covers the last scanline of the image</td>
<td>Any</td>
<td>llumaHeight / 2 Rounded up to the nearest integer.</td>
</tr>
</table>
 

The full scanline width must be encoded, and the width of the bitmap sources must match their planar configuration.

Additionally, if a pixel format is set via <a href="https://msdn.microsoft.com/9327b5dd-18a3-40c6-8bb4-245fcc7fb582">IWICBitmapFrameEncode::SetPixelFormat</a>, it must be GUID_WICPixelFormat24bppBGR.  



The supported pixel formats of the bitmap sources passed into this method are as follows:


<table>
<tr>
<th>Plane Count</th>
<th>Plane 1</th>
<th>Plane 2</th>
<th>Plane 3</th>
</tr>
<tr>
<td>3</td>
<td>GUID_WICPixelFormat8bppY</td>
<td>GUID_WICPixelFormat8bppCb</td>
<td>GUID_WICPixelFormat8bppCr</td>
</tr>
<tr>
<td>2</td>
<td>GUID_WICPixelFormat8bppY</td>
<td>GUID_WICPixelFormat16bppCbCr</td>
<td>N/A</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e1e3a9d9-209b-46a6-92da-5570476507cf">Encoding Overview</a>



<a href="https://msdn.microsoft.com/1c48f603-e7be-4b0c-a262-0dd01308e868">IWICBitmapEncoder::CreateNewFrame</a>



<a href="https://msdn.microsoft.com/7ACA58CC-E132-4836-B955-322375ADDAA1">IWICPlanarBitmapFrameEncode</a>
 

 

