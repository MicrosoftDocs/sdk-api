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
 

 

