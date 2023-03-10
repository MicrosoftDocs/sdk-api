---
UID: NF:gdipluspath.PathGradientBrush.GetCenterPoint(Point)
title: PathGradientBrush::GetCenterPoint(OUT Point) (gdipluspath.h)
description: The PathGradientBrush::GetCenterPoint method gets the center point of this path gradient brush. (overload 1/2)
helpviewer_keywords: ["GetCenterPoint","GetCenterPoint method [GDI+]","GetCenterPoint method [GDI+]","PathGradientBrush class","PathGradientBrush class [GDI+]","GetCenterPoint method","PathGradientBrush.GetCenterPoint","PathGradientBrush.GetCenterPoint(OUT Point)","PathGradientBrush.GetCenterPoint(Point*)","PathGradientBrush::GetCenterPoint","PathGradientBrush::GetCenterPoint(OUT Point)","_gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_","gdiplus._gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_"]
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\pathgradientbrushgetcenterpointmethods\getcenterpoint.htm
ms.date: 12/05/2018
ms.keywords: GetCenterPoint, GetCenterPoint method [GDI+], GetCenterPoint method [GDI+],PathGradientBrush class, PathGradientBrush class [GDI+],GetCenterPoint method, PathGradientBrush.GetCenterPoint, PathGradientBrush.GetCenterPoint(OUT Point), PathGradientBrush.GetCenterPoint(Point*), PathGradientBrush::GetCenterPoint, PathGradientBrush::GetCenterPoint(OUT Point), _gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_, gdiplus._gdiplus_CLASS_PathGradientBrush_GetCenterPoint_Point_point_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - PathGradientBrush::GetCenterPoint
 - gdipluspath/PathGradientBrush::GetCenterPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.GetCenterPoint
---

# PathGradientBrush::GetCenterPoint(OUT Point)


## -description

The <b>PathGradientBrush::GetCenterPoint</b> method gets the center point of this path gradient brush.

## -parameters

### -param point [out]

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object that receives the center point.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

By default, the center point of a 
				<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> object is at the centroid of the brush's boundary path, but you can set the center point to any location, inside or outside the path, by calling the 
				<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)">SetCenterPoint</a> method of the 
				<b>PathGradientBrush</b> object.


#### Examples



The following example demonstrates several methods of the 
						<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a> class including <b>PathGradientBrush::GetCenterPoint</b> and <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor">PathGradientBrush::SetCenterColor</a>. The code creates a 
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

<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-filling-a-shape-with-a-color-gradient-use">Filling a Shape with a Color Gradient</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-getcentercolor">PathGradientBrush::GetCenterColor</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcentercolor">PathGradientBrush::SetCenterColor</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-pathgradientbrush-setcenterpoint(inconstpoint_)">PathGradientBrush::SetCenterPoint Methods</a>
