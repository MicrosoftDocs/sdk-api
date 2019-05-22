---
UID: NF:gdiplusgraphics.Graphics.DrawLines
title: Graphics::DrawLines
description: The Graphics::DrawLines method draws a sequence of connected lines.
ms.assetid: ea0d1b7b-f278-4a44-a99f-77801031d51e
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::DrawLines
ms.topic: language-reference
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusgraphics.h
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
 - gdiplusgraphics.h
api_name:
 - Graphics::DrawLines
---

# DrawLines(Pen*,PointF*,INT)

## -description

The **Graphics::DrawLines** method draws a sequence of connected lines.

## -parameters

### -param pen

Pointer to a pen that is used to draw the lines.

### -param points

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a> objects that specify the starting and ending points of the lines.

### -param count

Integer that specifies the number of elements in the *points* array.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example draws a sequence of connected lines.

```cpp
VOID Example_DrawLines2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a Pen object.
   Pen blackPen(Color(255, 0, 0, 0), 3);

   // Create an array of PointF objects that define the lines to draw.
   PointF point1(10.0f, 10.0f);
   PointF point2(10.0f, 100.0f);
   PointF point3(200.0f, 50.0f);
   PointF point4(250.0f, 300.0f);

   PointF points[4] = {point1, point2, point3, point4};
   PointF* pPoints = points;

   // Draw the lines.
   graphics.DrawLines(&blackPen, pPoints, 4);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms535748(v=VS.85).aspx">DrawLine Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536372(v=VS.85).aspx">Pens, Lines, and Rectangles</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533855(v=VS.85).aspx">Using a Pen to Draw Lines and Rectangles</a>
