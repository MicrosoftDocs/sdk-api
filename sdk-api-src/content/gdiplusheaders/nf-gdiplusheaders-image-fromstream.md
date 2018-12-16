---
UID: NF:gdiplusheaders.Image.FromStream
title: Image::FromStream
author: windows-sdk-content
description: The Image::FromStream method creates a new Image object based on a stream.
old-location: gdiplus\_gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\fromstream_58stream_useembeddedcolormanagement.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FromStream, FromStream method [GDI+], FromStream method [GDI+],Image class, Image class [GDI+],FromStream method, Image.FromStream, Image::FromStream, _gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_
ms.topic: method
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
 - Image.FromStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::FromStream


## -description


The <b>Image::FromStream</b> method creates a new 
			<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object based on a stream.


## -parameters




### -param stream [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a>*</b>

Pointer to an 
					<a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a> interface. The implementation of 
					IStream must include the 
					<a href="https://msdn.microsoft.com/en-us/library/Aa380043(v=VS.85).aspx">IStream::Seek</a>, 
					<b>Read</b>, and 
					<a href="https://msdn.microsoft.com/en-us/library/Aa380045(v=VS.85).aspx">IStream::Stat</a> methods. 


### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new 
					<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object applies color correction according to color management information that is embedded in the stream. Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536388(v=VS.85).aspx">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380034(v=VS.85).aspx">IStream</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535365(v=VS.85).aspx">Image Constructors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535367(v=VS.85).aspx">Image::Clone</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535370(v=VS.85).aspx">Image::FromFile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533830(v=VS.85).aspx">Loading and Displaying Bitmaps</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380341(v=VS.85).aspx">StgOpenStorage</a>
 

 

