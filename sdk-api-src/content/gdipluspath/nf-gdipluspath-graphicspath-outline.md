---
UID: NF:gdipluspath.GraphicsPath.Outline
title: GraphicsPath::Outline
author: windows-sdk-content
description: The GraphicsPath::Outline method transforms and flattens this path, and then converts this path's data points so that they represent only the outline of the path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\outline.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GraphicsPath class [GDI+],Outline method, GraphicsPath.Outline, GraphicsPath::Outline, Outline, Outline method [GDI+], Outline method [GDI+],GraphicsPath class, _gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_, gdiplus._gdiplus_CLASS_GraphicsPath_Outline_matrix_flatness_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WmfPlaceableFileHeader
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPath::Outline


## -description


The <b>GraphicsPath::Outline</b> method transforms and flattens this path, and then converts this path's data points so that they represent only the outline of the path.


## -parameters




### -param matrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>*</b>

Optional. Pointer to a <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> object that specifies the transformation. If this parameter is <b>NULL</b>, no transformation is applied. The default value is <b>NULL</b>. 


### -param flatness [in]

Type: <b>REAL</b>

Optional. Real number that specifies the maximum error between the path and its flattened approximation. Reducing the flatness increases the number of line segments in the approximation. The default value is FlatnessDefault, which is a constant defined in Gdiplusenums.h. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object stores a collection of data points that represent lines and curves. The <b>GraphicsPath::Outline</b> method changes those data points, and the original data points are lost.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object and calls the <a href="https://msdn.microsoft.com/41dfe6f5-330c-4f72-9c54-10290e96aadc">GraphicsPath::AddClosedCurve</a> method to add a closed cardinal spline to the path. The code calls the <a href="https://msdn.microsoft.com/e8351fb1-b11f-4da7-9cc4-dc3ab685f29d">GraphicsPath::Widen</a> method to widen the path and then draws the path. Next, the code calls the path's <b>Outline</b> method. The code calls the <a href="https://msdn.microsoft.com/99b51fb7-b1de-421f-9743-bf6a5ec758ef">TranslateTransform</a> method of a Graphics object so that the outlined path drawn by the subsequent call to <a href="https://msdn.microsoft.com/fffed788-ee5c-4c15-9480-dbedb7caa614">DrawPath</a> sits to the right of the first path.

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




<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/f6a8085c-3d6a-494f-a1ee-5fa96efb1aae">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/947b3e68-67ad-47fb-80bb-b5a678f71381">GraphicsPath::Flatten</a>



<a href="https://msdn.microsoft.com/7c7931ab-f8fd-46f9-a140-9e680bf06002">GraphicsPath::Warp</a>



<a href="https://msdn.microsoft.com/e8351fb1-b11f-4da7-9cc4-dc3ab685f29d">GraphicsPath::Widen</a>



<a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

