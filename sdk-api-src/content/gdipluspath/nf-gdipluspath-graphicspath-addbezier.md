---
UID: NF:gdipluspath.GraphicsPath.AddBezier
title: GraphicsPath::AddBezier
description: The GraphicsPath::AddBezier method adds a Bezier spline to the current figure of this path.
ms.assetid: 9ab28c47-f72b-472e-8b8e-22f4839a0b42
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddBezier
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdipluspath.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPath::AddBezier
---

# GraphicsPath::AddBezier

## -description

The **GraphicsPath::AddBezier** method adds a Bézier spline to the current figure of this path.

## -parameters

### -param pt1

Reference to a point at which to start the Bézier spline.

### -param pt2

Reference to a point that is the first control point of the Bézier spline.

### -param pt3

Reference to a point that is the second control point of the Bézier spline.

### -param pt4

Reference to a point at which to end the Bézier spline.

## -returns

**Type:** <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object path, adds a Bézier spline to path, closes the current figure (the only figure in this case), and then draws path.

```cpp
VOID Example_AddBezier(HDC hdc)
{
   Graphics graphics(hdc);
   GraphicsPath  path;

   PointF pt1(50.0f, 50.0f); 
   PointF pt2(60.0f, 20.0f);
   PointF pt3(70.0f, 100.0f); 
   PointF pt4(80.0f, 50.0f);

   path.AddBezier(pt1, pt2, pt3, pt4);
   path.CloseFigure();

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms535538(v=VS.85).aspx">AddBezier Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535539(v=VS.85).aspx">AddBeziers Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535541(v=VS.85).aspx">AddCurve Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536354(v=VS.85).aspx">Bézier Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533926(v=VS.85).aspx">Drawing Bézier Splines</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
