---
UID: NF:gdipluspath.GraphicsPath.GetPathTypes
title: GraphicsPath::GetPathTypes
author: windows-sdk-content
description: The GraphicsPath::GetPathTypes method gets this path's array of point types.
old-location: gdiplus\_gdiplus_CLASS_GraphicsPath_GetPathTypes_types_count_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathclass\graphicspathmethods\getpathtypes.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetPathTypes, GetPathTypes method [GDI+], GetPathTypes method [GDI+],GraphicsPath class, GraphicsPath class [GDI+],GetPathTypes method, GraphicsPath.GetPathTypes, GraphicsPath::GetPathTypes, _gdiplus_CLASS_GraphicsPath_GetPathTypes_types_count_, gdiplus._gdiplus_CLASS_GraphicsPath_GetPathTypes_types_count_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdipluspath.h
req.include-header: Gdiplus.h
req.redist: 
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
 - GraphicsPath.GetPathTypes
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# GraphicsPath::GetPathTypes


## -description


The <b>GraphicsPath::GetPathTypes</b> method gets this path's array of point types.


## -parameters




### -param types [out]

Type: <b>BYTE*</b>

Pointer to an array that receives the point types. You must allocate memory for this array. You can call the <a href="https://msdn.microsoft.com/en-us/library/ms535536(v=VS.85).aspx">GraphicsPath::GetPointCount</a> method to determine the required size of the array. 


### -param count [in]

Type: <b>INT</b>

Integer that specifies the number of elements in the <i>types</i> array. Set this parameter equal to the return value of the <a href="https://msdn.microsoft.com/en-us/library/ms535536(v=VS.85).aspx">GraphicsPath::GetPointCount</a> method. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -remarks



A <a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. Possible point types and flags are listed in the <a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a> enumeration.


#### Examples



The following example creates a path and adds a sequence of three connected lines to the path. The code calls the <a href="https://msdn.microsoft.com/en-us/library/ms535536(v=VS.85).aspx">GraphicsPath::GetPointCount</a> method to determine the number of bytes in the path's array of point types and then allocates a buffer large enough to hold that array. Then the code calls the <b>GraphicsPath::GetPathTypes</b> method to fill the buffer with the array of point types.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>GraphicsPath path;
Point pts[] = {Point(0, 0), Point(2, 2), Point(3, 3), Point(0, 5)};
path.AddLines(pts, 4);
INT num = path.GetPointCount();
BYTE* pTypes = new BYTE[num];
path.GetPathTypes(pTypes, num);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533917(v=VS.85).aspx">Creating a Path Gradient</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535561(v=VS.85).aspx">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534456(v=VS.85).aspx">GraphicsPath</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535534(v=VS.85).aspx">GraphicsPath::GetPathData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535536(v=VS.85).aspx">GraphicsPath::GetPointCount</a>



<a href="https://msdn.microsoft.com/b8e9a4cb-72e1-4646-956a-50801176a3bd">PathData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534162(v=VS.85).aspx">PathPointType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534488(v=VS.85).aspx">PointF</a>
 

 

