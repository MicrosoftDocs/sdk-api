---
UID: NF:gdiplusgraphics.Graphics.DrawPolygon(IN const Pen,IN const Point,IN INT)
title: Graphics::DrawPolygon(IN const Pen,IN const Point,IN INT)
author: windows-sdk-content
description: The Graphics::DrawPolygon method draws a polygon.
old-location: gdiplus\_gdiplus_CLASS_Graphics_DrawPolygon_Pen_pen_PointF_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsdrawpolygonmethods\drawpolygon_62penpen_pointfpoints_intcount.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: DrawPolygon, DrawPolygon method [GDI+], DrawPolygon method [GDI+],Graphics class, Graphics class [GDI+],DrawPolygon method, Graphics.DrawPolygon, Graphics.DrawPolygon(IN const Pen,IN const Point,IN INT), Graphics.DrawPolygon(const Pen*,const PointF*,INT*), Graphics::DrawPolygon, Graphics::DrawPolygon(IN const Pen,IN const Point,IN INT), _gdiplus_CLASS_Graphics_DrawPolygon_Pen_pen_PointF_points_INT_count_, gdiplus._gdiplus_CLASS_Graphics_DrawPolygon_Pen_pen_PointF_points_INT_count_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
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
 - Graphics.DrawPolygon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# Graphics::DrawPolygon(IN const Pen,IN const Point,IN INT)


## -description


The <b>Graphics::DrawPolygon</b> method draws a polygon.


## -parameters




### -param pen [in]

Type: <b>const <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>*</b>

Pointer to a pen that is used to draw the polygon. 


### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> objects that specify the vertices of the polygon. 


### -param count [in]

Type: <b>INT*</b>

Integer that specifies the number of elements in the 
					<i>points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



If the first and last coordinates in the 
				<i>points</i> array are not identical, a line is drawn between them to close the polygon.


#### Examples



The following example draws a polygon, defined by an array of points.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_DrawPolygon2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Create an array of PointF objects that define the polygon.
   PointF point1(100.0f, 100.0f);
   PointF point2(200.0f, 130.0f);
   PointF point3(150.0f, 200.0f);
   PointF point4(50.0f, 200.0f);
   PointF point5(0.0f, 130.0f);
   PointF points[5] = {point1, point2, point3, point4, point5};
   PointF* pPoints = points;

   // Draw the polygon.
   graphics.DrawPolygon(&amp;blackPen, pPoints, 5);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e7cc93ab-c1e6-40e7-8888-f6bbffa42a00">FillPolygon Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>



<a href="https://msdn.microsoft.com/f1155341-83f3-4805-8d42-a1910515db31">Polygons</a>
 

 

