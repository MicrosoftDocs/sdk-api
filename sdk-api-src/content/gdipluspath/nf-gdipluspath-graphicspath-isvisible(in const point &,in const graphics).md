---
UID: NF:gdipluspath.GraphicsPath.IsVisible(IN const Point &,IN const Graphics)
title: GraphicsPath::IsVisible(IN const Point &,IN const Graphics)
author: windows-sdk-content
description: The GraphicsPath::IsVisible method determines whether a specified point lies in the area that is filled when this path is filled by a specified Graphics object.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_IsVisible_Point_point_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathisvisiblemethods\isvisible_90pointamppoint_graphicsg.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GraphicsPath class [GDI+],IsVisible method, GraphicsPath.IsVisible, GraphicsPath.IsVisible(IN const Point &,IN const Graphics), GraphicsPath.IsVisible(const Point&,const Graphics*), GraphicsPath::IsVisible, GraphicsPath::IsVisible(IN const Point &,IN const Graphics), IsVisible, IsVisible method [GDI+], IsVisible method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_IsVisible_Point_point_Graphics_g_, gdiplus._gdiplus_CLASS_GraphicsPath_IsVisible_Point_point_Graphics_g_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdipluspath.h
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
 - GraphicsPath.IsVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdipluspath.h
: 
- GraphicsPath.IsVisible
: 
req.product: GDI+ 1.0
---

# GraphicsPath::IsVisible(IN const Point &,IN const Graphics)


## -description


The <b>GraphicsPath::IsVisible</b> method determines whether a specified point lies in the area that is filled when this path is filled by a specified <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.


## -parameters




### -param point [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a></b>

Reference to the point to be tested. 


### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object that specifies a world-to-device transformation. If the value of this parameter is <b>NULL</b>, the test is done in world coordinates; otherwise, the test is done in device coordinates. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the test point lies in the interior of this path, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/4a6b7b5d-a74d-43be-b35c-54c49d742f89">IsOutlineVisible Methods</a>



<a href="https://msdn.microsoft.com/d686ed98-9633-46f5-90f2-cb128b2b7e1c">IsVisible Methods</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>
 

 

