---
UID: NF:gdiplusimagecodec.GetImageDecodersSize
title: GetImageDecodersSize function (gdiplusimagecodec.h)
author: windows-sdk-content
description: The GetImageDecodersSize function gets the number of available image decoders and the total size of the array of ImageCodecInfo objects that is returned by the GetImageDecoders function.
old-location: gdiplus\_gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimagedecoderssize.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetImageDecodersSize, GetImageDecodersSize function [GDI+], _gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_, gdiplus._gdiplus_FUNC_GetImageDecodersSize_numDecoders_size_, gdiplusimagecodec/GetImageDecodersSize
ms.topic: function
f1_keywords: ["gdiplusimagecodec/GetImageDecodersSize"]
req.header: gdiplusimagecodec.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - GetImageDecodersSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GetImageDecodersSize function


## -description


The <b>GetImageDecodersSize</b> function gets the number of available image decoders and the total size of the array of 
			<a href="https://docs.microsoft.com/previous-versions//ms534466(v=vs.85)">ImageCodecInfo</a> objects that is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders">GetImageDecoders</a> function.


## -parameters




### -param numDecoders [out]

Type: <b>UINT*</b>

Pointer to a <b>UINT</b> that receives the number of available image decoders.


### -param size [out]

Type: <b>UINT*</b>

Pointer to a 
					<b>UINT</b> that receives the total size, in bytes, of the array of 
					<a href="https://docs.microsoft.com/previous-versions//ms534466(v=vs.85)">ImageCodecInfo</a> objects that is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders">GetImageDecoders</a> function. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders">GetImageDecoders</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>
 

 

