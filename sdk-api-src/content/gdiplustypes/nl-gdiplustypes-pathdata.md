---
UID: NL:gdiplustypes.PathData
title: PathData
author: windows-sdk-content
description: The PathData class is a helper class for the GraphicsPath and GraphicsPathIterator classes.
old-location: gdiplus\_gdiplus_CLASS_PathData_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathdata.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PathData, PathData class [GDI+], PathData class [GDI+],described, _gdiplus_CLASS_PathData_Class, gdiplus._gdiplus_CLASS_PathData_Class, gdiplustypes/PathData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
req.header: gdiplustypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplustypes.h
api_name:
 - PathData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PathData class


## -description


The <b>PathData</b> class is a helper class for the 
			<a href="https://msdn.microsoft.com/1072a5cc-4e82-41f4-aaad-5f90eb2cfa22">GraphicsPath</a> and 
			<a href="https://msdn.microsoft.com/f534b1b2-1fe3-4f30-8a7f-30d44f11d297">GraphicsPathIterator</a> classes. A 
			<b>GraphicsPath</b> object has an array of points and an array of types. Each element in the array of types is a byte that specifies the point type and a set of flags for the corresponding element in the array of points. You can use a <b>PathData</b> object to get or set the data points (and their types) of a path.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">PathData</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">PathData</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a81bfbd5-929d-4baa-b1d6-69445942a9dd">PathData::PathData()</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/a81bfbd5-929d-4baa-b1d6-69445942a9dd">PathData::PathData</a> object. The <b>Count</b> data member is initialized to 0. The <b>Points</b> and <b>Types</b> data members are initialized to <b>NULL</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dbfe8cea-bd9e-43ad-85c8-37cce3ef97a4">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/65a9d308-e1b7-40c4-a079-2ec9d9a5cae3">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/c757cfb8-25fe-4881-96b3-5257f925b781">GraphicsPath::GetPathData</a>



<a href="https://msdn.microsoft.com/fded6e62-0134-4e2c-aa40-cf0a32a5b2f2">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/52bbe19b-298f-4297-9d23-a7b3b1f1e004">GraphicsPath::GetPointCount</a>



<a href="https://msdn.microsoft.com/daad4301-f338-4cce-bb31-ddcf09c0c59c">PathPointType</a>



<a href="https://msdn.microsoft.com/88fea2ec-7b53-44bb-841d-486c5c879c68">Paths</a>



<a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a>
 

 

