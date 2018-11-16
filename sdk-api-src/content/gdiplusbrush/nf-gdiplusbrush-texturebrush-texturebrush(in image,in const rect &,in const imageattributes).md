---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(IN Image,IN const Rect &,IN const ImageAttributes)
title: TextureBrush::TextureBrush(IN Image,IN const Rect &,IN const ImageAttributes)
author: windows-sdk-content
description: Creates a TextureBrush object based on an image, a defining rectangle, and a set of image properties.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_Rect_dstRect_ImageAttributes_imageAttributes_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_25imageimage_rectampdstrect_imageattribu.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN const Rect &,IN const ImageAttributes), TextureBrush.TextureBrush(Image*,Rect&,ImageAttributes*), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN const Rect &,IN const ImageAttributes), _gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_Rect_dstRect_ImageAttributes_imageAttributes_, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_Rect_dstRect_ImageAttributes_imageAttributes_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
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
 - TextureBrush.TextureBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusbrush.h
: 
- TextureBrush.TextureBrush
: 
req.product: GDI+ 1.0
---

# TextureBrush::TextureBrush(IN Image,IN const Rect &,IN const ImageAttributes)


## -description


Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a defining rectangle, and a set of image properties.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that contains the bitmap of the image to use. 


### -param dstRect [in, ref]

Type: <b><a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a></b>

Reference to a rectangle that defines the size of this texture brush and the portion of the image to be used by this texture brush. If the <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object is created from a metafile, the brush uses the entire image, which is scaled to fit the size of the brush. 


### -param imageAttributes [in]

Type: <b><a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>*</b>

Optional. Pointer to an <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object that contains properties of the image. The default value is <b>NULL</b>. 


## -remarks



The width and height of the 
				<i>dstRect</i> rectangle define the width and height of a texture brush. A texture brush is always oriented at (0, 0). The upper-left point, width, and height of the rectangle specify the starting point, width, and height of the portion of the image to be used by a texture brush.

<h3><a id="How_this_constructor_uses_the_______dstRect_rectangle_with_nonmetafile_images"></a><a id="how_this_constructor_uses_the_______dstrect_rectangle_with_nonmetafile_images"></a><a id="HOW_THIS_CONSTRUCTOR_USES_THE_______DSTRECT_RECTANGLE_WITH_NONMETAFILE_IMAGES"></a>How this constructor uses the 
					dstRect rectangle with nonmetafile images</h3>
If the dimensions of the 
				<i>dstRect</i>rectangle are smaller than those of the image on which the brush is based, the brush's image is cropped — it is a portion of the image. If the dimensions of the 
				<i>dstRect</i> rectangle are equal to those of the image, the brush's image is identical to the image. The 
				<i>dstRect</i> rectangle must not include areas outside the dimensions of the image. Doing so will either produce unpredictable behavior or generate a run-time error. For example, suppose you have an image that is 256
				×256 pixels and you create a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on this image, passing  as the 
				<i>dstRect</i> parameter. The brush will use the lower-left portion of the image. The lower-left corner of this portion is also the lower-left corner of the image. Now suppose that you create another <b>TextureBrush</b> object based on the same image, passing  as the 
				<i>dstRect</i> parameter. Note that this rectangle has its uppermost coordinate at 157 instead of 156. This rectangle extends one unit beyond the height of the image and will most likely generate an access violation.

<h3><a id="How_this_constructor_uses_the_______dstRect_rectangle_with_metafile_images"></a><a id="how_this_constructor_uses_the_______dstrect_rectangle_with_metafile_images"></a><a id="HOW_THIS_CONSTRUCTOR_USES_THE_______DSTRECT_RECTANGLE_WITH_METAFILE_IMAGES"></a>How this constructor uses the 
					dstRect rectangle with metafile images</h3>
If the dimensions of the 
				<i>dstRect</i> rectangle are different from those of the image, the brush's image is scaled smaller or larger as needed to fit the rectangle. For example, suppose you have a metafile image that is 256
				×256 pixels and you create a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object, passing  as the 
				<i>dstRect</i> parameter. The brush's image will include all of the metafile image but will be scaled to fit the brush: It will be squished vertically and stretched horizontally. If the dimensions of the rectangle are equal to those of the image, the brush's image is identical to the image.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/12e1e132-a93f-4438-8a1d-9036a43a8fd8">Filling a Shape with an Image Texture</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a>
 

 

