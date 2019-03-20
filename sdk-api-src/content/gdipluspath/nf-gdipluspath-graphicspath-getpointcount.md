---
UID: NF:gdipluspath.GraphicsPath.GetPointCount
title: GraphicsPath::GetPointCount (gdipluspath.h)
author: windows-sdk-content
description: The GraphicsPath::GetPointCount method gets the number of points in this path's array of data points. This is the same as the number of types in the path's array of point types.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPointCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getpointcount.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPointCount, GetPointCount method [GDI+], GetPointCount method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPointCount method, GraphicsPath.GetPointCount, GraphicsPath::GetPointCount, _gdiplus_CLASS_GraphicsPath_GetPointCount_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPointCount_
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
 - GraphicsPath.GetPointCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::GetPointCount


## -description


The <b>GraphicsPath::GetPointCount</b> method gets the number of points in this path's array of data points. This is the same as the number of types in the path's array of point types.


## -parameters






## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of points in the path's array of data points.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a> enumeration.


#### Examples



The following example creates a path that has one ellipse and one line. The code calls the <b>GraphicsPath::GetPointCount</b> method to determine the number of data points stored in the path. Then the code calls the <a href="https://msdn.microsoft.com/en-us/library/ms535581(v=VS.85).aspx">GraphicsPath::GetPathPoints</a> method to retrieve those data points. Finally, the code fills a small ellipse at each of the data points.


```cpp
VOID GetPointCountExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has one ellipse and one line.
   GraphicsPath path;
   path.AddEllipse(10, 10, 200, 100);
   path.AddLine(220, 120, 300, 160);

   // Find out how many data points are stored in the path.
   INT count = path.GetPointCount();

   // Draw the path points.
   SolidBrush redBrush(Color(255, 255, 0, 0));
   PointF* points = new PointF[count];
   path.GetPathPoints(points, count);

   for(INT j = 0; j < count; ++j)
      graphics.FillEllipse(
         &redBrush, 
         points[j].X - 3.0f, 
         points[j].Y - 3.0f, 
         6.0f, 
         6.0f); 

   delete [] points; 
} 
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535561(v=VS.85).aspx">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535534(v=VS.85).aspx">GraphicsPath::GetPathData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535535(v=VS.85).aspx">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534481(v=VS.85).aspx">PathData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

