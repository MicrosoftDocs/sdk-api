---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(IN Image,IN WrapMode,IN REAL,IN REAL,IN REAL,IN REAL)
title: TextureBrush::TextureBrush(IN Image,IN WrapMode,IN REAL,IN REAL,IN REAL,IN REAL)
author: windows-sdk-content
description: Creates a TextureBrush object based on an image, a wrap mode, and a defining set of coordinates.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_REAL_dstX_REAL_dstY_REAL_dstW.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_5imageimage_wrapmodewrapmode_realdstx_re.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN WrapMode,IN REAL,IN REAL,IN REAL,IN REAL), TextureBrush.TextureBrush(Image*,WrapMode,REAL,REAL,REAL,REAL), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN WrapMode,IN REAL,IN REAL,IN REAL,IN REAL), _gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_REAL_dstX_REAL_dstY_REAL_dstW, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_REAL_dstX_REAL_dstY_REAL_dstW
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

# TextureBrush::TextureBrush(IN Image,IN WrapMode,IN REAL,IN REAL,IN REAL,IN REAL)


## -description


Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a wrap mode, and a defining set of coordinates.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that contains the bitmap of the image to use. 


### -param wrapMode [in]

Type: <b><a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a></b>

Element of the <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush. 


### -param dstX [in]

Type: <b>REAL</b>

Leftmost coordinate of the image portion to be used by this brush. 


### -param dstY [in]

Type: <b>REAL</b>

Uppermost coordinate of the image portion to be used by this brush. 


### -param dstWidth [in]

Type: <b>REAL</b>

Width of the brush and width of the image portion to be used by the brush. 


### -param dstHeight [in]

Type: <b>REAL</b>

Height of the brush and height of the image portion to be used by the brush. 


## -remarks



The 
				<i>dstX</i>, 
				<i>dstY</i>, 
				<i>dstWidth</i>, and 
				<i>dstHeight</i> parameters specify a rectangle. The size of the brush is defined by 
				<i>dstWidth</i> and 
				<i>dstHeight</i>. The 
				<i>dstX</i> and 
				<i>dstY</i> parameters have no affect on the brush's size or position — the brush is always oriented at (0, 0). The 
				<i>dstX</i>, 
				<i>dstY</i>, 
				<i>dstWidth</i>, and 
				<i>dstHeight</i> parameters define the portion of the image to be used by the brush.

For example, suppose you have an image that is stored in an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object and is 256
				×512 (width
				×height) pixels. Then you create a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on this image as follows: 

<code>TextureBrush(&amp;someImage, WrapModeTile, 12, 50, 100, 150)</code>

The brush will have a width of 100 units and a height of 150 units. The brush will use a rectangular portion of the image. This portion begins at the pixel having coordinates (12, 50). The width and height of the portion are 100 and 150, respectively, measured from the starting pixel. 

Now suppose you create another <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on the same image and specify a different rectangle: 

<code>TextureBrush(&amp;someImage, WrapModeTile, 0, 0, 256, 512)</code>

The brush will have width and height equal to 256 and 512, respectively. The brush will use the entire image instead of a portion of it because the rectangle specifies a starting pixel at coordinates (0, 0) and dimensions identical to those of the image.



