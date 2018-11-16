---
UID: NF:gdipluspath.GraphicsPathIterator.Enumerate
title: GraphicsPathIterator::Enumerate
author: windows-sdk-content
description: The GraphicsPathIterator::Enumerate method copies the path's data points to a PointF array and copies the path's point types to a BYTE array.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_Enumerate_points_types_count_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiteratorclass\graphicspathiteratormethods\enumerate.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Enumerate, Enumerate method [GDI+], Enumerate method [GDI+],GraphicsPathIterator class, GraphicsPathIterator class [GDI+],Enumerate method, GraphicsPathIterator.Enumerate, GraphicsPathIterator::Enumerate, _gdiplus_CLASS_GraphicsPathIterator_Enumerate_points_types_count_, gdiplus._gdiplus_CLASS_GraphicsPathIterator_Enumerate_points_types_count_
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
 - GraphicsPathIterator.Enumerate
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
- GraphicsPathIterator.Enumerate
: 
req.product: GDI+ 1.0
---

# GraphicsPathIterator::Enumerate


## -description


The <b>GraphicsPathIterator::Enumerate</b> method copies the path's data points to a <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> array and copies the path's point types to a <b>BYTE</b> array.


## -parameters




### -param points [out]

Type: <b><a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>*</b>

Pointer to an array that receives the path's data points. 


### -param types [out]

Type: <b>BYTE*</b>

Pointer to an array that receives the path's point types. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>points</i> array. This is the same as the number of elements in the <i>types</i> array. 


## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of points retrieved. 




## -remarks



This 
				<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> object is associated with a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object. That <b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a> enumeration.

You can call the <a href="https://msdn.microsoft.com/36ec0f46-fb11-4d03-8d44-57e3f5efbdf5">GraphicsPathIterator::GetCount</a> method to determine the number of data points in the path. The <i>points</i> parameter points to a buffer that receives the data points, and the <i>types</i> parameter points to a buffer that receives the types. Before you call the <b>GraphicsPathIterator::Enumerate</b> method, you must allocate memory for those buffers. The size of the <i>points</i> buffer should be the return value of <b>GraphicsPathIterator::GetCount</b> multiplied by <b>sizeof(PointF)</b>. The size of the types buffer should be the return value of <b>GraphicsPathIterator::GetCount</b>.


#### Examples



The following example creates a <a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> object and adds three lines to the path. The code creates a <a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> object and calls its <b>GraphicsPathIterator::Enumerate</b> method to retrieve the path's data points and point types. Then the code displays the count returned by the <b>GraphicsPathIterator::Enumerate</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#define BUFFER_SIZE 30
TCHAR numPointsEnum[BUFFER_SIZE];

// Add some lines to a path.
Point pts[] = {Point(20, 20), 
                Point(100, 20), 
                Point(100, 50), 
                Point(20, 50)};
GraphicsPath path;
path.AddLines(pts, 4);

// Create a GraphicsPathIterator object, and associate it with the path.
GraphicsPathIterator pathIterator(&amp;path);

// Create destination arrays, and copy the path data to them.
UINT c = pathIterator.GetCount();
PointF* pEnumPoints = new PointF[c]; 
BYTE* pTypes = new BYTE[c];
INT count = pathIterator.Enumerate(pEnumPoints, pTypes, c);

// Confirm that the points were enumerated.
StringCchPrintf(
   numPointsEnum, BUFFER_SIZE, TEXT("%d points were enumerated."), count);

MessageBox(hWnd, numPointsEnum, TEXT("Enumerate"), NULL);

delete[] pEnumPoints;
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



<a href="https://msdn.microsoft.com/6b58521e-3093-45c7-93b4-ca658b67601f">GraphicsPathIterator::CopyData</a>



<a href="https://msdn.microsoft.com/36ec0f46-fb11-4d03-8d44-57e3f5efbdf5">GraphicsPathIterator::GetCount</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>
 

 

