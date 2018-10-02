---
UID: NF:gdipluspath.GraphicsPathIterator.GetCount
title: GraphicsPathIterator::GetCount
author: windows-sdk-content
description: The GraphicsPathIterator::GetCount method returns the number of data points in the path.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_GetCount_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\getcount.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
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
 - GraphicsPathIterator.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This <a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a> object is associated with a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object. That <b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a> enumeration.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object and then adds a rectangle and an ellipse to the path. The code passes the address of that <b>GraphicsPath</b> object to a <a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a> constructor to create an iterator that is associated with the path. The code calls the iterator's <b>GraphicsPathIterator::GetCount</b> method to determine the number of data points in the path. The call to <a href="https://msdn.microsoft.com/en-us/library/ms535453(v=VS.85).aspx">GraphicsPathIterator::Enumerate</a> retrieves two arrays from the path: one that holds the path's data points and one that holds the path's point types. After the data points have been retrieved, the code calls the <a href="https://msdn.microsoft.com/en-us/library/ms535967(v=VS.85).aspx">FillEllipse</a> method of a  object to draw each of the data points.


```cpp

VOID GetCountExample(HDC hdc)
{
   Graphics graphics(hdc);

   // Create a path that has a rectangle and an ellipse.
   GraphicsPath path;
   path.AddRectangle(Rect(20, 20, 60, 30));
   path.AddEllipse(Rect(20, 70, 100, 50));

   // Create an iterator, and associate it with the path.
   GraphicsPathIterator iterator(&path);

   // Get the number of data points in the path.
   INT count = iterator.GetCount();

   // Get the data points.
   PointF* points = new PointF[count];
   BYTE* types = new BYTE[count];
   iterator.Enumerate(points, types, count);

   // Draw the data points.
   SolidBrush brush(Color(255, 255, 0, 0));
   for(INT j = 0; j < count; ++j)
      graphics.FillEllipse(
         &brush,
         points[j].X - 3.0f, 
         points[j].Y - 3.0f,
         6.0f,
         6.0f);

   delete points;
   delete types;
}

```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535534(v=VS.85).aspx">GetPathData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535561(v=VS.85).aspx">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535535(v=VS.85).aspx">GetPathTypes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535536(v=VS.85).aspx">GetPointCount</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535452(v=VS.85).aspx">GraphicsPathIterator::CopyData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535453(v=VS.85).aspx">GraphicsPathIterator::Enumerate</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>
 

 

