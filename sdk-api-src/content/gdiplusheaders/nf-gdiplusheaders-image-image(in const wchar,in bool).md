---
UID: NF:gdiplusheaders.Image.Image(IN const WCHAR,IN BOOL)
title: Image::Image(IN const WCHAR,IN BOOL)
author: windows-sdk-content
description: Creates an Image::Image object based on a file.
old-location: gdiplus\_gdiplus_CLASS_Image_Image_filename_useEmbeddedColorManagement_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imageconstructors\image_53filename_useembeddedcolormanagement.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FALSE, Image, Image class [GDI+],Image constructor, Image constructor [GDI+], Image constructor [GDI+],Image class, Image.Image, Image.Image(IN const WCHAR,IN BOOL), Image.Image(const WCHAR*,BOOL), Image::Image, Image::Image(IN const WCHAR,IN BOOL), TRUE, _gdiplus_CLASS_Image_Image_filename_useEmbeddedColorManagement_, gdiplus._gdiplus_CLASS_Image_Image_filename_useEmbeddedColorManagement_
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
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Image.Image
: 
req.product: GDI+ 1.0
---

# Image::Image(IN const WCHAR,IN BOOL)


## -description


Creates an <b>Image::Image</b> object based on a file.


## -parameters




### -param filename [in]

Type: <b>const WCHAR*</b>

Pointer to a wide-character string that specifies the name of the file. 


### -param useEmbeddedColorManagement [in]

Type: <b>BOOL</b>

Optional. Boolean value that specifies whether the new <b>Image::Image</b> object applies color correction according to color management information that is embedded in the image file. Embedded information can include ICC profiles, gamma values, and chromaticity information.



#### FALSE

Default. Specifies that color correction is enabled



#### TRUE

Specifies that color correction is not enabled


## -remarks



You can construct <b>Image::Image</b> objects based on files of a variety of types including BMP, Graphics Interchange Format (GIF), JPEG, PNG, TIFF, and EMF. 




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/0ad2a132-6db6-4099-81a2-10e1cd1b1f61">Drawing, Positioning, and Cloning Images</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/4962e901-cc4f-4225-8d24-731225e149e6">Image Constructors</a>



<a href="https://msdn.microsoft.com/a22163d0-36fc-4bf3-be21-f39145138a87">Image::Clone</a>



<a href="https://msdn.microsoft.com/53b237cc-4d96-46fb-8430-b7210ba9f42e">Image::FromFile</a>



<a href="https://msdn.microsoft.com/93fd84c5-ef6b-447f-b456-30b5a8cf0e7d">Image::FromStream</a>



<a href="https://msdn.microsoft.com/8c1a26d9-b640-4f38-8276-10c4464525f2">Loading and Displaying Bitmaps</a>
 

 

