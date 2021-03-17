---
UID: NL:gdiplusheaders.Image
title: Image (gdiplusheaders.h)
description: The Image class provides methods for loading and saving raster images (bitmaps) and vector images (metafiles).
helpviewer_keywords: ["Image","Image class [GDI+]","Image class [GDI+]","described","_gdiplus_CLASS_Image_Class","gdiplus._gdiplus_CLASS_Image_Class","gdiplusheaders/Image"]
old-location: gdiplus\_gdiplus_CLASS_Image_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\image.htm
ms.date: 12/05/2018
ms.keywords: Image, Image class [GDI+], Image class [GDI+],described, _gdiplus_CLASS_Image_Class, gdiplus._gdiplus_CLASS_Image_Class, gdiplusheaders/Image
req.header: gdiplusheaders.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Image
 - gdiplusheaders/Image
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Image
---

# Image class


## -description

The <a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-image(gpimage_status)">Image</a> class provides methods for loading and saving raster images (bitmaps) and vector images (metafiles). An Image object encapsulates a bitmap or a metafile and stores attributes that you can retrieve by calling various Get methods. You can construct Image objects from a variety of file types including BMP, ICON, GIF, JPEG, Exif, PNG, TIFF, WMF, and EMF.