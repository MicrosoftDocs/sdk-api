---
UID: NF:gdiplusheaders.Bitmap.FromStream
title: Bitmap::FromStream (gdiplusheaders.h)
author: windows-sdk-content
description: The Bitmap::FromStream method creates a Bitmap object based on a stream.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapmethods\fromstream.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Bitmap class [GDI+],FromStream method, Bitmap.FromStream, Bitmap::FromStream, FromStream, FromStream method [GDI+], FromStream method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Bitmap_FromStream_stream_useEmbeddedColorManagement_
ms.topic: method
f1_keywords: 
 - "gdiplusheaders/Bitmap.FromStream"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.FromStream
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Bitmap::FromStream


## -description


The <b>Bitmap::FromStream</b> method creates a 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object based on a stream.


## -parameters




### -param stream [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>*</b>

Pointer to an 
					<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>COMCOM interface. The implementation of 
					IStream must include the 
					<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-seek">IStream::Seek</a>, 
					<b>Read</b>, and 
					<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istream-stat">IStream::Stat</a> methods. 


### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. <b>BOOL</b> value that specifies whether the new 
					<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object applies color correction according to color management information that is embedded in the stream. Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-images-bitmaps-and-metafiles-about">Images, Bitmaps, and Metafiles</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-using-images-bitmaps-and-metafiles-use">Using Images, Bitmaps, and Metafiles</a>
 

 

