---
UID: NF:gdiplusbrush.LinearGradientBrush.LinearGradientBrush(IN const PointF &,IN const PointF &,IN const Color &,IN const Color &)
title: LinearGradientBrush::LinearGradientBrush(IN const PointF &,IN const PointF &,IN const Color &,IN const Color &)
author: windows-sdk-content
description: Creates a LinearGradientBrush::LinearGradientBrush object from a set of boundary points and boundary colors.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_Point_point1_Point_point2_Color_color1_Color_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushconstructors\lineargradientbrush_61pointamppoint1_pointamppoint2_coloramp.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: LinearGradientBrush, LinearGradientBrush class [GDI+],LinearGradientBrush constructor, LinearGradientBrush constructor [GDI+], LinearGradientBrush constructor [GDI+],LinearGradientBrush class, LinearGradientBrush.LinearGradientBrush, LinearGradientBrush.LinearGradientBrush(IN const PointF &,IN const PointF &,IN const Color &,IN const Color &), LinearGradientBrush.LinearGradientBrush(const Point&,const Point&,const Color&,const Color&), LinearGradientBrush::LinearGradientBrush, LinearGradientBrush::LinearGradientBrush(IN const PointF &,IN const PointF &,IN const Color &,IN const Color &), _gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_Point_point1_Point_point2_Color_color1_Color_, gdiplus._gdiplus_CLASS_LinearGradientBrush_LinearGradientBrush_Point_point1_Point_point2_Color_color1_Color_
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
req.product: GDI+ 1.0
---

# LinearGradientBrush::LinearGradientBrush(IN const PointF &,IN const PointF &,IN const Color &,IN const Color &)


## -description


Creates a <b>LinearGradientBrush::LinearGradientBrush</b> object from a set of boundary points and boundary colors.


## -parameters




### -param point1 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a></b>

Reference to a <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> object that specifies the starting point of the gradient. The starting boundary line passes through the starting point. 


### -param point2 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a></b>

Reference to a <a href="https://msdn.microsoft.com/8bf4d566-b061-4102-8307-218431e286f8">Point</a> object that specifies the ending point of the gradient. The ending boundary line passes through the ending point. 


### -param color1 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color at the starting boundary line of this linear gradient brush. 


### -param color2 [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a></b>

Reference to a <a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a> object that specifies the color at the ending boundary line of this linear gradient brush. 


## -remarks



The "directional line," an imaginary straight line, is defined by the starting point, <i>point1</i>, and the ending point, <i>point2</i>. The starting boundary of the gradient is a straight line that is perpendicular to the directional line and that passes through the starting point. The ending boundary of the gradient is a straight line that is parallel to the starting boundary line and that passes through the ending point. The gradient color is constant along lines that are parallel to the boundary lines. The gradient gradually changes from the starting color to the ending color along the directional line.


#### Examples



The following example creates a linear gradient brush from a set of boundary points and boundary colors. The code then uses the brush to paint the interior of a rectangle.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_Construct01(HDC hdc)
{
   Graphics myGraphics(hdc);

   LinearGradientBrush linGrBrush(
      Point(50, 50),
      Point(200, 100),
      Color(255, 255, 0, 0),   // red
      Color(255, 0, 0, 255));  // blue

   myGraphics.FillRectangle(&amp;linGrBrush, 0, 0, 300, 200);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dae648fd-1302-481e-9f5b-331a4c1b5e0d">Color</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/9b995615-3ea1-488d-8960-90add719c3f9">Rect</a>
 

 

