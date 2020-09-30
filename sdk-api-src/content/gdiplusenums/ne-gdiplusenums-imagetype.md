---
UID: NE:gdiplusenums.ImageType
title: ImageType (gdiplusenums.h)
description: The ImageType enumeration indicates whether an image is a bitmap or a metafile. The Image::GetType method returns an element of this enumeration.
helpviewer_keywords: ["ImageType","ImageType enumeration [GDI+]","ImageTypeBitmap","ImageTypeMetafile","ImageTypeUnknown","_gdiplus_ENUM_ImageType","gdiplus._gdiplus_ENUM_ImageType","gdiplusenums/ImageType","gdiplusenums/ImageTypeBitmap","gdiplusenums/ImageTypeMetafile","gdiplusenums/ImageTypeUnknown"]
old-location: gdiplus\_gdiplus_ENUM_ImageType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\imagetype.htm
ms.date: 12/05/2018
ms.keywords: ImageType, ImageType enumeration [GDI+], ImageTypeBitmap, ImageTypeMetafile, ImageTypeUnknown, _gdiplus_ENUM_ImageType, gdiplus._gdiplus_ENUM_ImageType, gdiplusenums/ImageType, gdiplusenums/ImageTypeBitmap, gdiplusenums/ImageTypeMetafile, gdiplusenums/ImageTypeUnknown
req.header: gdiplusenums.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - ImageType
 - gdiplusenums/ImageType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - ImageType
---

# ImageType enumeration


## -description

The <b>ImageType</b> enumeration indicates whether an image is a bitmap or a metafile. The 
			<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-gettype">Image::GetType</a> method returns an element of this enumeration.

## -enum-fields

### -field ImageTypeUnknown

Indicates that the image type is not known.

### -field ImageTypeBitmap

Indicates a bitmap image.

### -field ImageTypeMetafile

Indicates a metafile image.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-gettype">Image::GetType</a>