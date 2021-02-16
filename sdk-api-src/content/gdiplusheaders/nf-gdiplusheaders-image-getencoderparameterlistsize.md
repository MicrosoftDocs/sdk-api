---
UID: NF:gdiplusheaders.Image.GetEncoderParameterListSize
title: Image::GetEncoderParameterListSize (gdiplusheaders.h)
description: The Image::GetEncoderParameterListSize method gets the size, in bytes, of the parameter list for a specified image encoder.
helpviewer_keywords: ["GetEncoderParameterListSize","GetEncoderParameterListSize method [GDI+]","GetEncoderParameterListSize method [GDI+]","Image class","Image class [GDI+]","GetEncoderParameterListSize method","Image.GetEncoderParameterListSize","Image::GetEncoderParameterListSize","_gdiplus_CLASS_Image_GetEncoderParameterListSize_clsidEncoder_","gdiplus._gdiplus_CLASS_Image_GetEncoderParameterListSize_clsidEncoder_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetEncoderParameterListSize_clsidEncoder_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getencoderparameterlistsize.htm
ms.date: 12/05/2018
ms.keywords: GetEncoderParameterListSize, GetEncoderParameterListSize method [GDI+], GetEncoderParameterListSize method [GDI+],Image class, Image class [GDI+],GetEncoderParameterListSize method, Image.GetEncoderParameterListSize, Image::GetEncoderParameterListSize, _gdiplus_CLASS_Image_GetEncoderParameterListSize_clsidEncoder_, gdiplus._gdiplus_CLASS_Image_GetEncoderParameterListSize_clsidEncoder_
req.header: gdiplusheaders.h
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
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Image::GetEncoderParameterListSize
 - gdiplusheaders/Image::GetEncoderParameterListSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.GetEncoderParameterListSize
---

# Image::GetEncoderParameterListSize


## -description

The <b>Image::GetEncoderParameterListSize</b> method gets the size, in bytes, of the parameter list for a specified image encoder.

## -parameters

### -param clsidEncoder [in]

Type: <b>const CLSID*</b>

Pointer to a 
					<b>CLSID</b> that specifies the encoder.

## -returns

Type: <b>UINT</b>

This method returns the size, in bytes, of the parameter list.

## -remarks

The <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist">Image::GetEncoderParameterList</a> method returns an array of 
				<a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a> objects. Before you call <b>Image::GetEncoderParameterList</b>, you must allocate a buffer large enough to receive that array, which is part of an 
				<a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object. You can call the <b>Image::GetEncoderParameterListSize</b> method to get the size, in bytes, of the required 
				<b>EncoderParameters</b> object.

## -see-also

<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlist">Image::GetEncoderParameterList</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>