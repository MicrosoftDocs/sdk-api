---
UID: NF:gdipluspath.GraphicsPathIterator.Rewind
title: GraphicsPathIterator::Rewind
author: windows-sdk-content
description: The GraphicsPathIterator::Rewind method rewinds this iterator to the beginning of its associated path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_Rewind_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\rewind.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GraphicsPathIterator class [GDI+],Rewind method, GraphicsPathIterator.Rewind, GraphicsPathIterator::Rewind, Rewind, Rewind method [GDI+], Rewind method [GDI+],GraphicsPathIterator class, _gdiplus_CLASS_GraphicsPathIterator_Rewind_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_Rewind_
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
 - GraphicsPathIterator.Rewind
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GraphicsPathIterator::Rewind


## -description


The <b>GraphicsPathIterator::Rewind</b> method rewinds this iterator to the beginning of its associated path.


## -parameters






## -returns



This method does not return a value.




## -remarks



The first time you call the 
				<b>NextSubpath</b> method of an iterator, it gets the first figure (subpath) of that iterator's associated path. The second time, it gets the second figure, and so on. When you call <b>GraphicsPathIterator::Rewind</b>, the sequence starts over; that is, after you call <b>GraphicsPathIterator::Rewind</b>, the next call to <a href="https://msdn.microsoft.com/en-us/library/ms535462(v=VS.85).aspx">GraphicsPathIterator::NextSubpath</a> gets the first figure in the path. The <a href="https://msdn.microsoft.com/en-us/library/ms535464(v=VS.85).aspx">GraphicsPathIterator::NextMarker</a> and <a href="https://msdn.microsoft.com/en-us/library/ms535460(v=VS.85).aspx">GraphicsPathIterator::NextPathType</a> methods behave similarly.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object and adds five figures to the path. The code passes the address of that <b>GraphicsPath</b> object to a <a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <a href="https://msdn.microsoft.com/en-us/library/ms535462(v=VS.85).aspx">GraphicsPathIterator::NextSubpath</a> method twice to retrieve the second figure in the path. The <a href="https://msdn.microsoft.com/en-us/library/ms535685(v=VS.85).aspx">DrawPath</a> method draws that path in blue. Next, the code calls the <b>GraphicsPathIterator::Rewind</b> method and then calls <b>GraphicsPathIterator::NextSubpath</b> once to obtain the first figure in the path. The <b>DrawPath</b> method draws that figure in red.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID RewindExample(HDC hdc)
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
   GraphicsPathIterator iterator(&amp;amp;path);

   // Get the second subpath by calling NextSubpath twice.
   GraphicsPath subpath;
   BOOL isClosed;
   INT count;
   count = iterator.NextSubpath(&amp;amp;subpath, &amp;amp;isClosed);
   count = iterator.NextSubpath(&amp;amp;subpath, &amp;amp;isClosed);

   // Draw the second figure in blue.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawPath(&amp;amp;bluePen, &amp;amp;subpath);

   // Rewind the iterator, and get the first figure in the path.
   iterator.Rewind();
   count = iterator.NextSubpath(&amp;amp;subpath, &amp;amp;isClosed);

   // Draw the first figure in red.
   Pen redPen(Color(255, 255, 0, 0));
   graphics.DrawPath(&amp;amp;redPen, &amp;amp;subpath);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535457(v=VS.85).aspx">GraphicsPathIterator::NextMarker Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535460(v=VS.85).aspx">GraphicsPathIterator::NextPathType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535458(v=VS.85).aspx">GraphicsPathIterator::NextSubpath Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

