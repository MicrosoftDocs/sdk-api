---
UID: NF:gdipluspath.PathGradientBrush.GetCenterPoint(OUT Point)
title: PathGradientBrush::GetCenterPoint(OUT Point)
author: windows-sdk-content
description: The PathGradientBrush::GetCenterPoint method gets the center point of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushgetcenterpointmethods\getcenterpoint.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetCenterPoint, GetCenterPoint method [GDI+], GetCenterPoint method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetCenterPoint method, PathGradientBrush.GetCenterPoint, PathGradientBrush.GetCenterPoint(OUT Point), PathGradientBrush.GetCenterPoint(Point*), PathGradientBrush::GetCenterPoint, PathGradientBrush::GetCenterPoint(OUT Point), _gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_
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
 - PathGradientBrush.GetCenterPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::GetCenterPoint(OUT Point)


## -description


The <b>PathGradientBrush::GetCenterPoint</b> method gets the center point of this path gradient brush.


## -parameters




### -param point [out]

Type: <b><a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> object that receives the center point. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



By default, the center point of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a> object is at the centroid of the brush's boundary path, but you can set the center point to any location, inside or outside the path, by calling the 
				<a href="https://msdn.microsoft.com/41765887-b1de-4259-95af-a1ef8c84d01a">SetCenterPoint</a> method of the 
				<b>PathGradientBrush</b> object.


#### Examples



The following example demonstrates several methods of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a> class including <b>PathGradientBrush::GetCenterPoint</b> and <a href="https://msdn.microsoft.com/33e9a8f0-7c07-475d-8332-cf2e08190b35">PathGradientBrush::SetCenterColor</a>. The code creates a 
						<b>PathGradientBrush</b> object and then sets the brush's center color and boundary color. The code calls the <b>PathGradientBrush::GetCenterPoint</b> method to determine the center point of the path gradient brush and then draws a line from the origin to that center point.


```cpp
VOID Example_GetCenterPoint(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that consists of a single ellipse.
   GraphicsPath path;
   path.AddEllipse(0, 0, 200, 100);

   // Use the path to construct a brush.
   PathGradientBrush pthGrBrush(&path);

   // Set the color at the center of the path to blue.
   pthGrBrush.SetCenterColor(Color(255, 0, 0, 255));

   // Set the color along the entire boundary of the path to aqua.
   Color colors[] = {Color(255, 0, 255, 255)};
   INT count = 1;
   pthGrBrush.SetSurroundColors(colors, &count);

   // Fill the ellipse with the path gradient brush.
   graphics.FillEllipse(&pthGrBrush, 0, 0, 200, 100);

   // Obtain information about the path gradient brush.
   Point  centerPoint;
   pthGrBrush.GetCenterPoint(&centerPoint);

   // Draw a line from the origin to the center of the ellipse.
   Pen pen(Color(255, 0, 255, 0));
   graphics.DrawLine(&pen, Point(0, 0), centerPoint);
}
```





## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/b5b79732-f89a-46fb-b7ac-2eb45f7d4f87">PathGradientBrush::GetCenterColor</a>



<a href="https://msdn.microsoft.com/33e9a8f0-7c07-475d-8332-cf2e08190b35">PathGradientBrush::SetCenterColor</a>



<a href="https://msdn.microsoft.com/41765887-b1de-4259-95af-a1ef8c84d01a">PathGradientBrush::SetCenterPoint Methods</a>
 

 

