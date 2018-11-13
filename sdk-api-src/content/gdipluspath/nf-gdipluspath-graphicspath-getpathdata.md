---
UID: NF:gdipluspath.GraphicsPath.GetPathData
title: GraphicsPath::GetPathData
author: windows-sdk-content
description: The GraphicsPath::GetPathData method gets an array of points and an array of point types from this path. Together, these two arrays define the lines, curves, figures, and markers of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPathData_pathData_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getpathdata.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetPathData, GetPathData method [GDI+], GetPathData method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPathData method, GraphicsPath.GetPathData, GraphicsPath::GetPathData, _gdiplus_CLASS_GraphicsPath_GetPathData_pathData_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPathData_pathData_
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
 - GraphicsPath.GetPathData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::GetPathData


## -description


The <b>GraphicsPath::GetPathData</b> method gets an array of points and an array of point types from this path. Together, these two arrays define the lines, curves, figures, and markers of this path.


## -parameters




### -param pathData [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534481(v=VS.85).aspx">PathData</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534481(v=VS.85).aspx">PathData</a> object that receives the path data. The <i>Points</i> data member of the <b>PathData</b> object receives a pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects that contains the path points. The <i>Types</i> data member of the <b>PathData</b> object receives a pointer to an array of bytes that contains the point types. The <i>Count</i> data member of the <b>PathData</b> object receives an integer that indicates the number of elements in the <i>Points</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a> enumeration.

You do not have to allocate or deallocate memory for the array of points or the array of types. The <b>GraphicsPath::GetPathData</b> method allocates memory for the arrays (points and types) that it returns. The <a href="https://msdn.microsoft.com/en-us/library/ms534481(v=VS.85).aspx">PathData</a> destructor deallocates the memory for those arrays.


#### Examples



The following example creates and draws a path that has a line, a rectangle, an ellipse, and a curve. The code gets the path's points and types by passing the address of a <a href="https://msdn.microsoft.com/en-us/library/ms534481(v=VS.85).aspx">PathData</a> object to the <b>GraphicsPath::GetPathData</b> method. Then the code draws each of the path's data points.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID GetPathDataExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has a line, a rectangle, an ellipse, and a curve.
   GraphicsPath path;
   
   PointF points[] = {
      PointF(200, 200),
      PointF(250, 240),
      PointF(200, 300),
      PointF(300, 310),
      PointF(250, 350)};

   path.AddLine(20, 100, 150, 200);
   path.AddRectangle(Rect(40, 30, 80, 60));
   path.AddEllipse(Rect(200, 30, 200, 100));
   path.AddCurve(points, 5);

   // Draw the path.
   Pen pen(Color(255, 0, 0, 255));
   graphics.DrawPath(&amp;pen, &amp;path);

   // Get the path data.
   PathData pathData;
   path.GetPathData(&amp;pathData);

   // Draw the path's data points.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j &lt; pathData.Count; ++j)
   {
      graphics.FillEllipse(
         &amp;brush, 
         pathData.Points[j].X - 3.0f, 
         pathData.Points[j].Y - 3.0f,
         6.0f,
         6.0f);
   }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535561(v=VS.85).aspx">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535535(v=VS.85).aspx">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535536(v=VS.85).aspx">GraphicsPath::GetPointCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534481(v=VS.85).aspx">PathData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
 

 

