---
UID: NF:wincodec.IWICBitmapFrameEncode.SetPixelFormat
title: IWICBitmapFrameEncode::SetPixelFormat (wincodec.h)
author: windows-sdk-content
description: Requests that the encoder use the specified pixel format.
old-location: wic\_wic_codec_iwicbitmapframeencode_setpixelformat.htm
tech.root: wic
ms.assetid: 9327b5dd-18a3-40c6-8bb4-245fcc7fb582
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetPixelFormat method, IWICBitmapFrameEncode.SetPixelFormat, IWICBitmapFrameEncode::SetPixelFormat, SetPixelFormat, SetPixelFormat method [Windows Imaging Component], SetPixelFormat method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setpixelformat, wic._wic_codec_iwicbitmapframeencode_setpixelformat, wincodec/IWICBitmapFrameEncode::SetPixelFormat
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IWICBitmapFrameEncode.SetPixelFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWICBitmapFrameEncode::SetPixelFormat


## -description


Requests that the encoder use the specified pixel format.


## -parameters




### -param pPixelFormat [in, out]

Type: <b>WICPixelFormatGUID*</b>

On input, the requested pixel format GUID. On output, the closest pixel format GUID supported by the encoder; this may be different than the requested format. For a list of pixel format GUIDs, see <a href="https://msdn.microsoft.com/348b6d15-e339-4dce-99f3-4d639ee9bf7d">Native Pixel Formats</a>.


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
<dt><b>WINCODEC_ERR_WRONGSTATE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/ec215e32-b4bd-469a-903d-f5b546185183">IWICBitmapFrameEncode::Initialize</a> method was not called.

</td>
</tr>
</table>
 




## -remarks



The encoder might not support the requested pixel format. If not, <b>SetPixelFormat</b> returns the closest match in the memory block that <i>pPixelFormat</i> points to. If the returned pixel format doesn't match the requested format, you must use an <a href="https://msdn.microsoft.com/d558aaa7-5962-424c-9e83-363fba09ad50">IWICFormatConverter</a> object to convert the pixel data.




## -see-also




<a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>



<a href="https://msdn.microsoft.com/348b6d15-e339-4dce-99f3-4d639ee9bf7d">Native Pixel Formats</a>
 

 

