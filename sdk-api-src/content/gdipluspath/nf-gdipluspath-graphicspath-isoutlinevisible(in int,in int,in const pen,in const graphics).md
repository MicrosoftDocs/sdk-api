---
UID: NF:gdipluspath.GraphicsPath.IsOutlineVisible(IN INT,IN INT,IN const Pen,IN const Graphics)
title: GraphicsPath::IsOutlineVisible(IN INT,IN INT,IN const Pen,IN const Graphics)
author: windows-sdk-content
description: The GraphicsPath::IsOutlineVisible method determines whether a specified point touches the outline of this path when the path is drawn by a specified Graphics object and a specified pen.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_IsOutlineVisible_INT_x_INT_y_Pen_pen_Graphics_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathisoutlinevisiblemethods\isoutlinevisible_5intx_inty_penpen_graphicsg.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GraphicsPath class [GDI+],IsOutlineVisible method, GraphicsPath.IsOutlineVisible, GraphicsPath.IsOutlineVisible(IN INT,IN INT,IN const Pen,IN const Graphics), GraphicsPath.IsOutlineVisible(INT,INT,const Pen*,const Graphics*), GraphicsPath::IsOutlineVisible, GraphicsPath::IsOutlineVisible(IN INT,IN INT,IN const Pen,IN const Graphics), IsOutlineVisible, IsOutlineVisible method [GDI+], IsOutlineVisible method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_IsOutlineVisible_INT_x_INT_y_Pen_pen_Graphics_g_, gdiplus._gdiplus_CLASS_GraphicsPath_IsOutlineVisible_INT_x_INT_y_Pen_pen_Graphics_g_
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
 - GraphicsPath.IsOutlineVisible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::IsOutlineVisible(IN INT,IN INT,IN const Pen,IN const Graphics)


## -description


The <b>GraphicsPath::IsOutlineVisible</b> method determines whether a specified point touches the outline of this path when the path is drawn by a specified <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object and a specified pen.


## -parameters




### -param x [in]

Type: <b>INT</b>

Integer that specifies the x-coordinate of the point to be tested. 


### -param y [in]

Type: <b>INT</b>

Integer that specifies the y-coordinate of the point to be tested. 


### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object. This method determines whether the test point touches the path outline that would be drawn by this pen. More points will touch an outline drawn by a wide pen than will touch an outline drawn by a narrow pen. 


### -param g [in]

Type: <b>const <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object that specifies a world-to-device transformation. If the value of this parameter is <b>NULL</b>, the test is done in world coordinates; otherwise, the test is done in device coordinates. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the test point touches the outline of this path, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/4a6b7b5d-a74d-43be-b35c-54c49d742f89">IsOutlineVisible Methods</a>



<a href="https://msdn.microsoft.com/d686ed98-9633-46f5-90f2-cb128b2b7e1c">IsVisible Methods</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/b529ba0b-1786-4925-88bd-1a8369fc368c">Setting Pen Width and Alignment</a>
 

 

