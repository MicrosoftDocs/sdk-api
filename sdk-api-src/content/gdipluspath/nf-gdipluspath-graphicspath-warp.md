---
UID: NF:gdipluspath.GraphicsPath.Warp
title: GraphicsPath::Warp
author: windows-sdk-content
description: The GraphicsPath::Warp method applies a warp transformation to this path. The GraphicsPath::Warp method also flattens (converts to a sequence of straight lines) the path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Warp_destPoints_count_srcRect_matrix_warpMode_flatness_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\warp.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GraphicsPath class [GDI+],Warp method, GraphicsPath.Warp, GraphicsPath::Warp, Warp, Warp method [GDI+], Warp method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Warp_destPoints_count_srcRect_matrix_warpMode_flatness_, gdiplus._gdiplus_CLASS_GraphicsPath_Warp_destPoints_count_srcRect_matrix_warpMode_flatness_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.redist: 
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - GraphicsPath.Warp
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPath::Warp


## -description


The <b>GraphicsPath::Warp</b> method applies a warp transformation to this path. The <b>GraphicsPath::Warp</b> method also flattens (converts to a sequence of straight lines) the path.


## -parameters




### -param destPoints [in]

Type: <b>const <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array of points that, along with the <i>srcRect</i> parameter, defines the warp transformation. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of points in the 
					<i>destPoints</i> array. The value of this parameter must be 3 or 4. 


### -param srcRect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a></b>

Reference to a rectangle that, along with the <i>destPoints</i> parameter, defines the warp transformation. 


### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that represents a transformation to be applied along with the warp. If this parameter is <b>NULL</b>, no transformation is applied. The default value is <b>NULL</b>. 


### -param warpMode [in]

Type: <b><a href="https://msdn.microsoft.com/fd3d4d59-ee65-4a1c-93b9-473327c170ce">WarpMode</a></b>

Optional. Element of the <a href="https://msdn.microsoft.com/fd3d4d59-ee65-4a1c-93b9-473327c170ce">WarpMode</a> enumeration that specifies the kind of warp to be applied. The default value is WarpModePerspective. 


### -param flatness [in]

Type: <b>REAL</b>

Optional. Real number that influences the number of line segments that are used to approximate the original path. Small values specify that many line segments are used, and large values specify that few line segments are used. The default value is FlatnessDefault, which is a constant defined in Gdiplusenums.h. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object stores a collection of data points that represent lines and curves. The <b>GraphicsPath::Warp</b> method converts those data points so that they represent only lines. The <i>flatness</i> parameter influences the number of lines that are stored. The original data points that represented curves are lost.

If the 
				<i>count</i> parameter has a value of 4, the warp transformation is defined as shown in the following table.

<table>
<tr>
<th>Source point</th>
<th>Destination point</th>
</tr>
<tr>
<td>Upper-left corner of <i>srcRect</i></td>
<td><i>destPoints</i>[0]</td>
</tr>
<tr>
<td>Upper-right corner of <i>srcRect</i></td>
<td><i>destPoints</i>[1]</td>
</tr>
<tr>
<td>Lower-left corner of <i>srcRect</i></td>
<td><i>destPoints</i>[2]</td>
</tr>
<tr>
<td>Lower-right corner of <i>srcRect</i></td>
<td><i>destPoints</i>[3]</td>
</tr>
</table>
 

A transformation specified by a source rectangle and four destination points is capable of mapping a rectangle to an arbitrary quadrilateral that is not necessarily a parallelogram.

If the count parameter has a value of 3, the warp transformation is defined as shown in the following table.

<table>
<tr>
<th>Source point</th>
<th>Destination point</th>
</tr>
<tr>
<td>Upper-left corner of 
							<i>srcRect</i></td>
<td><i>destPoints</i>[0]</td>
</tr>
<tr>
<td>Upper-right corner of 
							<i>srcRect</i></td>
<td><i>destPoints</i>[1]</td>
</tr>
<tr>
<td>Lower-left corner of 
							<i>srcRect</i></td>
<td><i>destPoints</i>[2]</td>
</tr>
</table>
 

A transformation specified by a source rectangle and three destination points maps rectangles to parallelograms.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object and adds a closed figure to the path. The code defines a warp transformation by specifying a source rectangle and an array of four destination points. The source rectangle and destination points are passed to the <b>Warp</b> method. The code draws the path twice: once before it has been warped and once after it has been warped.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID WarpExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path.
   PointF points[] ={
      PointF(20.0f, 60.0f),
      PointF(30.0f, 90.0f),
      PointF(15.0f, 110.0f),
      PointF(15.0f, 145.0f),
      PointF(55.0f, 145.0f),
      PointF(55.0f, 110.0f),
      PointF(40.0f, 90.0f),
      PointF(50.0f, 60.0f)};

   GraphicsPath path;
   path.AddLines(points, 8);
   path.CloseFigure();

   // Draw the path before applying a warp transformation.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawPath(&amp;bluePen, &amp;path);

   // Define a warp transformation, and warp the path.
   RectF srcRect(10.0f, 50.0f, 50.0f, 100.0f);

   PointF destPts[] = {
      PointF(220.0f, 10.0f),
      PointF(280.0f, 10.0f),
      PointF(100.0f, 150.0f),
      PointF(400.0f, 150.0f)};

   path.Warp(destPts, 4, srcRect);

   // Draw the warped path.
   graphics.DrawPath(&amp;bluePen, &amp;path);

   // Draw the source rectangle and the destination polygon.
   Pen blackPen(Color(255, 0, 0, 0));
   graphics.DrawRectangle(&amp;blackPen, srcRect);
   graphics.DrawLine(&amp;blackPen, destPts[0], destPts[1]);
   graphics.DrawLine(&amp;blackPen, destPts[0], destPts[2]);
   graphics.DrawLine(&amp;blackPen, destPts[1], destPts[3]);
   graphics.DrawLine(&amp;blackPen, destPts[2], destPts[3]);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8">Flattening Paths</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/947b3e68-67ad-47fb-80bb-b5a678f71381">GraphicsPath::Flatten</a>



<a href="https://msdn.microsoft.com/f896fcfd-2094-46f0-a9f8-469f13dccfa2">GraphicsPath::Outline</a>



<a href="https://msdn.microsoft.com/e8351fb1-b11f-4da7-9cc4-dc3ab685f29d">GraphicsPath::Widen</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/fd3d4d59-ee65-4a1c-93b9-473327c170ce">WarpMode</a>
 

 

