---
UID: NF:gdipluspath.GraphicsPath.GetPathPoints(OUT Point,IN INT)
title: GraphicsPath::GetPathPoints(OUT Point,IN INT)
author: windows-sdk-content
description: The GraphicsPath::GetPathPoints method gets this path's array of points. The array contains the endpoints and control points of the lines and B&#233;zier splines that are used to draw the path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPathPoints_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathgetpathpointsmethods\getpathpoints.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetPathPoints, GetPathPoints method [GDI+], GetPathPoints method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPathPoints method, GraphicsPath.GetPathPoints, GraphicsPath.GetPathPoints(OUT Point,IN INT), GraphicsPath.GetPathPoints(Point*,INT), GraphicsPath::GetPathPoints, GraphicsPath::GetPathPoints(OUT Point,IN INT), _gdiplus_CLASS_GraphicsPath_GetPathPoints_Point_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPathPoints_Point_points_INT_count_
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
 - GraphicsPath.GetPathPoints
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
- GraphicsPath.GetPathPoints
: 
req.product: GDI+ 1.0
---

# GraphicsPath::GetPathPoints(OUT Point,IN INT)


## -description


The <b>GraphicsPath::GetPathPoints</b> method gets this path's array of points. The array contains the endpoints and control points of the lines and Bézier splines that are used to draw the path.


## -parameters




### -param points [out]

Type: <b><a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> objects that receives the data points. You must allocate memory for this array. You can call the <a href="https://msdn.microsoft.com/52bbe19b-298f-4297-9d23-a7b3b1f1e004">GraphicsPath::GetPointCount</a> method to determine the required size of the array. The size, in bytes, should be the return value of <b>GraphicsPath::GetPointCount</b> multiplied by <b>sizeof</b>(<b>Point</b>). 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. Set this parameter equal to the return value of the <a href="https://msdn.microsoft.com/52bbe19b-298f-4297-9d23-a7b3b1f1e004">GraphicsPath::GetPointCount</a> method. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a> enumeration.


#### Examples



The following example creates and draws a path that has a line, a rectangle, an ellipse, and a curve. The code calls the path's <a href="https://msdn.microsoft.com/52bbe19b-298f-4297-9d23-a7b3b1f1e004">GraphicsPath::GetPointCount</a> method to determine the number of data points that are stored in the path. The code allocates a buffer large enough to receive the array of data points and passes the address of that buffer to the <b>GraphicsPath::GetPathPoints</b> method. Finally, the code draws each of the path's data points.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID GetPathPointsExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has a line, a rectangle, an ellipse, and a curve.
   GraphicsPath path;

   Point points[] = {
      Point(200, 200),
      Point(250, 240),
      Point(200, 300),
      Point(300, 310),
      Point(250, 350)};

   path.AddLine(20, 100, 150, 200);
   path.AddRectangle(Rect(40, 30, 80, 60));
   path.AddEllipse(Rect(200, 30, 200, 100));
   path.AddCurve(points, 5);

   // Draw the path.
   Pen pen(Color(255, 0, 0, 255));
   graphics.DrawPath(&amp;pen, &amp;path);

   // Get the path points.
   INT count = path.GetPointCount();
   Point* dataPoints = new Point[count];
   path.GetPathPoints(dataPoints, count);

   // Draw the path's data points.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j &lt; count; ++j)
   {
      graphics.FillEllipse(
         &amp;brush, 
         dataPoints[j].X - 3.0f, 
         dataPoints[j].Y - 3.0f,
         6.0f,
         6.0f);
   }
   delete [] dataPoints; 
}
Color(255, 255, 0,  0)</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/c757cfb8-25fe-4881-96b3-5257f925b781">GraphicsPath::GetPathData</a>



<a href="https://msdn.microsoft.com/fded6e62-0134-4e2c-aa40-cf0a32a5b2f2">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/52bbe19b-298f-4297-9d23-a7b3b1f1e004">GraphicsPath::GetPointCount</a>



<a href="https://msdn.microsoft.com/b8e9a4cb-72e1-4646-956a-50801176a3bd">PathData</a>



<a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>
 

 

