---
UID: NF:gdiplusgraphics.Graphics.TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT)
title: Graphics::TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT)
author: windows-sdk-content
description: The Graphics::TransformPoints method converts an array of points from one coordinate space to another. The conversion is based on the current world and page transformations of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\transformpoints.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Graphics class [GDI+],TransformPoints method, Graphics.TransformPoints, Graphics.TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT), Graphics::TransformPoints, Graphics::TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT), TransformPoints, TransformPoints method [GDI+], TransformPoints method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_, gdiplus._gdiplus_CLASS_Graphics_TransformPoints_destSpace_srcSpace_pts_count_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusgraphics.h
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.TransformPoints
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::TransformPoints(IN CoordinateSpace,IN CoordinateSpace,IN OUT Point,IN INT)


## -description


The <b>Graphics::TransformPoints</b> method converts an array of points from one coordinate space to another. The conversion is based on the current world and page transformations of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object.


## -parameters




### -param destSpace [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534097(v=VS.85).aspx">CoordinateSpace</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534097(v=VS.85).aspx">CoordinateSpace</a> enumeration that specifies the destination coordinate space. 


### -param srcSpace [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534097(v=VS.85).aspx">CoordinateSpace</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534097(v=VS.85).aspx">CoordinateSpace</a> enumeration that specifies the source coordinate space. 


### -param pts [in, out]

Type: <b><a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to an array that, on input, holds the points to be converted and, on output, holds the converted points. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>pts</i> array. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The world transformation converts points from the world coordinate space to the page coordinate space. The page transformation converts points from the page coordinate space to the device coordinate space. For more information about coordinate spaces, see <a href="https://msdn.microsoft.com/en-us/library/ms536399(v=VS.85).aspx">Types of Coordinate Systems</a>.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object and sets its world transformation to a translation 40 units right and 30 units down. Then the code creates an array of points and passes the address of that array to the <b>Graphics::TransformPoints</b> method of the same <b>Graphics</b> object. The points in the array are transformed by the world transformation of the <b>Graphics</b> object. The code calls the <a href="https://msdn.microsoft.com/en-us/library/ms536020(v=VS.85).aspx">Graphics::DrawLine</a> method twice: once to connect the two points before the transformation and once to connect the two points after the transformation.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_TransformPoints(HDC hdc)
{
   Graphics graphics(hdc);
   Pen pen(Color(255, 0, 0, 255));

   // Create an array of two Point objects.
   Point points[2] = {Point(0, 0), Point(100, 50)};

   // Draw a line that connects the two points.
   // No transformation has been performed yet.
   graphics.DrawLine(&amp;pen, points[0], points[1]);

   // Set the world transformation of the Graphics object.
   graphics.TranslateTransform(40.0f, 30.0f);

   // Transform the points in the array from world to page coordinates.
   graphics.TransformPoints(
      CoordinateSpacePage, 
      CoordinateSpaceWorld, 
      points, 
      2);

   // It is the world transformation that takes points from world
   // space to page space. Because the world transformation is a
   // translation 40 to the right and 30 down, the
   // points in the array are now (40, 30) and (140, 80).

   // Draw a line that connects the transformed points.
   graphics.ResetTransform();
   graphics.DrawLine(&amp;pen, points[0], points[1]);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535729(v=VS.85).aspx">Graphics::GetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535800(v=VS.85).aspx">Graphics::MultiplyTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535803(v=VS.85).aspx">Graphics::ResetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535805(v=VS.85).aspx">Graphics::RotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535807(v=VS.85).aspx">Graphics::ScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535818(v=VS.85).aspx">Graphics::SetTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535820(v=VS.85).aspx">Graphics::TranslateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534149(v=VS.85).aspx">MatrixOrder</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533810(v=VS.85).aspx">Transformations</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536399(v=VS.85).aspx">Types of Coordinate Systems</a>
 

 

