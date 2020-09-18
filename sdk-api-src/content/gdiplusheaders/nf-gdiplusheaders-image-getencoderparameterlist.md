---
UID: NF:gdiplusheaders.Image.GetEncoderParameterList
title: Image::GetEncoderParameterList (gdiplusheaders.h)
description: The Image::GetEncoderParameterList method gets a list of the parameters supported by a specified image encoder.
helpviewer_keywords: ["GetEncoderParameterList","GetEncoderParameterList method [GDI+]","GetEncoderParameterList method [GDI+]","Image class","Image class [GDI+]","GetEncoderParameterList method","Image.GetEncoderParameterList","Image::GetEncoderParameterList","_gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_","gdiplus._gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getencoderparameterlist.htm
ms.date: 12/05/2018
ms.keywords: GetEncoderParameterList, GetEncoderParameterList method [GDI+], GetEncoderParameterList method [GDI+],Image class, Image class [GDI+],GetEncoderParameterList method, Image.GetEncoderParameterList, Image::GetEncoderParameterList, _gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_, gdiplus._gdiplus_CLASS_Image_GetEncoderParameterList_clsidEncoder_size_buffer_
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
 - Image::GetEncoderParameterList
 - gdiplusheaders/Image::GetEncoderParameterList
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
 - Image.GetEncoderParameterList
---

# Image::GetEncoderParameterList


## -description

The <b>Image::GetEncoderParameterList</b> method gets a list of the parameters supported by a specified image encoder.

## -parameters

### -param clsidEncoder [in]

Type: <b>const CLSID*</b>

Pointer to a 
					<b>CLSID</b> that specifies the encoder.

### -param size [in]

Type: <b>UINT</b>

Integer that specifies the size, in bytes, of the 
					<i>buffer</i> array. Call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize">Image::GetEncoderParameterListSize</a> method to obtain the required size.

### -param buffer [out]

Type: <b><a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a>*</b>

Pointer to an 
					<a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object that receives the list of supported parameters.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

The <b>Image::GetEncoderParameterList</b> method returns an array of 
				<a href="/previous-versions/ms534434(v=vs.85)">EncoderParameter</a> objects. Before you call <b>Image::GetEncoderParameterList</b>, you must allocate a buffer large enough to receive that array, which is part of an 
				<a href="/previous-versions/ms534435(v=vs.85)">EncoderParameters</a> object. You can call the <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize">Image::GetEncoderParameterListSize</a> method to get the size, in bytes, of the required 
				<b>EncoderParameters</b> object.

## -see-also

<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoders">GetImageEncoders</a>



<a href="/windows/desktop/api/gdiplusimagecodec/nf-gdiplusimagecodec-getimageencoderssize">GetImageEncodersSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getencoderparameterlistsize">Image::GetEncoderParameterListSize</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-image-encoders-and-decoders-use">Using Image Encoders and Decoders</a>