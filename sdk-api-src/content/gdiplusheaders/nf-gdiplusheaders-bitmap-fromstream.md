---
UID: NF:gdiplusheaders.Bitmap.FromStream
title: Bitmap::FromStream (gdiplusheaders.h)
description: The Bitmap::FromStream method creates a Bitmap object based on a stream.
helpviewer_keywords: ["Bitmap class [GDI+]","FromStream method","Bitmap.FromStream","Bitmap::FromStream","FromStream","FromStream method [GDI+]","FromStream method [GDI+]","Bitmap class","_gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_","gdiplus._gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromstream.htm
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],FromStream method, Bitmap.FromStream, Bitmap::FromStream, FromStream, FromStream method [GDI+], FromStream method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_
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
 - Bitmap::FromStream
 - gdiplusheaders/Bitmap::FromStream
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
 - Bitmap.FromStream
---

# Bitmap::FromStream


## -description

The <b>Bitmap::FromStream</b> method creates a 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on a stream.

## -parameters

### -param stream [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to an 
					<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> COM interface. The implementation of 
					IStream must include the 
					<a href="/windows/desktop/api/objidl/nf-objidl-istream-seek">IStream::Seek</a>, 
					<b>Read</b>, and 
					<a href="/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> methods.

### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. <b>BOOL</b> value that specifies whether the new 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object applies color correction according to color management information that is embedded in the stream. Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>*</b>

This method returns a pointer to the new 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>