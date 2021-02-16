---
UID: NF:gdiplusheaders.Image.GetRawFormat
title: Image::GetRawFormat (gdiplusheaders.h)
description: The Image::GetRawFormat method gets a globally unique identifier ( GUID) that identifies the format of this Image object. GUIDs that identify various file formats are defined in Gdiplusimaging.h.
helpviewer_keywords: ["GetRawFormat","GetRawFormat method [GDI+]","GetRawFormat method [GDI+]","Image class","Image class [GDI+]","GetRawFormat method","Image.GetRawFormat","Image::GetRawFormat","_gdiplus_CLASS_Image_GetRawFormat_format_","gdiplus._gdiplus_CLASS_Image_GetRawFormat_format_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetRawFormat_format_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getrawformat.htm
ms.date: 12/05/2018
ms.keywords: GetRawFormat, GetRawFormat method [GDI+], GetRawFormat method [GDI+],Image class, Image class [GDI+],GetRawFormat method, Image.GetRawFormat, Image::GetRawFormat, _gdiplus_CLASS_Image_GetRawFormat_format_, gdiplus._gdiplus_CLASS_Image_GetRawFormat_format_
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
 - Image::GetRawFormat
 - gdiplusheaders/Image::GetRawFormat
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
 - Image.GetRawFormat
---

# Image::GetRawFormat


## -description

The <b>Image::GetRawFormat</b> method gets a globally unique identifier (			GUID) that identifies the format of this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object. 
			GUIDs that identify various file formats are defined in Gdiplusimaging.h.

## -parameters

### -param format [out]

Type: <b>GUID*</b>

Pointer to a 
					GUID that receives the format identifier.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-gettype">Image::GetType</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-imagetype">ImageType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>