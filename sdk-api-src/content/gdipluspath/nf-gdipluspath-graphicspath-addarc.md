---
UID: NF:gdipluspath.GraphicsPath.AddArc
title: GraphicsPath::AddArc
description: The GraphicsPath::AddArc method adds an elliptical arc to the current figure of this path.
ms.assetid: 2616a8ff-8193-413b-ab7f-56c0dd82c17b
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddArc
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
 - GraphicsPath::AddArc
---

#  GraphicsPath::AddArc

## -description

The **GraphicsPath::AddArc** method adds an elliptical arc to the current figure of this path.

## -parameters

### -param rect

Reference to a rectangle that bounds the ellipse that contains the arc.

### -param startAngle

Real number that specifies the clockwise angle, in degrees, between the horizontal axis of the ellipse and the starting point of the arc.

### -param sweepAngle

Real number that specifies the clockwise angle, in degrees, between the starting point (startAngle) and the ending point of the arc.

## -returns

**Type:** <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object *path*, adds an arc to *path*, closes the arc, and then draws *path*.

```cpp
VOID AddArcExample(HDC hdc)
{
   Graphics graphics(hdc);
   RectF rect(20.0f, 20.0f, 50.0f, 100.0f);

   GraphicsPath path;
   path.AddArc(rect, 0.0f, 180.0f);
   path.CloseFigure();

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms535537(v=VS.85).aspx">AddArc Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535733(v=VS.85).aspx">DrawArc Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536362(v=VS.85).aspx">Ellipses and Arcs</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>
