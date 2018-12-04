---
UID: NF:gdiplusheaders.CustomLineCap.GetStrokeJoin
title: CustomLineCap::GetStrokeJoin
author: windows-sdk-content
description: The CustomLineCap::GetStrokeJoin method returns the style of LineJoin used to join multiple lines in the same GraphicsPath object.
old-location: gdiplus\_gdiplus_CLASS_CustomLineCap_GetStrokeJoin_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\customlinecapclass\customlinecapmethods\getstrokejoin.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CustomLineCap class [GDI+],GetStrokeJoin method, CustomLineCap.GetStrokeJoin, CustomLineCap::GetStrokeJoin, GetStrokeJoin, GetStrokeJoin method [GDI+], GetStrokeJoin method [GDI+],CustomLineCap class, _gdiplus_CLASS_CustomLineCap_GetStrokeJoin_, gdiplus._gdiplus_CLASS_CustomLineCap_GetStrokeJoin_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - CustomLineCap.GetStrokeJoin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# CustomLineCap::GetStrokeJoin


## -description


The <b>CustomLineCap::GetStrokeJoin</b> method returns the style of <a href="https://msdn.microsoft.com/7fd13263-10c9-45b1-99b4-a8da574a26f3">LineJoin</a> used to join multiple lines in the same <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/7fd13263-10c9-45b1-99b4-a8da574a26f3">LineJoin</a></b>
</strong>

This method returns the style of line join.




## -remarks



The <a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a> object uses a path and a stroke to define the end cap. The stroke is contained in a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object, which can contain more than one figure. If there is more than one figure in the <b>GraphicsPath</b> object, the stroke join determines how their joint is graphically displayed.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a> object with a stroke join. It then gets the stroke join and assigns it as the line join of a  <a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object that it then uses to draw a line.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VOID Example_GetStrokeJoin(HDC hdc)
{
   Graphics graphics(hdc);

   //Create a Path, and add two lines to it.
   Point points[3] = {Point(-15, -15), Point(0, 0), Point(15, -15)};
   GraphicsPath capPath;
   capPath.AddLines(points, 3);

   // Create a CustomLineCap object.
   CustomLineCap custCap(NULL, &amp;capPath); 
  
   // Set the stroke join for custCap.
   custCap.SetStrokeJoin(LineJoinBevel);

   // Get the stroke join from custCap.
   LineJoin strokeJoin = custCap.GetStrokeJoin();
  
   // Create a Pen object, assign strokeJoin as the line join, and draw two
   // joined lines in a path.
   Pen strokeJoinPen(Color(255, 255, 0, 0), 15.1f);
   strokeJoinPen.SetLineJoin(strokeJoin);
   GraphicsPath joinPath;
   joinPath.AddLine(Point(10, 10), Point(10, 200));
   joinPath.AddLine(Point(10, 200), Point(200, 200));
   graphics.DrawPath(&amp;strokeJoinPen, &amp;joinPath);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bab33c8b-3203-4560-9e71-c112d528e20c">CustomLineCap</a>



<a href="https://msdn.microsoft.com/e72e402b-3cb7-4fc7-9050-ce00054da352">LineCap</a>



<a href="https://msdn.microsoft.com/7fd13263-10c9-45b1-99b4-a8da574a26f3">LineJoin</a>
 

 

