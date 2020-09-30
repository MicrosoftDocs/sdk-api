---
UID: NF:gdiplusheaders.Image.GetPhysicalDimension
title: Image::GetPhysicalDimension (gdiplusheaders.h)
description: The Image::GetPhysicalDimension method gets the width and height of this image.
helpviewer_keywords: ["GetPhysicalDimension","GetPhysicalDimension method [GDI+]","GetPhysicalDimension method [GDI+]","Image class","Image class [GDI+]","GetPhysicalDimension method","Image.GetPhysicalDimension","Image::GetPhysicalDimension","_gdiplus_CLASS_Image_GetPhysicalDimension_size_","gdiplus._gdiplus_CLASS_Image_GetPhysicalDimension_size_"]
old-location: gdiplus\_gdiplus_CLASS_Image_GetPhysicalDimension_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\getphysicaldimension.htm
ms.date: 12/05/2018
ms.keywords: GetPhysicalDimension, GetPhysicalDimension method [GDI+], GetPhysicalDimension method [GDI+],Image class, Image class [GDI+],GetPhysicalDimension method, Image.GetPhysicalDimension, Image::GetPhysicalDimension, _gdiplus_CLASS_Image_GetPhysicalDimension_size_, gdiplus._gdiplus_CLASS_Image_GetPhysicalDimension_size_
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
 - Image::GetPhysicalDimension
 - gdiplusheaders/Image::GetPhysicalDimension
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
 - Image.GetPhysicalDimension
---

# Image::GetPhysicalDimension


## -description

The <b>Image::GetPhysicalDimension</b> method gets the width and height of this image.

## -parameters

### -param size [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object that receives the width and height of this image.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/gdiplus/-gdiplus-cropping-and-scaling-images-about">Cropping and Scaling Images</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getbounds">Image::GetBounds</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getheight">Image::GetHeight</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-gethorizontalresolution">Image::GetHorizontalResolution</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getverticalresolution">Image::GetVerticalResolution</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-getwidth">Image::GetWidth</a>



<a href="/windows/desktop/gdiplus/-gdiplus-improving-performance-by-avoiding-automatic-scaling-use">Improving Performance by Avoiding Automatic Scaling</a>