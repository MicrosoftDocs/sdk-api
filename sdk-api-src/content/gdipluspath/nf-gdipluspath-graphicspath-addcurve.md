---
UID: NF:gdipluspath.GraphicsPath.AddCurve
title: GraphicsPath::AddCurve
description: The GraphicsPath::AddCurve method adds a cardinal spline to the current figure of this path.
ms.assetid: bcd96b35-e6f5-42c6-8e08-185aad503453
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddCurve
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
 - GraphicsPath::AddCurve
---

# GraphicsPath::AddCurve

## -description

The **GraphicsPath::AddCurve** method adds a cardinal spline to the current figure of this path.

## -parameters

### -param points

Pointer to an array of points that define the cardinal spline.
The cardinal spline is a curve that passes through each point in the array.

### -param count

Integer that specifies the number of elements in the points array.

## -returns

**Type:** <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

## -remarks

You should keep a copy of the points array if those points will be needed later.
The **GraphicsPath** object does not store the points passed to the **AddClosedCurve** method; instead, it converts the cardinal spline to a sequence of Bézier splines and stores the points that define those Bézier splines.
You cannot retrieve the original array of points from the GraphicsPath object.

#### Examples

The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object path, adds a cardinal spline to path, and then draws path.

```cpp
VOID AddCurveExample(HDC hdc)
{
   Graphics graphics(hdc);
   PointF pts[] = {PointF(50.0f, 50.0f),
                   PointF(60.0f, 20.0f),
                   PointF(70.0f, 100.0f),
                   PointF(80.0f, 50.0f)};
   GraphicsPath path;
   path.AddCurve(pts, 4);
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

<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>
