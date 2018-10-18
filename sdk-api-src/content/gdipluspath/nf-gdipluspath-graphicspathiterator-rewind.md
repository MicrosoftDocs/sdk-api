---
UID: NF:gdipluspath.GraphicsPathIterator.Rewind
title: GraphicsPathIterator::Rewind
author: windows-sdk-content
description: The GraphicsPathIterator::Rewind method rewinds this iterator to the beginning of its associated path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_Rewind_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\rewind.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
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
				<b>NextSubpath</b> method of an iterator, it gets the first figure (subpath) of that iterator's associated path. The second time, it gets the second figure, and so on. When you call <b>GraphicsPathIterator::Rewind</b>, the sequence starts over; that is, after you call <b>GraphicsPathIterator::Rewind</b>, the next call to <a href="https://msdn.microsoft.com/e7ad0477-10f6-43e0-9788-47373a40e7cd">GraphicsPathIterator::NextSubpath</a> gets the first figure in the path. The <a href="https://msdn.microsoft.com/52454071-6806-430e-9ce0-d3640370047d">GraphicsPathIterator::NextMarker</a> and <a href="https://msdn.microsoft.com/66ed0b56-2408-4c45-a08f-aa263c05df07">GraphicsPathIterator::NextPathType</a> methods behave similarly.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object and adds five figures to the path. The code passes the address of that <b>GraphicsPath</b> object to a <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <a href="https://msdn.microsoft.com/e7ad0477-10f6-43e0-9788-47373a40e7cd">GraphicsPathIterator::NextSubpath</a> method twice to retrieve the second figure in the path. The <a href="https://msdn.microsoft.com/fffed788-ee5c-4c15-9480-dbedb7caa614">DrawPath</a> method draws that path in blue. Next, the code calls the <b>GraphicsPathIterator::Rewind</b> method and then calls <b>GraphicsPathIterator::NextSubpath</b> once to obtain the first figure in the path. The <b>DrawPath</b> method draws that figure in red.


```cpp

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
   GraphicsPathIterator iterator(&path);

   // Get the second subpath by calling NextSubpath twice.
   GraphicsPath subpath;
   BOOL isClosed;
   INT count;
   count = iterator.NextSubpath(&subpath, &isClosed);
   count = iterator.NextSubpath(&subpath, &isClosed);

   // Draw the second figure in blue.
   Pen bluePen(Color(255, 0, 0, 255));
   graphics.DrawPath(&bluePen, &subpath);

   // Rewind the iterator, and get the first figure in the path.
   iterator.Rewind();
   count = iterator.NextSubpath(&subpath, &isClosed);

   // Draw the first figure in red.
   Pen redPen(Color(255, 255, 0, 0));
   graphics.DrawPath(&redPen, &subpath);
}

```





## -see-also




<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/6eb9e19c-df28-4cf9-a434-c27478ba1fa5">GraphicsPathIterator::NextMarker Methods</a>



<a href="https://msdn.microsoft.com/66ed0b56-2408-4c45-a08f-aa263c05df07">GraphicsPathIterator::NextPathType</a>



<a href="https://msdn.microsoft.com/91137029-182d-4dc5-89a3-f3835f55d327">GraphicsPathIterator::NextSubpath Methods</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

