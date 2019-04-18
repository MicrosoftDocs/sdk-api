---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(IN Image,IN WrapMode,const IN Rect &)
title: TextureBrush::TextureBrush(IN Image,IN WrapMode,const IN Rect &) (gdiplusbrush.h)
author: windows-sdk-content
description: Creates a TextureBrush object based on an image, a wrap mode, and a defining rectangle.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_Rect_dstRect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_9imageimage_wrapmodewrapmode_rectampdstr.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN WrapMode,const IN Rect &), TextureBrush.TextureBrush(Image*,WrapMode,const Rect&), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN WrapMode,const IN Rect &), _gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_Rect_dstRect_, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_Rect_dstRect_
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
req.product: GDI+ 1.0
ms.custom: 19H1
---

# TextureBrush::TextureBrush(IN Image,IN WrapMode,const IN Rect &)


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a> object based on an image, a wrap mode, and a defining rectangle.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object that contains the bitmap of the image to use. 


### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush. 


### -param dstRect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a></b>

Reference to a rectangle that defines the size of this texture brush and the portion of the image to be used by this texture brush. If the <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object is created from a metafile, the brush uses the entire image, which is scaled to fit the size of the brush. 


## -remarks



The width and height of a texture brush are defined by the width and height of the 
				<i>dstRect</i> rectangle. A texture brush is always oriented at (0, 0). The upper-left point, width, and height of the rectangle specify the starting point, width, and height of the portion of the image to be used by a texture brush.

<h3><a id="How_this_constructor_uses_the_______dstRect_rectangle_with_nonmetafile_images"></a><a id="how_this_constructor_uses_the_______dstrect_rectangle_with_nonmetafile_images"></a><a id="HOW_THIS_CONSTRUCTOR_USES_THE_______DSTRECT_RECTANGLE_WITH_NONMETAFILE_IMAGES"></a>How this constructor uses the 
					dstRect rectangle with nonmetafile images</h3>
If the dimensions of the 
				<i>dstRect</i> rectangle are smaller than those of the image on which the brush is based, the brush's image is cropped — it is a portion of the image. If the dimensions of the 
				<i>dstRect</i> rectangle are equal to those of the image, the brush's image is identical to the image. The 
				<i>dstRect</i> rectangle must not include areas outside the dimensions of the image. Doing so will either produce unpredictable behavior or generate a run-time error. For example, suppose you have an image that is 256
				×256 pixels and you create a <a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a> object based on this image, passing  as the 
				<i>dstRect</i> parameter. The brush will use the lower left portion of the image. The lower-left corner of this portion is also the lower-left corner of the image. Now suppose that you create another <b>TextureBrush</b> object based on the same image, passing  as the 
				<i>dstRect</i> parameter. Note that this rectangle has its uppermost coordinate at 157 instead of 156. This rectangle extends one unit beyond the height of the image and will most likely generate an access violation.

<h3><a id="How_this_constructor_uses_the_______dstRect_rectangle_with_metafile_images"></a><a id="how_this_constructor_uses_the_______dstrect_rectangle_with_metafile_images"></a><a id="HOW_THIS_CONSTRUCTOR_USES_THE_______DSTRECT_RECTANGLE_WITH_METAFILE_IMAGES"></a>How this constructor uses the 
					dstRect rectangle with metafile images</h3>
If the dimensions of the 
				<i>dstRect</i> rectangle are different from those of the image, the brush's image is scaled smaller or larger as needed to fit the rectangle. For example, suppose you have a metafile image that is 256
				×256 pixels and you create a <a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a> object, passing  as the 
				<i>dstRect</i> parameter. The brush's image will include all of the metafile image but will be scaled to fit the brush: It will be squished vertically and stretched horizontally. If the dimensions of the rectangle are equal to those of the image, the brush's image is identical to the image.

<h3><a id="How_this_constructor_uses_the_wrap_mode"></a><a id="how_this_constructor_uses_the_wrap_mode"></a><a id="HOW_THIS_CONSTRUCTOR_USES_THE_WRAP_MODE"></a>How this constructor uses the wrap mode</h3>
An area that extends beyond the boundaries of the brush is tiled with repeated copies of the brush. A texture brush may have alternate tiles flipped in a certain direction, as specified by the wrap mode. Flipping has the effect of reversing the brush's image.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534527(v=VS.85).aspx">TextureBrush::GetWrapMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534540(v=VS.85).aspx">TextureBrush::SetWrapMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533811(v=VS.85).aspx">Using a Brush to Fill Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534407(v=VS.85).aspx">WrapMode</a>
 

 

