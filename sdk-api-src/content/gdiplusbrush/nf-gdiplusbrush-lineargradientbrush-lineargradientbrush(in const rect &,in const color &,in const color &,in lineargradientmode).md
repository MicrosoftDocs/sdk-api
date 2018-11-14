---
UID: NF:gdiplusbrush.LinearGradientBrush.LinearGradientBrush(IN const Rect &,IN const Color &,IN const Color &,IN LinearGradientMode)
title: LinearGradientBrush::LinearGradientBrush(IN const Rect &,IN const Color &,IN const Color &,IN LinearGradientMode)
author: windows-sdk-content
description: Creates a LinearGradientBrush::LinearGradientBrush object based on a rectangle and mode of direction.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_Rect_rect_Color_color1_Color_color2_LinearGra.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushconstructors\lineargradientbrush_87rectamprect_colorampcolor1_colorampcol.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: LinearGradientBrush, LinearGradientBrush class [GDI+],LinearGradientBrush constructor, LinearGradientBrush constructor [GDI+], LinearGradientBrush constructor [GDI+],LinearGradientBrush class, LinearGradientBrush.LinearGradientBrush, LinearGradientBrush.LinearGradientBrush(IN const Rect &,IN const Color &,IN const Color &,IN LinearGradientMode), LinearGradientBrush.LinearGradientBrush(const Rect&,const Color&,const Color&,LinearGradientMode), LinearGradientBrush::LinearGradientBrush, LinearGradientBrush::LinearGradientBrush(IN const Rect &,IN const Color &,IN const Color &,IN LinearGradientMode), _gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_Rect_rect_Color_color1_Color_color2_LinearGra, gdiplus._gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_Rect_rect_Color_color1_Color_color2_LinearGra
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
 - LinearGradientBrush.LinearGradientBrush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusbrush.h
: 
- LinearGradientBrush.LinearGradientBrush
: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::LinearGradientBrush(IN const Rect &,IN const Color &,IN const Color &,IN LinearGradientMode)


## -description


Creates a <b>LinearGradientBrush::LinearGradientBrush</b> object based on a rectangle and mode of direction.


## -parameters




### -param rect [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a></b>

Reference to a rectangle that specifies the starting and ending points of the gradient. The direction of the gradient, specified by <i>mode</i>, affects how these points are defined. The dimensions of the rectangle affect the direction of the gradient for forward diagonal mode and backward diagonal mode. 


### -param color1 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color at the starting boundary line of this linear gradient brush. 


### -param color2 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color at the ending boundary line of this linear gradient brush. 


### -param mode [in]

Type: <b><a href="https://msdn.microsoft.com/ad3cce3d-67f3-4f7a-84d0-4319425de07a">LinearGradientMode</a></b>

Element of the <a href="https://msdn.microsoft.com/ad3cce3d-67f3-4f7a-84d0-4319425de07a">LinearGradientMode</a> enumeration that specifies the direction of the gradient. 


## -remarks



The starting boundary of the gradient is a straight line that either passes through the starting point or borders the rectangle <i>rect</i>. The ending boundary of the gradient is a straight line that is parallel to the starting boundary line and that either passes through the ending point or borders the rectangle. The "directional line," an imaginary straight line, is perpendicular to the boundary lines. The gradient color is constant along lines that are parallel to the boundary lines. The gradient gradually changes from the starting color to the ending color along the directional line. 

The mode affects the boundaries of the gradient: 

<ul>
<li>Vertical mode 
							The boundary lines are parallel to the top (and bottom) of the rectangle <i>rect</i>. The starting and ending boundary lines are the top and bottom, respectively, of the rectangle <i>rect</i>. 

</li>
<li>Horizontal mode 
							The boundary lines are parallel to the left (and right) of the rectangle 
							<i>rect</i>. The starting and ending boundary lines are the left and right, respectively, of the rectangle <i>rect</i>. 

</li>
<li>Forward diagonal mode 
							The boundary lines are parallel to the diagonal line that is defined by the upper-right corner and lower-left corner of the rectangle <i>rect</i>. The starting boundary line passes through the starting point (upper-left corner of the rectangle <i>rect</i>). The ending boundary line passes through the ending point (lower-right corner of the rectangle <i>rect</i>). Note that starting and ending points are opposites of the starting and ending points for backward diagonal mode. 

</li>
<li>Backward diagonal mode 
							The boundary lines are parallel to the diagonal line that is defined by the upper-left corner and lower-right corner of the rectangle <i>rect</i>. The starting boundary line passes through the starting point (upper-right corner of the rectangle <i>rect</i>). The ending boundary line passes through the ending point (lower-left corner of the rectangle <i>rect</i>). Note that starting and ending points are opposites of the starting and ending points for forward diagonal mode. 

</li>
</ul>

#### Examples



The following example creates a linear gradient brush using LinearGradientModeVertical for the mode setting. 


```cpp
VOID Example_Construct04(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush(
      Rect(20, 10, 200, 100),
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255),   // blue
      LinearGradientModeVertical);
   myGraphics.FillRectangle(&linGrBrush, 0, 0, 300, 300); 
}
```





## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/9b0236b2-be6b-4918-a106-5b0e6c3dd5ff">Creating a Linear Gradient</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/ad3cce3d-67f3-4f7a-84d0-4319425de07a">LinearGradientMode</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>
 

 

