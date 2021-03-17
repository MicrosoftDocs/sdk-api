---
UID: NF:gdiplusheaders.Bitmap.FromFile
title: Bitmap::FromFile (gdiplusheaders.h)
description: The Bitmap::FromFile method creates a Bitmap object based on an image file.
helpviewer_keywords: ["Bitmap class [GDI+]","FromFile method","Bitmap.FromFile","Bitmap::FromFile","FromFile","FromFile method [GDI+]","FromFile method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_FromFile_filename_useEmbeddedColorManagement_","gdiplus._gdiplus_CLASS_Bitmap_FromFile_filename_useEmbeddedColorManagement_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromFile_filename_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromfile.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],FromFile method, Bitmap.FromFile, Bitmap::FromFile, FromFile, FromFile method [GDI+], FromFile method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromFile_filename_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Bitmap_FromFile_filename_useEmbeddedColorManagement_
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
 - Bitmap::FromFile
 - gdiplusheaders/Bitmap::FromFile
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
 - Bitmap.FromFile
---

# Bitmap::FromFile


## -description

The <b>Bitmap::FromFile</b> method creates a 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on an image file.

## -parameters

### -param filename [in]

Type: <b>const WCHAR*</b>

Pointer to a null-terminated string that specifies the path name of the image file. The graphics file formats supported by GDI+ are BMP, GIF, JPEG, PNG, TIFF, Exif, WMF, and EMF.

### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object applies color correction according to color management information that is embedded in the image file. Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>*</b>

This method returns a pointer to the new 
						<b>Bitmap</b> object.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://msdn.microsoft.com/9b246a76-e8c0-41b2-9bb2-0df06ebc5563">Bitmap Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>