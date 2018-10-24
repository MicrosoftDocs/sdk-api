---
UID: NF:gdipluspath.GraphicsPath.AddCurve(IN const Point,IN INT,IN INT,IN INT,IN REAL)
title: GraphicsPath::AddCurve(IN const Point,IN INT,IN INT,IN INT,IN REAL)
author: windows-sdk-content
description: The GraphicsPath::AddCurve method adds a cardinal spline to the current figure of this path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddCurve_Point_points_INT_count_INT_offset_INT_numberOfSegments_REAL_ten.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddcurvemethods\addcurve_5pointpoints_intcount_intoffset_intnumbe.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: AddCurve, AddCurve method [GDI+], AddCurve method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddCurve method, GraphicsPath.AddCurve, GraphicsPath.AddCurve(IN const Point,IN INT,IN INT,IN INT,IN REAL), GraphicsPath.AddCurve(const Point*,INT,INT,INT,REAL), GraphicsPath::AddCurve, GraphicsPath::AddCurve(IN const Point,IN INT,IN INT,IN INT,IN REAL), _gdiplus_CLASS_GraphicsPath_AddCurve_Point_points_INT_count_INT_offset_INT_numberOfSegments_REAL_ten, gdiplus._gdiplus_CLASS_GraphicsPath_AddCurve_Point_points_INT_count_INT_offset_INT_numberOfSegments_REAL_ten
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
 - GraphicsPath.AddCurve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::AddCurve(IN const Point,IN INT,IN INT,IN INT,IN REAL)


## -description


The <b>GraphicsPath::AddCurve</b> method adds a cardinal spline to the current figure of this path.


## -parameters




### -param points [in]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to an array of points that define the cardinal spline. The cardinal spline is a curve that passes through a subset (specified by the <i>offset</i> and <i>numberOfSegments</i> parameters) of the points in the array. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. 


### -param offset [in]

Type: <b>INT</b>

Integer that specifies the index of the array element that is used as the first point of the cardinal spline. 


### -param numberOfSegments [in]

Type: <b>INT</b>

Integer that specifies the number of segments in the cardinal spline. Segments are the curves that connect consecutive points in the array. 


### -param tension [in]

Type: <b>REAL</b>

Nonnegative real number that controls the length of the curve and how the curve bends. A value of 0 specifies that the spline is a sequence of straight line segments. As the value increases, the curve becomes fuller. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



You should keep a copy of the <i>points</i> array if those points will be needed later. The <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object does not store the points passed to the <b>AddClosedCurve</b> method; instead, it converts the cardinal spline to a sequence of Bézier splines and stores the points that define those Bézier splines. You cannot retrieve the original array of points from the 
				<b>GraphicsPath</b> object.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object <i>path</i>, adds a cardinal spline to <i>path</i>, and then draws <i>path</i>. The spline is built from the points indexed 2 through 6 in an array of eight points.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID AddCurveExample2(HDC hdc)
{
   GraphicsPath   path;
   Graphics graphics(hdc);
   
   Point pts[] = {Point(50, 50),
                  Point(70, 80),
                  Point(100, 100),
                  Point(130, 40),
                  Point(150, 90),
                  Point(180, 30),
                  Point(210, 120),
                  Point(240, 80)};
   path.AddCurve(
      pts, 
      8,     // There are eight points in the array. 
      2,     // Start at the point with index 2.
      4,     // Four segments. End at the point with index 6.
      1.0f);
   Pen pen(Color(255, 0, 0, 255));
   graphics.DrawPath(&amp;pen, &amp;path);
   // Draw all eight points in the array.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j &lt;= 7; ++j)
      graphics.FillEllipse(&amp;brush, pts[j].X - 3, pts[j].Y - 3, 6, 6);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1c4f3d1b-1fdb-4fde-8f69-bcfac1a33663">AddBezier Methods</a>



<a href="https://msdn.microsoft.com/fb754409-1867-41bd-a9d3-952e393490f8">AddBeziers Methods</a>



<a href="https://msdn.microsoft.com/5a633a04-1de4-43f5-a898-d30245567e5d">AddClosedCurve Methods</a>



<a href="https://msdn.microsoft.com/81f43f7e-a383-44f7-a3bd-2969d541b616">AddCurve Methods</a>



<a href="https://msdn.microsoft.com/4fc62f00-7006-4ade-bfcc-091a3a97d889">Cardinal Splines</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/0bb84f55-18d0-4a4c-bc5b-7803aa807954">Drawing Cardinal Splines</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>
 

 

