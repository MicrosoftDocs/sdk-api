---
UID: NL:gdiplusimaging.ImageCodecInfo
title: ImageCodecInfo (gdiplusimaging.h)
description: An ImageCodecInfo object stores information about an image codec (encoder/decoder).
helpviewer_keywords: ["ImageCodecInfo","ImageCodecInfo class [GDI+]","ImageCodecInfo class [GDI+]","described","_gdiplus_CLASS_ImageCodecInfo_Class","gdiplus._gdiplus_CLASS_ImageCodecInfo_Class","gdiplusimaging/ImageCodecInfo"]
old-location: gdiplus\_gdiplus_CLASS_ImageCodecInfo_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imagecodecinfo.htm
ms.date: 12/05/2018
ms.keywords: ImageCodecInfo, ImageCodecInfo class [GDI+], ImageCodecInfo class [GDI+],described, _gdiplus_CLASS_ImageCodecInfo_Class, gdiplus._gdiplus_CLASS_ImageCodecInfo_Class, gdiplusimaging/ImageCodecInfo
req.header: gdiplusimaging.h
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
 - ImageCodecInfo
 - gdiplusimaging/ImageCodecInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.lib
 - Gdiplus.dll
api_name:
 - ImageCodecInfo
---

# ImageCodecInfo class


## -description

An <b>ImageCodecInfo</b> object stores information about an image codec (encoder/decoder). GDI+ provides several built-in image codecs. You can obtain information about those codecs by calling the 
			<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a> function and the 
			<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimagedecoders">GetImageDecoders</a> function. Each of those functions returns an array of <b>ImageCodecInfo</b> objects, one for each available encoder or decoder.

<b>ImageCodecInfo</b> has these types of members:

## -see-also

<a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a>



<a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist">Image::GetEncoderParameterList</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize">Image::GetEncoderParameterListSize</a>



<a href="/windows/desktop/gdiplus/-gdiplus-listing-installed-encoders-use">Listing Installed Encoders</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>