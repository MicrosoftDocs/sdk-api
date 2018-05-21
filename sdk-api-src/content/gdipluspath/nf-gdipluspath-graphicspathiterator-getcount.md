---
UID: NF:gdipluspath.GraphicsPathIterator.GetCount
title: GraphicsPathIterator::GetCount
author: windows-driver-content
description: The GraphicsPathIterator::GetCount method returns the number of data points in the path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_GetCount_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\getcount.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetCount, GetCount method [GDI+], GetCount method [GDI+],GraphicsPathIterator class, GraphicsPathIterator class [GDI+],GetCount method, GraphicsPathIterator.GetCount, GraphicsPathIterator::GetCount, _gdiplus_CLASS_GraphicsPathIterator_GetCount_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_GetCount_
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
req.typenames: WmfPlaceableFileHeader
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	GraphicsPathIterator.GetCount
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPathIterator::GetCount


## -description


The <b>GraphicsPathIterator::GetCount</b> method returns the number of data points in the path.


## -parameters






## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of data points in the path.




## -remarks



This <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> object is associated with a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object. That <b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a> enumeration.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object and then adds a rectangle and an ellipse to the path. The code passes the address of that <b>GraphicsPath</b> object to a <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <b>GraphicsPathIterator::GetCount</b> method to determine the number of data points in the path. The call to <a href="https://msdn.microsoft.com/d5280184-292b-4d8f-a468-38edc9dd3cfc">GraphicsPathIterator::Enumerate</a> retrieves two arrays from the path: one that holds the path's data points and one that holds the path's point types. After the data points have been retrieved, the code calls the <a href="https://msdn.microsoft.com/b9ed4016-aaf9-4a9c-bcd3-d653b3498c7f">FillEllipse</a> method of a  object to draw each of the data points.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
VOID GetCountExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has a rectangle and an ellipse.
   GraphicsPath path;
   path.AddRectangle(Rect(20, 20, 60, 30));
   path.AddEllipse(Rect(20, 70, 100, 50));

   // Create an iterator, and associate it with the path.
   GraphicsPathIterator iterator(&amp;amp;path);

   // Get the number of data points in the path.
   INT count = iterator.GetCount();

   // Get the data points.
   PointF* points = new PointF[count];
   BYTE* types = new BYTE[count];
   iterator.Enumerate(points, types, count);

   // Draw the data points.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j &amp;lt; count; ++j)
      graphics.FillEllipse(
         &amp;amp;brush,
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



<a href="https://msdn.microsoft.com/65a9d308-e1b7-40c4-a079-2ec9d9a5cae3">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/fded6e62-0134-4e2c-aa40-cf0a32a5b2f2">GetPathTypes</a>



<a href="https://msdn.microsoft.com/52bbe19b-298f-4297-9d23-a7b3b1f1e004">GetPointCount</a>



<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a>



<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/6b58521e-3093-45c7-93b4-ca658b67601f">GraphicsPathIterator::CopyData</a>



<a href="https://msdn.microsoft.com/d5280184-292b-4d8f-a468-38edc9dd3cfc">GraphicsPathIterator::Enumerate</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

