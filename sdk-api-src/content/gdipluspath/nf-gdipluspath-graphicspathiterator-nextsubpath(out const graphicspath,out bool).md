---
UID: NF:gdipluspath.GraphicsPathIterator.NextSubpath(OUT const GraphicsPath,OUT BOOL)
title: GraphicsPathIterator::NextSubpath(OUT const GraphicsPath,OUT BOOL)
author: windows-sdk-content
description: The GraphicsPathIterator::NextSubpath method gets the next figure (subpath) from this iterator's associated path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_NextSubpath_path_isClosed_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\graphicspathiteratornextsubpathmethods\nextsubpath.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GraphicsPathIterator class [GDI+],NextSubpath method, GraphicsPathIterator.NextSubpath, GraphicsPathIterator.NextSubpath(GraphicsPath*,BOOL*), GraphicsPathIterator.NextSubpath(OUT const GraphicsPath,OUT BOOL), GraphicsPathIterator::NextSubpath, GraphicsPathIterator::NextSubpath(OUT const GraphicsPath,OUT BOOL), NextSubpath, NextSubpath method [GDI+], NextSubpath method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_NextSubpath_path_isClosed_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_NextSubpath_path_isClosed_
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
 - GraphicsPathIterator.NextSubpath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPathIterator::NextSubpath(OUT const GraphicsPath,OUT BOOL)


## -description


The <b>GraphicsPathIterator::NextSubpath</b> method gets the next figure (subpath) from this iterator's associated path.


## -parameters




### -param path [out]

Type: <b><a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object. This method sets the data points of this <b>GraphicsPath</b> object to match the data points of the retrieved figure. 


### -param isClosed [out]

Type: <b>BOOL*</b>

Pointer to a <b>BOOL</b> that receives a value that indicates whether the retrieved figure is closed. If the figure is closed, the received value is <b>TRUE</b>; otherwise, the received value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of data points in the retrieved figure. If there are no more figures to retrieve, this method returns 0.




## -remarks



The first time you call the <b>GraphicsPathIterator::NextSubpath</b> method of an iterator, it gets the first figure (subpath) of that iterator's associated path. The second time, it gets the second figure, and so on. Each time you call <b>GraphicsPathIterator::NextSubpath</b>, it returns the number of data points in the retrieved figure. When there are no figures remaining, it returns 0.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object and adds five figures (also called subpaths) to the path. The code passes the address of the <b>GraphicsPath</b> object to a <a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <b>GraphicsPathIterator::NextSubpath</b> method twice to retrieve the second figure (subpath) from the path. Then the code calls the <a href="https://msdn.microsoft.com/fffed788-ee5c-4c15-9480-dbedb7caa614">DrawPath</a> method of a <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object to draw that individual subpath.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID NextSubpathExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a graphics path with five figures (subpaths).
   GraphicsPath path;

   path.AddRectangle(Rect(20, 20, 60, 30));   // Subpath count is 1.

   path.AddLine(100, 20, 160, 50);            // Subpath count is 2.
   path.AddArc(180, 20, 60, 30, 0.0f, 180.0f);

   path.AddRectangle(Rect(260, 20, 60, 30));  // Subpath count is 3.

   path.AddLine(340, 20, 400, 50);            // Subpath count is 4.
   path.AddArc(340, 20, 60, 30, 0.0f, 180.0f);
   path.CloseFigure();
  
   path.AddRectangle(Rect(420, 20, 60, 30));  // Subpath count is 5.
 
   // Create an iterator, and associate it with the path.
   GraphicsPathIterator iterator(&amp;path);

   // Get the second subpath by calling NextSubpath twice.
   GraphicsPath subpath;
   BOOL isClosed;
   INT count;
   count = iterator.NextSubpath(&amp;subpath, &amp;isClosed);
   count = iterator.NextSubpath(&amp;subpath, &amp;isClosed);

   // The variable "count" now holds the number of 
   // data points in the second subpath.

   // Draw the retrieved subpath.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawPath(&amp;bluePen, &amp;subpath);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/c757cfb8-25fe-4881-96b3-5257f925b781">GetPathData</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/815bd2c6-c778-4983-acf4-071a89269a19">GraphicsPathIterator::GetSubpathCount</a>



<a href="https://msdn.microsoft.com/6eb9e19c-df28-4cf9-a434-c27478ba1fa5">GraphicsPathIterator::NextMarker Methods</a>



<a href="https://msdn.microsoft.com/91137029-182d-4dc5-89a3-f3835f55d327">NextSubpath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

