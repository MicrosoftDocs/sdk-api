---
UID: NF:wincodec.IWICBitmapFrameEncode.SetThumbnail
title: IWICBitmapFrameEncode::SetThumbnail
author: windows-sdk-content
description: Sets the frame thumbnail if supported by the codec.
old-location: wic\_wic_codec_iwicbitmapframeencode_setthumbnail.htm
old-project: wic
ms.assetid: da6924cf-87c0-4774-a02e-5d54be65ef28
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICBitmapFrameEncode interface [Windows Imaging Component],SetThumbnail method, IWICBitmapFrameEncode.SetThumbnail, IWICBitmapFrameEncode::SetThumbnail, SetThumbnail, SetThumbnail method [Windows Imaging Component], SetThumbnail method [Windows Imaging Component],IWICBitmapFrameEncode interface, _wic_codec_iwicbitmapframeencode_setthumbnail, wic._wic_codec_iwicbitmapframeencode_setthumbnail, wincodec/IWICBitmapFrameEncode::SetThumbnail
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICBitmapFrameEncode.SetThumbnail
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapFrameEncode::SetThumbnail


## -description


Sets the frame thumbnail if supported by the codec.


## -parameters




### -param pIThumbnail [in]

Type: <b><a href="https://msdn.microsoft.com/abcc84af-6067-4856-8618-fb66aff4255a">IWICBitmapSource</a>*</b>

The bitmap source to use as the thumbnail.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.
            

Returns WINCODEC_ERR_UNSUPPORTEDOPERATION if the feature is not supported by the encoder.




## -remarks



We recommend that you call
			   <b>SetThumbnail</b> before calling <a href="https://msdn.microsoft.com/6b430fe0-5230-47dc-95c0-aeabd138cefe">WritePixels</a> or <a href="https://msdn.microsoft.com/bc748982-6dc8-41cc-a23b-9d127dc22a1f">WriteSource</a>.
				The thumbnail won't be added to the encoded file if <b>SetThumbnail</b> is called after a call to <b>WritePixels</b> or <b>WriteSource</b>.
			

<ul>
<li><b>BMP, PNG</b>Setting thumbnails is unsupported. This function will return <b>WINCODEC_ERR_UNSUPPORTEDOPERATION</b>.

</li>
<li><b>JPEG</b>Setting the thumbnail is supported. The source image will be re-encoded as either an 8bpp or 24bpp JPEG and will be written to the JPEG’s APP1 metadata block.


</li>
<li><b>TIFF</b> Setting the thumbnail is supported. The source image will be re-encoded as a TIFF and will be written to the frame’s SubIFD block.

</li>
<li><b>JPEG-XR</b>Setting the thumbnail is supported. The source image will be re-encoded as an additional 8bpp or 24bpp frame.


</li>
</ul>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/e1e3a9d9-209b-46a6-92da-5570476507cf">Encoding Overview</a>



<a href="https://msdn.microsoft.com/58f03dc2-cc31-4d76-b75a-f332da1f900f">How to Write a WIC-Enabled CODEC</a>



<a href="https://msdn.microsoft.com/a8de774b-3783-46be-9a21-c9fec2f10ffd">IWICBitmapFrameEncode</a>
 

 

