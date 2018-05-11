---
UID: NF:wincodec.IWICBitmapFrameEncode.WritePixels
title: IWICBitmapFrameEncode::WritePixels
author: windows-driver-content
description: Copies scan-line data from a caller-supplied buffer to the IWICBitmapFrameEncode object.
old-location: wic\_wic_codec_iwicbitmapframeencode_writepixels.htm
old-project: wic
ms.assetid: 6b430fe0-5230-47dc-95c0-aeabd138cefe
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],WritePixels method, IWICBitmapFrameEncode.WritePixels, IWICBitmapFrameEncode::WritePixels, WritePixels, WritePixels method [Windows Imaging Component], WritePixels method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_writepixels, wic._wic_codec_iwicbitmapframeencode_writepixels, wincodec/IWICBitmapFrameEncode::WritePixels
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICBitmapFrameEncode.WritePixels
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFrameEncode::WritePixels


## -description


Copies scan-line data from a caller-supplied buffer to the <a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a> object.



## -parameters




### -param lineCount [in]

Type: <b>UINT</b>

The number of lines to encode.


### -param cbStride [in]

Type: <b>UINT</b>

The <a href="https://docs.microsoft.com/">stride</a> of the image pixels.


### -param cbBufferSize [in]

Type: <b>UINT</b>

The size of the pixel buffer.


### -param pbPixels [in]

Type: <b>BYTE*</b>

A pointer to the pixel buffer.


## -returns



Type: <b>HRESULT</b>

Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WINCODEC_ERR_CODECTOOMANYSCANLINES</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>lineCount</i> is larger than the number of scan lines in the image.

</td>
</tr>
</table>
 




## -remarks



Successive <b>WritePixels</b> calls are assumed to be sequential scan-line access in the output image.



