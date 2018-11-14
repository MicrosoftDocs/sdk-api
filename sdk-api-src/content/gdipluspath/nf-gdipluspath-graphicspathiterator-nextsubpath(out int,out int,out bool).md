---
UID: NF:gdipluspath.GraphicsPathIterator.NextSubpath(OUT INT,OUT INT,OUT BOOL)
title: GraphicsPathIterator::NextSubpath(OUT INT,OUT INT,OUT BOOL)
author: windows-sdk-content
description: The GraphicsPathIterator::NextSubpath method gets the starting index and the ending index of the next subpath (figure) in this iterator's associated path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_NextSubpath_startIndex_endIndex_isClosed_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\graphicspathiteratornextsubpathmethods\nextsubpath_33startindex_endindex_isclosed.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GraphicsPathIterator class [GDI+],NextSubpath method, GraphicsPathIterator.NextSubpath, GraphicsPathIterator.NextSubpath(INT*,INT*,BOOL*), GraphicsPathIterator.NextSubpath(OUT INT,OUT INT,OUT BOOL), GraphicsPathIterator::NextSubpath, GraphicsPathIterator::NextSubpath(OUT INT,OUT INT,OUT BOOL), NextSubpath, NextSubpath method [GDI+], NextSubpath method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_NextSubpath_startIndex_endIndex_isClosed_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_NextSubpath_startIndex_endIndex_isClosed_
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
- apiref
: 
- COM
: 
- gdipluspath.h
: 
- GraphicsPathIterator.NextSubpath
: 
req.product: GDI+ 1.0
---

# GraphicsPathIterator::NextSubpath(OUT INT,OUT INT,OUT BOOL)


## -description


The <b>GraphicsPathIterator::NextSubpath</b> method gets the starting index and the ending index of the next subpath (figure) in this iterator's associated path.


## -parameters




### -param startIndex [out]

Type: <b>INT*</b>

Pointer to an 
					<b>INT</b> that receives the starting index. 


### -param endIndex [out]

Type: <b>INT*</b>

Pointer to an 
					<b>INT</b> that receives the ending index. 


### -param isClosed [out]

Type: <b>BOOL*</b>

Pointer to a <b>BOOL</b> that receives a value that indicates whether the obtained figure is closed. If the figure is closed, the received value is <b>TRUE</b>; otherwise, the received value is <b>FALSE</b>. 


## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of data points in the next figure. If there are no more figures in the path, this method returns 0.




## -remarks



The first time you call the <b>GraphicsPathIterator::NextSubpath</b> method of an iterator, it gets the indices for the first figure (subpath) of that iterator's associated path. The second time, it gets the indices for the second figure, and so on. Each time you call <b>GraphicsPathIterator::NextSubpath</b>, it returns the number of data points in the figure whose indices were retrieved. When there are no figures remaining, it returns 0.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object and adds five figures to the path. The code passes the address of that <b>GraphicsPath</b> object to a <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <b>GraphicsPathIterator::NextSubpath</b> method three times to obtain the starting index and the ending index of the path's third figure. Then the code calls the iterator's <a href="https://msdn.microsoft.com/6b58521e-3093-45c7-93b4-ca658b67601f">GraphicsPathIterator::CopyData</a> method to retrieve the third figure's data points.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID NextSubpathExample2(HDC hdc)
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

   // Call NextSubpath three times to get the starting and ending 
   // indices for the third figure. 
   INT start;
   INT end;
   BOOL isClosed;
   INT count;
   count = iterator.NextSubpath(&amp;start, &amp;end, &amp;isClosed);
   count = iterator.NextSubpath(&amp;start, &amp;end, &amp;isClosed);
   count = iterator.NextSubpath(&amp;start, &amp;end, &amp;isClosed);

   // Get the third figure's data points.
   PointF* points = new PointF[count];
   BYTE* types = new BYTE[count];
   iterator.CopyData(points, types, start, end);

   // Draw the third figure's data points.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j &lt; count; ++j)
      graphics.FillEllipse(
         &amp;brush,
         points[j].X - 3.0f, 
         points[j].Y - 3.0f, 
         6.0f, 
         6.0f);

   delete points;
   delete types;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/c757cfb8-25fe-4881-96b3-5257f925b781">GetPathData</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/6b58521e-3093-45c7-93b4-ca658b67601f">GraphicsPathIterator::CopyData</a>



<a href="https://msdn.microsoft.com/815bd2c6-c778-4983-acf4-071a89269a19">GraphicsPathIterator::GetSubpathCount</a>



<a href="https://msdn.microsoft.com/6eb9e19c-df28-4cf9-a434-c27478ba1fa5">GraphicsPathIterator::NextMarker Methods</a>



<a href="https://msdn.microsoft.com/91137029-182d-4dc5-89a3-f3835f55d327">NextSubpath</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

