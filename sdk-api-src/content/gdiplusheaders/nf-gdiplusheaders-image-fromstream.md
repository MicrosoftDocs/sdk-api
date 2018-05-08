---
UID: NF:gdiplusheaders.Image.FromStream
title: Image::FromStream
author: windows-driver-content
description: The Image::FromStream method creates a new Image object based on a stream.
old-location: gdiplus\_gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\fromstream_58stream_useembeddedcolormanagement.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: FromStream, FromStream method [GDI+], FromStream method [GDI+],Image class, Image class [GDI+],FromStream method, Image.FromStream, Image::FromStream, _gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Image_FromStream_stream_useEmbeddedColorManagement_
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Image.FromStream
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Image::FromStream


## -description


The <b>Image::FromStream</b> method creates a new 
			<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object based on a stream.


## -parameters




### -param stream [in]

Type: <b><a href="_stg_istream">IStream</a>*</b>

Pointer to an 
					<a href="_stg_istream">IStream</a> interface. The implementation of 
					IStream must include the 
					<a href="_stg_istream_seek">IStream::Seek</a>, 
					<b>Read</b>, and 
					<a href="_stg_istream_stat">IStream::Stat</a> methods. 


### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new 
					<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object applies color correction according to color management information that is embedded in the stream. Embedded information can include International Color Consortium (ICC) profiles, gamma values, and chromaticity information. <b>TRUE</b> specifies that color correction is enabled, and <b>FALSE</b> specifies that color correction is not enabled. The default value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>
</strong>

This method returns a pointer to the new 
						<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/0ad2a132-6db6-4099-81a2-10e1cd1b1f61">Drawing, Positioning, and Cloning Images</a>



<a href="_stg_istream">IStream</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/4962e901-cc4f-4225-8d24-731225e149e6">Image Constructors</a>



<a href="https://msdn.microsoft.com/a22163d0-36fc-4bf3-be21-f39145138a87">Image::Clone</a>



<a href="https://msdn.microsoft.com/53b237cc-4d96-46fb-8430-b7210ba9f42e">Image::FromFile</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>



<a href="_stg_stgopenstorage">StgOpenStorage</a>
 

 

