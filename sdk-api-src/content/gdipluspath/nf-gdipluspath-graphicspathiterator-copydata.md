---
UID: NF:gdipluspath.GraphicsPathIterator.CopyData
title: GraphicsPathIterator::CopyData
author: windows-driver-content
description: The GraphicsPathIterator::CopyData method copies a subset of the path's data points to a PointF array and copies a subset of the path's point types to a BYTE array.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_CopyData_points_types_startIndex_endIndex_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\copydata.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: CopyData, CopyData method [GDI+], CopyData method [GDI+],GraphicsPathIterator class, GraphicsPathIterator class [GDI+],CopyData method, GraphicsPathIterator.CopyData, GraphicsPathIterator::CopyData, _gdiplus_CLASS_GraphicsPathIterator_CopyData_points_types_startIndex_endIndex_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_CopyData_points_types_startIndex_endIndex_
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
-	GraphicsPathIterator.CopyData
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPathIterator::CopyData


## -description


The <b>GraphicsPathIterator::CopyData</b> method copies a subset of the path's data points to a <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> array and copies a subset of the path's point types to a <b>BYTE</b> array.


## -parameters




### -param points [out]

Type: <b><a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array that receives a subset of the path's data points. 


### -param types [out]

Type: <b>BYTE*</b>

Pointer to an array that receives a subset of the path's point types. 


### -param startIndex [in]

Type: <b>INT</b>

Integer that specifies the starting index of the points and types to be copied. 


### -param endIndex [in]

Type: <b>INT</b>

Integer that specifies the ending index of the points and types to be copied. 


## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of points copied. This is the same as the number of types copied.




## -remarks



This <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> object is associated with a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object. That <b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a> enumeration.

You can call the <a href="https://msdn.microsoft.com/36ec0f46-fb11-4d03-8d44-57e3f5efbdf5">GraphicsPathIterator::GetCount</a> method to determine the number of data points in the path.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object and adds three lines to the path. The code creates a <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a>&gt; object and calls its <b>GraphicsPathIterator::CopyData</b> method to retrieve the path's points and point types. Then the code displays the count returned by the <b>GraphicsPathIterator::CopyData</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define BUFFER_SIZE 30
TCHAR numPointsCopied[BUFFER_SIZE];

// Create the points for three lines in a path.
Point pts[] = { Point(20, 20), 
                Point(100, 20), 
                Point(100, 50), 
                Point(20, 50) };
GraphicsPath path;
path.AddLines(pts, 4); // Add the lines to the path.

// Create a GraphicsPathIterator object and associate it with the path. 
GraphicsPathIterator pathIterator(&amp;path);

// Create destination arrays, and copy the path data to them.
PointF* pCopiedPoints = new PointF[4]; 
BYTE* pTypes = new BYTE[4];
INT count = pathIterator.CopyData(pCopiedPoints, pTypes, 0, 3);

// Confirm that the points copied.
StringCchPrintf(
   numPointsCopied, BUFFER_SIZE, TEXT("%d points were copied."), count);

MessageBox(hWnd, numPointsCopied, TEXT("CopyData"), NULL);

delete[] pCopiedPoints;
delete[] pTypes;
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



<a href="https://msdn.microsoft.com/d5280184-292b-4d8f-a468-38edc9dd3cfc">GraphicsPathIterator::Enumerate</a>



<a href="https://msdn.microsoft.com/36ec0f46-fb11-4d03-8d44-57e3f5efbdf5">GraphicsPathIterator::GetCount</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

