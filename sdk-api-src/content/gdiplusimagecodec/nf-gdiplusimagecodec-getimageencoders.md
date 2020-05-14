---
UID: NF:gdiplusimagecodec.GetImageEncoders
title: GetImageEncoders function (gdiplusimagecodec.h)
description: The GetImageEncoders function gets an array of ImageCodecInfo objects that contain information about the available image encoders.helpviewer_keywords: ["GetImageEncoders","GetImageEncoders function [GDI+]","_gdiplus_FUNC_GetImageEncoders_numEncoders_size_encoders_","gdiplus._gdiplus_FUNC_GetImageEncoders_numEncoders_size_encoders_","gdiplusimagecodec/GetImageEncoders"]
old-location: gdiplus\_gdiplus_FUNC_GetImageEncoders_numEncoders_size_encoders_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimageencoders.htm
ms.date: 12/05/2018
ms.keywords: GetImageEncoders, GetImageEncoders function [GDI+], _gdiplus_FUNC_GetImageEncoders_numEncoders_size_encoders_, gdiplus._gdiplus_FUNC_GetImageEncoders_numEncoders_size_encoders_, gdiplusimagecodec/GetImageEncoders
f1_keywords:
- gdiplusimagecodec/GetImageEncoders
dev_langs:
- c++
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
- GetImageEncoders
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# GetImageEncoders function


## -description


The <b>GetImageEncoders</b> function gets an array of 
			<a href="https://docs.microsoft.com/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a> objects that contain information about the available image encoders.


## -parameters




### -param numEncoders [in]

Type: <b>UINT</b>

Integer that specifies the number of available image encoders. Call <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a> to determine this number. 


### -param size [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the array of 
					<a href="https://docs.microsoft.com/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a> objects. Call <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a> to determine this number. 


### -param encoders [out]

Type: <b><a href="https://docs.microsoft.com/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a>*</b>

Pointer to a buffer that receives the array of 
					<a href="https://docs.microsoft.com/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a> objects. You must allocate memory for this buffer. Call <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a> to determine the size of the required buffer. 


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders">GetImageDecoders</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize">GetImageDecodersSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>
 

 

