---
UID: NF:gdiplusheaders.Image.Image(IN IStream,IN BOOL)
title: Image::Image(IN IStream,IN BOOL)
author: windows-sdk-content
description: Creates an Image::Image object based on a stream.
old-location: gdiplus\_gdiplus_CLASS_Image_Image_stream_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imageconstructors\image_28stream_useembeddedcolormanagement.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FALSE, Image, Image class [GDI+],Image constructor, Image constructor [GDI+], Image constructor [GDI+],Image class, Image.Image, Image.Image(IN IStream,IN BOOL), Image.Image(IStream*,BOOL), Image::Image, Image::Image(IN IStream,IN BOOL), TRUE, _gdiplus_CLASS_Image_Image_stream_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Image_Image_stream_useEmbeddedColorManagement_
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
 - Image.Image
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Image::Image(IN IStream,IN BOOL)


## -description


Creates an <b>Image::Image</b> object based on a stream.


## -parameters




### -param stream [in]

Type: <b><a href="_stg_istream">IStream</a>*</b>

Pointer to an <a href="_stg_istream">IStream</a> interface. The implementation of IStream must include the <b>Seek</b>, <b>Read</b>, and <b>Stat</b> methods. 


### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. <b>BOOL</b> value that specifies whether the new <b>Image::Image</b> object applies color correction according to color management information that is embedded in the stream. Embedded information can include ICC profiles, gamma values, and chromaticity information.



#### FALSE

Default. Specifies that color correction is enabled



#### TRUE

Specifies that color correction is not enabled


## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/0ad2a132-6db6-4099-81a2-10e1cd1b1f61">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/4962e901-cc4f-4225-8d24-731225e149e6">Image Constructors</a>



<a href="https://msdn.microsoft.com/a22163d0-36fc-4bf3-be21-f39145138a87">Image::Clone</a>



<a href="https://msdn.microsoft.com/53b237cc-4d96-46fb-8430-b7210ba9f42e">Image::FromFile</a>



<a href="https://msdn.microsoft.com/93fd84c5-ef6b-447f-b456-30b5a8cf0e7d">Image::FromStream</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>
 

 

