---
UID: NF:gdiplusgraphics.Graphics.FillEllipse
title: Graphics::FillEllipse
description: The **Graphics::FillEllipse** method uses a brush to fill the interior of an ellipse that is specified by a rectangle.
ms.assetid: a89598db-a1b9-404a-a2bc-1a0a94afb8d4
ms.author: windowssdkdev
ms.date: 05/13/2019
ms.keywords: Graphics::FillEllipse
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
 - Graphics::FillEllipse
---

# FillEllipse(Brush*,RectF&)

## -description

The **Graphics::FillEllipse** method uses a brush to fill the interior of an ellipse that is specified by a rectangle.

## -parameters

### -param brush

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a> object that is used to paint the interior of the ellipse.

### -param rect

Reference to a rectangle that specifies the boundaries of the ellipse.

## -returns

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the **Status** enumeration.

## -remarks

#### Examples

The following example fills an ellipse defined by a bounding rectangle.

```cpp
VOID Example_FillEllipse2(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a SolidBrush object.
   SolidBrush blackBrush(Color(255, 0, 0, 0));

   // Create the RectF object that defines the ellipse.
   RectF ellipseRect(0.0f, 0.6f, 200.8f, 100.9f);

   // Fill the ellipse.
   graphics.FillEllipse(&blackBrush, ellipseRect);
}
```

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/ms534424(v=VS.85).aspx">Brush</a>

<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>

<a href="https://msdn.microsoft.com/en-us/library/ms534497(v=VS.85).aspx">RectF</a>

<a href="https://msdn.microsoft.com/en-us/library/ms533811(v=VS.85).aspx">Using a Brush to Fill Shapes</a>
