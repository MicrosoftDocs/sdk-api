---
UID: NF:gdipluspath.PathGradientBrush.GetCenterPoint(OUT Point)
title: PathGradientBrush::GetCenterPoint(OUT Point) (gdipluspath.h)
author: windows-sdk-content
description: The PathGradientBrush::GetCenterPoint method gets the center point of this path gradient brush.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushgetcenterpointmethods\getcenterpoint.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCenterPoint, GetCenterPoint method [GDI+], GetCenterPoint method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetCenterPoint method, PathGradientBrush.GetCenterPoint, PathGradientBrush.GetCenterPoint(OUT Point), PathGradientBrush.GetCenterPoint(Point*), PathGradientBrush::GetCenterPoint, PathGradientBrush::GetCenterPoint(OUT Point), _gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_
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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>*</b>

Pointer to a 
					<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a> object that receives the center point. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



By default, the center point of a 
				<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a> object is at the centroid of the brush's boundary path, but you can set the center point to any location, inside or outside the path, by calling the 
				<a href="https://msdn.microsoft.com/en-us/library/ms535078(v=VS.85).aspx">SetCenterPoint</a> method of the 
				<b>PathGradientBrush</b> object.


#### Examples



The following example demonstrates several methods of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a> class including <b>PathGradientBrush::GetCenterPoint</b> and <a href="https://msdn.microsoft.com/en-us/library/ms535085(v=VS.85).aspx">PathGradientBrush::SetCenterColor</a>. The code creates a 
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




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535064(v=VS.85).aspx">PathGradientBrush::GetCenterColor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535085(v=VS.85).aspx">PathGradientBrush::SetCenterColor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535078(v=VS.85).aspx">PathGradientBrush::SetCenterPoint Methods</a>
 

 

