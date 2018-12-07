---
UID: NF:gdipluspath.GraphicsPath.Outline
title: GraphicsPath::Outline
author: windows-sdk-content
description: The GraphicsPath::Outline method transforms and flattens this path, and then converts this path's data points so that they represent only the outline of the path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\outline.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GraphicsPath class [GDI+],Outline method, GraphicsPath.Outline, GraphicsPath::Outline, Outline, Outline method [GDI+], Outline method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_, gdiplus._gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_
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
 - GraphicsPath.Outline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPath::Outline


## -description


The <b>GraphicsPath::Outline</b> method transforms and flattens this path, and then converts this path's data points so that they represent only the outline of the path.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a> object that specifies the transformation. If this parameter is <b>NULL</b>, no transformation is applied. The default value is <b>NULL</b>. 


### -param flatness [in]

Type: <b>REAL</b>

Optional. Real number that specifies the maximum error between the path and its flattened approximation. Reducing the flatness increases the number of line segments in the approximation. The default value is FlatnessDefault, which is a constant defined in Gdiplusenums.h. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object stores a collection of data points that represent lines and curves. The <b>GraphicsPath::Outline</b> method changes those data points, and the original data points are lost.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object and calls the <a href="https://msdn.microsoft.com/en-us/library/ms535615(v=VS.85).aspx">GraphicsPath::AddClosedCurve</a> method to add a closed cardinal spline to the path. The code calls the <a href="https://msdn.microsoft.com/en-us/library/ms535572(v=VS.85).aspx">GraphicsPath::Widen</a> method to widen the path and then draws the path. Next, the code calls the path's <b>Outline</b> method. The code calls the <a href="https://msdn.microsoft.com/en-us/library/ms535820(v=VS.85).aspx">TranslateTransform</a> method of a Graphics object so that the outlined path drawn by the subsequent call to <a href="https://msdn.microsoft.com/en-us/library/ms535685(v=VS.85).aspx">DrawPath</a> sits to the right of the first path.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID OutlineExample(HDC hdc)
{
   Graphics graphics(hdc);

   Pen bluePen(Color(255, 0, 0, 255));
   Pen greenPen(Color(255, 0, 255,  0), 10);

   PointF points[] = {
      PointF(20.0f, 20.0f),
      PointF(160.0f, 100.0f),
      PointF(140.0f, 60.0f),
      PointF(60.0f, 100.0f)};

   GraphicsPath path;
   path.AddClosedCurve(points, 4);

   path.Widen(&amp;greenPen);
   graphics.DrawPath(&amp;bluePen, &amp;path);

   path.Outline();

   graphics.TranslateTransform(180.0f, 0.0f);
   graphics.DrawPath(&amp;bluePen, &amp;path);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535530(v=VS.85).aspx">GraphicsPath::Flatten</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535571(v=VS.85).aspx">GraphicsPath::Warp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535572(v=VS.85).aspx">GraphicsPath::Widen</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534475(v=VS.85).aspx">Matrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

