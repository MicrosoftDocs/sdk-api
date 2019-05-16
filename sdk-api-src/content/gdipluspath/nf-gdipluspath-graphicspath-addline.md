---
UID: NF:gdipluspath.GraphicsPath.AddLine
title: GraphicsPath::AddLine
description: The GraphicsPath::AddLine method adds a line to the current figure of this path.
ms.assetid: edb6b196-e8f0-4ddd-830b-ff740a94369a
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddLine
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
 - GraphicsPath::AddLine
---
#  GraphicsPath::AddLine

## -description

The **GraphicsPath::AddLine** method adds a line to the current figure of this path.

## -parameters

### -param pt1

Reference to a point at which to start the line.

### -param pt2

Reference to a point at which to end the line.

## -returns

**Type:** <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

## -remarks

#### Examples

The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object path, adds a line to path, and then draws path.

```cpp
VOID Example_AddLine(HDC hdc)
{
   Graphics graphics(hdc);

   PointF point1(20.0f, 20.0f);
   PointF point2(100.0f, 100.0f);

   GraphicsPath path;
   path.AddLine(point1, point2);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms535543(v=VS.85).aspx">AddLine Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535544(v=VS.85).aspx">AddLines Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
