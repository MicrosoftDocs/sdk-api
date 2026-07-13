---
UID: NF:gdipluspath.GraphicsPath.AddClosedCurve(constPoint,INT)
title: GraphicsPath::AddClosedCurve(IN const Point,IN INT) (gdipluspath.h)
description: The GraphicsPath::AddClosedCurve method adds a closed cardinal spline to this path. (overload 2/4)
helpviewer_keywords: ["AddClosedCurve","AddClosedCurve method [GDI+]","AddClosedCurve method [GDI+]","GraphicsPath class","GraphicsPath class [GDI+]","AddClosedCurve method","GraphicsPath.AddClosedCurve","GraphicsPath.AddClosedCurve(IN const Point","IN INT)","GraphicsPath.AddClosedCurve(const Point*","INT)","GraphicsPath::AddClosedCurve","GraphicsPath::AddClosedCurve(IN const Point","IN INT)","_gdiplus_CLASS_GraphicsPath_AddClosedCurve_Point_points_INT_count_","gdiplus._gdiplus_CLASS_GraphicsPath_AddClosedCurve_Point_points_INT_count_"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_AddClosedCurve_Point_points_INT_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\graphicspathaddclosedcurvemethods\addclosedcurve.htm
ms.date: 12/05/2018
ms.keywords: AddClosedCurve, AddClosedCurve method [GDI+], AddClosedCurve method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],AddClosedCurve method, GraphicsPath.AddClosedCurve, GraphicsPath.AddClosedCurve(IN const Point,IN INT), GraphicsPath.AddClosedCurve(const Point*,INT), GraphicsPath::AddClosedCurve, GraphicsPath::AddClosedCurve(IN const Point,IN INT), _gdiplus_CLASS_GraphicsPath_AddClosedCurve_Point_points_INT_count_, gdiplus._gdiplus_CLASS_GraphicsPath_AddClosedCurve_Point_points_INT_count_
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
 - GraphicsPath::AddClosedCurve
 - gdipluspath/GraphicsPath::AddClosedCurve
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
 - GraphicsPath.AddClosedCurve
---

# GraphicsPath::AddClosedCurve(IN const Point,IN INT)


## -description

The <b>GraphicsPath::AddClosedCurve</b> method adds a closed cardinal spline to this path.

## -parameters

### -param points [in]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>*</b>

Pointer to an array of points that define the cardinal spline. The cardinal spline is a curve that passes through each point in the array.

### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

You should keep a copy of the 
				<i>points</i> array if those points will be needed later. The <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object does not store the points passed to the <b>GraphicsPath::AddClosedCurve</b> method; instead, it converts the cardinal spline to a sequence of Bézier splines and stores the points that define those Bézier splines. You cannot retrieve the original array of points from the <b>GraphicsPath</b> object. 


#### Examples



The following example creates a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object <i>path</i>, adds a closed cardinal spline to <i>path</i>, and then draws <i>path</i>.


```cpp
VOID Example_AddClosedCurve(HDC hdc)
{
   Graphics graphics(hdc); 

   Point pts[] = {Point(50,50),
                  Point(60,20),
                  Point(70,100),
                  Point(80,50)};

   GraphicsPath path;
   path.AddClosedCurve(pts, 4);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inconstpoint__inconstpoint__inconstpoint__inconstpoint_)">AddBezier Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpoint_inint)">AddBeziers Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint_inreal)">AddClosedCurve Methods</a>



<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpointf_inint_inint_inint_inreal)">AddCurve Methods</a>



<a href="/windows/desktop/gdiplus/-gdiplus-cardinal-splines-about">Cardinal Splines</a>



<a href="/windows/desktop/gdiplus/-gdiplus-clipping-with-a-region-use">Clipping with a Region</a>



<a href="/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="/windows/desktop/gdiplus/-gdiplus-creating-a-path-gradient-use">Creating a Path Gradient</a>



<a href="/windows/desktop/gdiplus/-gdiplus-drawing-cardinal-splines-use">Drawing Cardinal Splines</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a>
