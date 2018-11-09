---
UID: NF:gdiplusbrush.LinearGradientBrush.GetRectangle(OUT Rect)
title: LinearGradientBrush::GetRectangle(OUT Rect)
author: windows-sdk-content
description: The LinearGradientBrush::GetRectangle method gets the rectangle that defines the boundaries of the gradient.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetRectangle_Rect_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\lineargradientbrushgetrectanglemethods\getrectangle.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetRectangle, GetRectangle method [GDI+], GetRectangle method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetRectangle method, LinearGradientBrush.GetRectangle, LinearGradientBrush.GetRectangle(OUT Rect), LinearGradientBrush.GetRectangle(Rect*), LinearGradientBrush::GetRectangle, LinearGradientBrush::GetRectangle(OUT Rect), _gdiplus_CLASS_LinearGradientBrush_GetRectangle_Rect_rect_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetRectangle_Rect_rect_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusbrush.h
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
 - LinearGradientBrush.GetRectangle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::GetRectangle(OUT Rect)


## -description


The <b>LinearGradientBrush::GetRectangle</b> method gets the rectangle that defines the boundaries of the gradient. 


## -parameters




### -param rect [out]

Type: <b><a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a> object that receives the rectangle that defines the boundaries of the gradient. For example, if a linear gradient brush is constructed with a starting point at (20, 50) and an ending point at (60, 110), then the defining rectangle has its upper-left point at (20, 50), a width of 40, and a height of 60. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



The rectangle defines the boundaries of the gradient in the following ways: The right and left sides of the rectangle form the boundaries of a horizontal gradient. The top and bottom sides form the boundaries of a vertical gradient. Two of the diagonally opposing corners lie on the boundaries of a diagonal gradient. In each of these cases, either side/corner may be on the starting boundary, depending on how the starting and ending points are passed to the constructor.


#### Examples



The following example creates a linear gradient brush. Then the code gets the brush's rectangle and draws it.


```cpp
VOID Example_GetRect(HDC hdc)
{
   Graphics myGraphics(hdc);

   // Create a linear gradient brush.
   LinearGradientBrush linGrBrush( 
      Point(20, 10),
      Point(60, 110),
      Color(255, 0, 0, 0),     // black
      Color(255, 0, 0, 255));  // blue

   // Obtain information about the linear gradient brush.
   Rect rect;
   linGrBrush.GetRectangle(&rect);

   // Draw the retrieved rectangle.
   Pen myPen(Color(255, 0, 0, 0));
   myGraphics.DrawRectangle(&myPen, rect);
}
```





## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/9b0236b2-be6b-4918-a106-5b0e6c3dd5ff">Creating a Linear Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a>



<a href="https://msdn.microsoft.com/d91562ab-41e6-4bca-a320-74f490a4f88f">Pens, Lines, and Rectangles</a>



<a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>



<a href="https://msdn.microsoft.com/f2e4144f-f2f1-49db-bfdf-ffce3023b4cb">Using a Pen to Draw Lines and Rectangles</a>
 

 

