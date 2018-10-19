---
UID: NF:gdiplusbrush.TextureBrush.TextureBrush(IN Image,IN WrapMode,IN const RectF &)
title: TextureBrush::TextureBrush(IN Image,IN WrapMode,IN const RectF &)
author: windows-sdk-content
description: Creates a TextureBrush object based on an image, a wrap mode, and a defining rectangle.
old-location: gdiplus\_gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_RectF_dstRect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\texturebrushclass\texturebrushconstructors\texturebrush_10imageimage_wrapmodewrapmode_rectfampds.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: TextureBrush, TextureBrush class [GDI+],TextureBrush constructor, TextureBrush constructor [GDI+], TextureBrush constructor [GDI+],TextureBrush class, TextureBrush.TextureBrush, TextureBrush.TextureBrush(IN Image,IN WrapMode,IN const RectF &), TextureBrush.TextureBrush(Image*,wrapMode,const RectF&), TextureBrush::TextureBrush, TextureBrush::TextureBrush(IN Image,IN WrapMode,IN const RectF &), _gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_RectF_dstRect_, gdiplus._gdiplus_CLASS_TextureBrush_TextureBrush_Image_image_WrapMode_wrapMode_RectF_dstRect_
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

# TextureBrush::TextureBrush(IN Image,IN WrapMode,IN const RectF &)


## -description


Creates a <a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object based on an image, a wrap mode, and a defining rectangle.


## -parameters




### -param image [in]

Type: <b><a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object that contains the bitmap of the image to use. 


### -param wrapMode [in]

Type: <b>wrapMode</b>

Element of the <a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a> enumeration that specifies how repeated copies of an image are used to tile an area when it is painted with this texture brush. 


### -param dstRect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a></b>

Reference to a rectangle that defines the size of this texture brush and the portion of the image to be used by this texture brush. If the <a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a> object is created from a metafile, the brush uses the entire image, which is scaled to fit the size of the brush. 


## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a>



<a href="https://msdn.microsoft.com/e5970d3d-e2ef-42f3-9dcc-6b22dfbdf5c7">TextureBrush::GetWrapMode</a>



<a href="https://msdn.microsoft.com/a6a63380-700c-424e-a7c9-f877d1d520ab">TextureBrush::SetWrapMode</a>



<a href="https://msdn.microsoft.com/8ccf2c4a-6f99-465f-8adf-0f7fcd002f79">Using a Brush to Fill Shapes</a>



<a href="https://msdn.microsoft.com/24b035f9-c03e-4502-b603-d6a9e47d6df9">WrapMode</a>
 

 

