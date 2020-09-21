---
UID: NF:gdiplusheaders.Image.FromFile
title: Image::FromFile (gdiplusheaders.h)
description: The Image::FromFile method creates an Image object based on a file.
helpviewer_keywords: ["FromFile","FromFile method [GDI+]","FromFile method [GDI+]","Image class","Image class [GDI+]","FromFile method","Image.FromFile","Image::FromFile","_gdiplus_CLASS_Image_FromFile_filename_useEmbeddedColorManagement_","gdiplus._gdiplus_CLASS_Image_FromFile_filename_useEmbeddedColorManagement_"]
old-location: gdiplus\_gdiplus_CLASS_Image_FromFile_filename_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\fromfile_75filename_useembeddedcolormanagement.htm
ms.date: 12/05/2018
ms.keywords: FromFile, FromFile method [GDI+], FromFile method [GDI+],Image class, Image class [GDI+],FromFile method, Image.FromFile, Image::FromFile, _gdiplus_CLASS_Image_FromFile_filename_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Image_FromFile_filename_useEmbeddedColorManagement_
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
 - Image::FromFile
 - gdiplusheaders/Image::FromFile
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
 - Image.FromFile
---

# Image::FromFile


## -description

The <b>Image::FromFile</b> method creates an 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a file.

## -parameters

### -param filename [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string that specifies the name of the file.

### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object applies color correction according to color management information that is embedded in the image file. Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

## -remarks

You can create 
				<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> objects based on files of a variety of types including BMP, GIF, JPEG, PNG, TIFF, and EMF.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-image(gpimage_status)">Image Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-clone">Image::Clone</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-fromstream">Image::FromStream</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>