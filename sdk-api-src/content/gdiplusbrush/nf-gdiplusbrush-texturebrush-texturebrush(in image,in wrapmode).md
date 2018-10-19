---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(IN Image,IN WrapMode)
title: TextureBrush::TextureBrush(IN Image,IN WrapMode)
author: windows-sdk-content
description: Creates a TextureBrush object based on an image and a wrap mode. The size of the brush defaults to the size of the image, so the entire image is used by the brush.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_image_wrapMode_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_99image_wrapmode.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN WrapMode), TextureBrush.TextureBrush(Image*,WrapMode), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN WrapMode), _gdiplus_CLASS_TextureBrush_TextureBrush_image_wrapMode_, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_image_wrapMode_
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
req.product: GDI+ 1.0
---

# TextureBrush::TextureBrush(IN Image,IN WrapMode)


## -description


Creates a <a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a> object based on an image and a wrap mode. The size of the brush defaults to the size of the image, so the entire image is used by the brush.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that contains the bitmap of the image to use. 


### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush. The default value is <b>WrapModeTile</b>. 


## -remarks



An area that extends beyond the boundaries of the brush is tiled with repeated copies of the brush. A texture brush may have alternate tiles flipped in a certain direction, as specified by the wrap mode. Flipping has the effect of reversing the brush's image. For example, if the wrap mode is specified as <b>WrapModeTileFlipX</b>, the brush is flipped about a line that is parallel to the y-axis. 

The texture brush is always oriented at (0, 0). If the wrap mode is specified as <b>WrapModeClamp</b>, no area outside of the brush is tiled. For example, suppose you create a texture brush, specifying <b>WrapModeClamp</b> as the wrap mode:

<code>TextureBrush(&amp;SomeImage, WrapModeClamp)</code>

Then, you paint an area with the brush. If the size of the brush has a height of 50 and the painted area is a rectangle with its upper-left corner at (0, 50), you will see no repeated copies of the brush (no tiling).

The default wrap mode for a texture brush is <b>WrapModeTile</b>, which specifies no flipping of the tile and no clamping.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534512(v=VS.85).aspx">TextureBrush</a>



<a href="https://msdn.microsoft.com/e5970d3d-e2ef-42f3-9dcc-6b22dfbdf5c7">TextureBrush::GetWrapMode</a>



<a href="https://msdn.microsoft.com/a6a63380-700c-424e-a7c9-f877d1d520ab">TextureBrush::SetWrapMode</a>



<a href="https://msdn.microsoft.com/8ccf2c4a-6f99-465f-8adf-0f7fcd002f79">Using a Brush to Fill Shapes</a>



<a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a>
 

 

