---
UID: NF:gdiplusheaders.Image.FromStream
title: Image::FromStream (gdiplusheaders.h)
description: The Image::FromStream method creates a new Image object based on a stream.
helpviewer_keywords: ["FromStream","FromStream method [GDI+]","FromStream method [GDI+]","Image class","Image class [GDI+]","FromStream method","Image.FromStream","Image::FromStream","_gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_","gdiplus._gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_"]
old-location: gdiplus\_gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\fromstream_58stream_useembeddedcolormanagement.htm
ms.date: 12/05/2018
ms.keywords: FromStream, FromStream method [GDI+], FromStream method [GDI+],Image class, Image class [GDI+],FromStream method, Image.FromStream, Image::FromStream, _gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_
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
 - Image::FromStream
 - gdiplusheaders/Image::FromStream
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
 - Image.FromStream
---

# Image::FromStream


## -description

The <b>Image::FromStream</b> method creates a new 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object based on a stream.

## -parameters

### -param stream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to an 
					<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface. The implementation of 
					IStream must include the 
					<a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">IStream::Seek</a>, 
					<b>Read</b>, and 
					<a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> methods.

### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object applies color correction according to color management information that is embedded in the stream. Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a> object.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-positioning-and-cloning-images-about">Drawing, Positioning, and Cloning Images</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-image(gpimage_status)">Image Constructors</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-clone">Image::Clone</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-image-fromfile">Image::FromFile</a>



<a href="/windows/desktop/gdiplus/-gdiplus-loading-and-displaying-bitmaps-use">Loading and Displaying Bitmaps</a>



<a href="/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage">StgOpenStorage</a>