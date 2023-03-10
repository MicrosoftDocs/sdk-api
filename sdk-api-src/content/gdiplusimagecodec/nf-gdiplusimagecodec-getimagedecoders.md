---
UID: NF:gdiplusimagecodec.GetImageDecoders
title: GetImageDecoders function (gdiplusimagecodec.h)
description: The GetImageDecoders function gets an array of ImageCodecInfo objects that contain information about the available image decoders.
helpviewer_keywords: ["GetImageDecoders","GetImageDecoders function [GDI+]","_gdiplus_FUNC_GetImageDecoders_numDecoders_size_decoders_","gdiplus._gdiplus_FUNC_GetImageDecoders_numDecoders_size_decoders_","gdiplusimagecodec/GetImageDecoders"]
old-location: gdiplus\_gdiplus_FUNC_GetImageDecoders_numDecoders_size_decoders_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\getimagedecoders.htm
ms.date: 12/05/2018
ms.keywords: GetImageDecoders, GetImageDecoders function [GDI+], _gdiplus_FUNC_GetImageDecoders_numDecoders_size_decoders_, gdiplus._gdiplus_FUNC_GetImageDecoders_numDecoders_size_decoders_, gdiplusimagecodec/GetImageDecoders
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - GetImageDecoders
 - gdiplusimagecodec/GetImageDecoders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - GetImageDecoders
---

# GetImageDecoders function


## -description

The <b>GetImageDecoders</b> function gets an array of <a href="/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a> objects that contain information about the available image decoders.

## -parameters

### -param numDecoders [in]

Type: <b>UINT</b>

Integer that specifies the number of available image decoders. Call <a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize">GetImageDecodersSize</a> to determine this number.

### -param size [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the array of 
					<a href="/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a> objects. Call <a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize">GetImageDecodersSize</a> to determine this number.

### -param decoders [out]

Type: <b><a href="/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a>*</b>

Pointer to a buffer that receives the array of 
					<a href="/previous-versions/ms534466(v=vs.85)">ImageCodecInfo</a> objects. You must allocate memory for this buffer. Call <a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize">GetImageDecodersSize</a> to determine the size of the required buffer.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoderssize">GetImageDecodersSize</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-metafile">Metafile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>