---
UID: NF:gdipluspath.PathGradientBrush.SetCenterColor
title: PathGradientBrush::SetCenterColor
author: windows-sdk-content
description: The PathGradientBrush::SetCenterColor method sets the center color of this path gradient brush. The center color is the color that appears at the brush's center point.
old-location: gdiplus\_gdiplus_CLASS_PathGradientBrush_SetCenterColor_color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathgradientbrushclass\pathgradientbrushmethods\setcentercolor.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PathGradientBrush class [GDI+],SetCenterColor method, PathGradientBrush.SetCenterColor, PathGradientBrush::SetCenterColor, SetCenterColor, SetCenterColor method [GDI+], SetCenterColor method [GDI+],PathGradientBrush class, _gdiplus_CLASS_PathGradientBrush_SetCenterColor_color_, gdiplus._gdiplus_CLASS_PathGradientBrush_SetCenterColor_color_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - PathGradientBrush.SetCenterColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PathGradientBrush::SetCenterColor


## -description


The <b>PathGradientBrush::SetCenterColor</b> method sets the center color of this path gradient brush. The center color is the color that appears at the brush's center point.


## -parameters




### -param color [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a> object that specifies the center color. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



By default the center point is the centroid of the brush's boundary path, but you can set the center point to any location inside or outside the path.


#### Examples



The following example creates a 
						<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>object based on an ellipse. The code calls the <b>PathGradientBrush::SetCenterColor</b> method of the 
						<b>PathGradientBrush</b>object to set the center color to blue. The 
						<a href="https://msdn.microsoft.com/en-us/library/ms535090(v=VS.85).aspx">PathGradientBrush::SetSurroundColors</a> method sets the color along the entire boundary to aqua. The 
						<a href="https://msdn.microsoft.com/en-us/library/ms535773(v=VS.85).aspx">FillRectangle Methods</a> method uses the path gradient brush to paint a rectangle that contains the ellipse.


```cpp
VOID Example_SetCenter(HDC hdc)
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

   graphics.FillRectangle(&pthGrBrush, 0, 0, 300, 300); 
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534427(v=VS.85).aspx">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534483(v=VS.85).aspx">PathGradientBrush</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535064(v=VS.85).aspx">PathGradientBrush::GetCenterColor</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535076(v=VS.85).aspx">PathGradientBrush::GetCenterPoint Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535078(v=VS.85).aspx">PathGradientBrush::SetCenterPoint Methods</a>
 

 

