---
UID: NF:gdipluspath.GraphicsPath.GetPointCount
title: GraphicsPath::GetPointCount
author: windows-sdk-content
description: The GraphicsPath::GetPointCount method gets the number of points in this path's array of data points. This is the same as the number of types in the path's array of point types.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPointCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getpointcount.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPointCount, GetPointCount method [GDI+], GetPointCount method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPointCount method, GraphicsPath.GetPointCount, GraphicsPath::GetPointCount, _gdiplus_CLASS_GraphicsPath_GetPointCount_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPointCount_
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



A <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a> enumeration.


#### Examples



The following example creates a path that has one ellipse and one line. The code calls the <b>GraphicsPath::GetPointCount</b> method to determine the number of data points stored in the path. Then the code calls the <a href="https://msdn.microsoft.com/4f797bdb-16c3-4d49-9c00-cae431fa35bc">GraphicsPath::GetPathPoints</a> method to retrieve those data points. Finally, the code fills a small ellipse at each of the data points.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID GetPointCountExample(HDC hdc)
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

   for(INT j = 0; j &lt; count; ++j)
      graphics.FillEllipse(
         &amp;redBrush, 
         points[j].X - 3.0f, 
         points[j].Y - 3.0f, 
         6.0f, 
         6.0f); 

   delete [] points; 
} </pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/65a9d308-e1b7-40c4-a079-2ec9d9a5cae3">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/c757cfb8-25fe-4881-96b3-5257f925b781">GraphicsPath::GetPathData</a>



<a href="https://msdn.microsoft.com/fded6e62-0134-4e2c-aa40-cf0a32a5b2f2">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/b8e9a4cb-72e1-4646-956a-50801176a3bd">PathData</a>



<a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

