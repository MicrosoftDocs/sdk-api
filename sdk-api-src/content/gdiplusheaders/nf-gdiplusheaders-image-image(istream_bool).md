---
UID: NF:gdiplusheaders.Image.Image(IStream,BOOL)
title: Image::Image(IN IStream,IN BOOL) (gdiplusheaders.h)
description: Creates an Image::Image object based on a stream.
helpviewer_keywords: ["FALSE","Image","Image class [GDI+]","Image constructor","Image constructor [GDI+]","Image constructor [GDI+]","Image class","Image.Image","Image.Image(IN IStream","IN BOOL)","Image.Image(IStream*","BOOL)","Image::Image","Image::Image(IN IStream","IN BOOL)","TRUE","_gdiplus_CLASS_Image_Image_stream_useEmbeddedColorManagement_","gdiplus._gdiplus_CLASS_Image_Image_stream_useEmbeddedColorManagement_"]
old-location: gdiplus\_gdiplus_CLASS_Image_Image_stream_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imageconstructors\image_28stream_useembeddedcolormanagement.htm
ms.date: 12/05/2018
ms.keywords: FALSE, Image, Image class [GDI+],Image constructor, Image constructor [GDI+], Image constructor [GDI+],Image class, Image.Image, Image.Image(IN IStream,IN BOOL), Image.Image(IStream*,BOOL), Image::Image, Image::Image(IN IStream,IN BOOL), TRUE, _gdiplus_CLASS_Image_Image_stream_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Image_Image_stream_useEmbeddedColorManagement_
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
 - Image::Image
 - gdiplusheaders/Image::Image
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
 - Image.Image
---

# Image::Image(IN IStream,IN BOOL)


## -description

Creates an <b>Image::Image</b> object based on a stream.

## -parameters

### -param stream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface. The implementation of IStream must include the <b>Seek</b>, <b>Read</b>, and <b>Stat</b> methods.

### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. <b>BOOL</b> value that specifies whether the new <b>Image::Image</b> object applies color correction according to color management information that is embedded in the stream. Embedded information can include ICC profiles, gamma values, and chromaticity information.



#### FALSE

Default. Specifies that color correction is enabled



#### TRUE

Specifies that color correction is not enabled

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-image(gpimage_status)">Image Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-clone">Image::Clone</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-fromfile">Image::FromFile</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-fromstream">Image::FromStream</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>