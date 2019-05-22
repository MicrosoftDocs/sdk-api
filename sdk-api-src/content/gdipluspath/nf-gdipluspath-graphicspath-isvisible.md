---
UID: NF:gdipluspath.GraphicsPath.IsVisible
title: GraphicsPath::IsVisible
description: The GraphicsPath::IsVisible method determines whether a specified point lies in an area.
ms.assetid: 0065e994-f6a0-47ea-a6c0-ab496f90f061
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: GraphicsPath::IsVisible
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
 - GraphicsPath::IsVisible
---

# GraphicsPath::IsVisible

## -description

The **GraphicsPath::IsVisible** method determines whether a specified point lies in the area that is filled when this path is filled by a specified <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.

## -parameters

### -param point

Reference to the point to be tested.

### -param g

Optional.
Pointer to a **Graphics** object that specifies a world-to-device transformation.
If the value of this parameter is **NULL**, the test is done in world coordinates; otherwise, the test is done in device coordinates.
The default value is **NULL**.

## -returns

If the test point lies in the interior of this path, this method returns **TRUE**; otherwise, it returns **FALSE**.

## -remarks

#### Examples

The following example creates an elliptical path and draws that path with a narrow black pen.
Then the code tests each point in an array to see whether the point lies in the interior of the path.
Points that lie in the interior are painted green, and points that do not lie in the interior are painted red.

```cpp
VOID IsVisibleExample(HDC hdc)
{
   Graphics graphics(hdc);

   INT j;
   Pen blackPen(Color(255, 0, 0, 0), 1);
   SolidBrush brush(Color(255, 255, 0,  0));

   // Create and draw a path.
   GraphicsPath path;
   path.AddEllipse(50, 50, 200, 100);
   graphics.DrawPath(&blackPen, &path);

   // Create an array of four points, and determine whether each
   // point in the array touches the outline of the path.
   // If a point touches the outline, paint it green.
   // If a point does not touch the outline, paint it red.
   PointF[] = {
      PointF(50, 100),
      PointF(250, 100),
      PointF(150, 170),
      PointF(180, 60)};

   for(j = 0; j <= 3; ++j)
   {
      if(path.IsVisible(points[j], &graphics))
         brush.SetColor(Color(255, 0, 255,  0));
      else
         brush.SetColor(Color(255, 255, 0,  0));

      graphics.FillEllipse(&brush, points[j].X - 3.0f, points[j].Y - 3.0f, 6.0f, 6.0f);
   }
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535562(v=VS.85).aspx">IsOutlineVisible Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms535563(v=VS.85).aspx">IsVisible Methods</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
