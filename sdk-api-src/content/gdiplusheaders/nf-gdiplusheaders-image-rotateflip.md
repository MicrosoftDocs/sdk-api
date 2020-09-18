---
UID: NF:gdiplusheaders.Image.RotateFlip
title: Image::RotateFlip (gdiplusheaders.h)
description: The Image::RotateFlip method rotates and flips this image.
helpviewer_keywords: ["Image class [GDI+]","RotateFlip method","Image.RotateFlip","Image::RotateFlip","RotateFlip","RotateFlip method [GDI+]","RotateFlip method [GDI+]","Image class","_gdiplus_CLASS_Image_RotateFlip_rotateFlipType_","gdiplus._gdiplus_CLASS_Image_RotateFlip_rotateFlipType_"]
old-location: gdiplus\_gdiplus_CLASS_Image_RotateFlip_rotateFlipType_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\rotateflip.htm
ms.date: 12/05/2018
ms.keywords: Image class [GDI+],RotateFlip method, Image.RotateFlip, Image::RotateFlip, RotateFlip, RotateFlip method [GDI+], RotateFlip method [GDI+],Image class, _gdiplus_CLASS_Image_RotateFlip_rotateFlipType_, gdiplus._gdiplus_CLASS_Image_RotateFlip_rotateFlipType_
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
 - Image::RotateFlip
 - gdiplusheaders/Image::RotateFlip
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
 - Image.RotateFlip
---

# Image::RotateFlip


## -description

The <b>Image::RotateFlip</b> method rotates and flips this image.

## -parameters

### -param rotateFlipType [in]

Type: <b><a href="/windows/desktop/api/gdiplusimaging/ne-gdiplusimaging-rotatefliptype">RotateFlipType</a></b>

Element of the <a href="/windows/desktop/api/gdiplusimaging/ne-gdiplusimaging-rotatefliptype">RotateFlipType</a> enumeration that specifies the type of rotation and the type of flip.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusimaging/ne-gdiplusimaging-rotatefliptype">RotateFlipType</a>



<a href="/windows/desktop/gdiplus/-gdiplus-rotating-reflecting-and-skewing-images-use">Rotating, Reflecting, and Skewing Images</a>