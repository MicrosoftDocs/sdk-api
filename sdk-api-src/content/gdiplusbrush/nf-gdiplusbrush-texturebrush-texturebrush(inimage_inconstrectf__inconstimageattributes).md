---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(IN Image,IN const RectF &,IN const ImageAttributes)
title: TextureBrush::TextureBrush(IN Image,IN const RectF &,IN const ImageAttributes)
author: windows-sdk-content
description: Creates a TextureBrush object based on an image, a defining rectangle, and a set of image properties.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_RectF_dstRect_ImageAttributes_imageAttributes_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_76imageimage_rectfampdstrect_imageattrib.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN const RectF &,IN const ImageAttributes), TextureBrush.TextureBrush(Image*,RectF&,ImageAttributes*), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN const RectF &,IN const ImageAttributes), _gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_RectF_dstRect_ImageAttributes_imageAttributes_, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_RectF_dstRect_ImageAttributes_imageAttributes_
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
---

# TextureBrush::TextureBrush(IN Image,IN const RectF &,IN const ImageAttributes)


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a> object based on an image, a defining rectangle, and a set of image properties.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object that contains the bitmap of the image to use. 


### -param dstRect [in, ref]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a></b>

Reference to a rectangle that defines the size of this texture brush and the portion of the image to be used by this texture brush. If the <a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object is created from a metafile, the brush uses the entire image, which is scaled to fit the size of the brush. 


### -param imageAttributes [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>*</b>

Optional. Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object that contains properties of the image. The default value is <b>NULL</b>. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533858(v=VS.85).aspx">Filling a Shape with an Image Texture</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534495(v=VS.85).aspx">Rect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>
 

 

