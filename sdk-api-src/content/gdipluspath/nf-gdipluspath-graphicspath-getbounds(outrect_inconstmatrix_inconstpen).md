---
UID: NF:gdipluspath.GraphicsPath.GetBounds(OUT Rect,IN const Matrix,IN const Pen)
title: GraphicsPath::GetBounds(OUT Rect,IN const Matrix,IN const Pen)
author: windows-sdk-content
description: The GraphicsPath::GetBounds method gets a bounding rectangle for this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetBounds_Rect_bounds_Matrix_matrix_Pen_pen_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathgetboundsmethods\getbounds.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetBounds, GetBounds method [GDI+], GetBounds method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetBounds method, GraphicsPath.GetBounds, GraphicsPath.GetBounds(OUT Rect,IN const Matrix,IN const Pen), GraphicsPath.GetBounds(Rect*,const Matrix*,const Pen*), GraphicsPath::GetBounds, GraphicsPath::GetBounds(OUT Rect,IN const Matrix,IN const Pen), _gdiplus_CLASS_GraphicsPath_GetBounds_Rect_bounds_Matrix_matrix_Pen_pen_, gdiplus._gdiplus_CLASS_GraphicsPath_GetBounds_Rect_bounds_Matrix_matrix_Pen_pen_
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
 - GraphicsPath.GetBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::GetBounds(OUT Rect,IN const Matrix,IN const Pen)


## -description


The <b>GraphicsPath::GetBounds</b> method gets a bounding rectangle for this path.


## -parameters




### -param bounds [out]

Type: <b><a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object that receives the bounding rectangle. 


### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies a transformation to be applied to this path before the bounding rectangle is calculated. This path is not permanently transformed; the transformation is used only during the process of calculating the bounding rectangle. The default value is <b>NULL</b>. 


### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object that influences the size of the bounding rectangle. The bounding rectangle received in <i>bounds</i> will be large enough to enclose this path when the path is drawn with the pen specified by this parameter. This ensures that the path is enclosed by the bounding rectangle even if the path is drawn with a wide pen. The default value is <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The rectangle returned by this method might be larger than necessary to enclose the path as drawn by the specified pen. The rectangle is calculated to allow for the pen's miter limit at sharp corners and to allow for the pen's end caps.


#### Examples



The following example creates a path that has one curve and one ellipse. The code draws the path with a thick yellow pen and a thin black pen. The <b>GraphicsPath::GetBounds</b> method receives the address of the thick yellow pen and calculates a bounding rectangle for the path. Then the code draws the bounding rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID GetBoundsExample(HDC hdc)
{
   Graphics graphics(hdc);
   Pen blackPen(Color(255, 0, 0, 0), 1);
   Pen yellowPen(Color(255, 255, 255, 0), 10);
   Pen redPen(Color(255, 255, 0, 0), 1);

   Point pts[] = {Point(120,120), 
                  Point(200,130), 
                  Point(150,200), 
                  Point(130,180)};

   // Create a path that has one curve and one ellipse.
   GraphicsPath path;
   path.AddClosedCurve(pts, 4);
   path.AddEllipse(120, 220, 100, 40);

   // Draw the path with a thick yellow pen and a thin black pen.
   graphics.DrawPath(&amp;yellowPen, &amp;path);
   graphics.DrawPath(&amp;blackPen, &amp;path);
 
   // Get the path's bounding rectangle.
   Rect rect;
   path.GetBounds(&amp;rect, NULL, &amp;yellowPen);
   graphics.DrawRectangle(&amp;redPen, rect);  
}

Color(255, 0, 0, 0)Color(255, 255, 0,  0)</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>
 

 

