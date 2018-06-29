---
UID: NL:gdiplustypes.PathData
title: PathData
author: windows-sdk-content
description: The PathData class is a helper class for the GraphicsPath and GraphicsPathIterator classes.
old-location: gdiplus\_gdiplus_CLASS_PathData_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathdata.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: PathData, PathData class [GDI+], PathData class [GDI+],described, _gdiplus_CLASS_PathData_Class, gdiplus._gdiplus_CLASS_PathData_Class, gdiplustypes/PathData
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# PathData class


## -description


The <b>PathData</b> class is a helper class for the 
			<a href="https://msdn.microsoft.com/library/ms534456(v=VS.85).aspx">GraphicsPath</a> and 
			<a href="https://msdn.microsoft.com/library/ms534458(v=VS.85).aspx">GraphicsPathIterator</a> classes. A 
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
<a href="https://msdn.microsoft.com/library/ms535103(v=VS.85).aspx">PathData::PathData()</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/library/ms535103(v=VS.85).aspx">PathData::PathData</a> object. The <b>Count</b> data member is initialized to 0. The <b>Points</b> and <b>Types</b> data members are initialized to <b>NULL</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/ms533805(v=VS.85).aspx">Constructing and Drawing Paths</a>



<a href="https://msdn.microsoft.com/library/ms535561(v=VS.85).aspx">GetPathPoints Methods</a>



<a href="https://msdn.microsoft.com/library/ms535534(v=VS.85).aspx">GraphicsPath::GetPathData</a>



<a href="https://msdn.microsoft.com/library/ms535535(v=VS.85).aspx">GraphicsPath::GetPathTypes</a>



<a href="https://msdn.microsoft.com/library/ms535536(v=VS.85).aspx">GraphicsPath::GetPointCount</a>



<a href="https://msdn.microsoft.com/library/ms534162(v=VS.85).aspx">PathPointType</a>



<a href="https://msdn.microsoft.com/library/ms536370(v=VS.85).aspx">Paths</a>



<a href="https://msdn.microsoft.com/library/ms534488(v=VS.85).aspx">PointF</a>
 

 

