---
UID: NF:gdipluspath.GraphicsPath.AddEllipse
title: GraphicsPath::AddEllipse
description: The GraphicsPath::AddEllipse method adds an ellipse to this path.
ms.assetid: 9acdbd19-0354-4728-a96c-611b93cbffe5
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: GraphicsPath::AddEllipse
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
 - GraphicsPath::AddEllipse
---

# GraphicsPath::AddEllipse

## -description

The **GraphicsPath::AddEllipse** method adds an ellipse to this path.

## -parameters

### -param rect

Reference to a rectangle that bounds the ellipse.

## -returns

**Type:** <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

## -remarks

A <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object stores an ellipse as a sequence of four connected Bézier splines.
The **GraphicsPath** object does not store the upper-left corner, width, and height of the ellipse's bounding rectangle.

#### Examples

The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object path, adds an ellipse to path, and then draws path.

```cpp
VOID Example_AddEllipse(HDC hdc)
{
   Graphics graphics(hdc); 
   RectF rect(20.0f, 20.0f, 200.0f, 100.0f);

   GraphicsPath path;
   path.AddEllipse(rect);

   // Draw the path.
   Pen pen(Color(255, 255, 0, 0));
   graphics.DrawPath(&pen, &path);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms535537(v=VS.85).aspx">AddArc Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535542(v=VS.85).aspx">AddEllipse Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536362(v=VS.85).aspx">Ellipses and Arcs</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>
