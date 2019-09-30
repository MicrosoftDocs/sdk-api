---
UID: NL:gdiplustypes.PathData
title: PathData (gdiplustypes.h)
author: windows-sdk-content
description: The PathData class is a helper class for the GraphicsPath and GraphicsPathIterator classes.
old-location: gdiplus\_gdiplus_CLASS_PathData_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pathdata.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PathData, PathData class [GDI+], PathData class [GDI+],described, _gdiplus_CLASS_PathData_Class, gdiplus._gdiplus_CLASS_PathData_Class, gdiplustypes/PathData
ms.topic: class
f1_keywords: 
 - "gdiplustypes/PathData"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PathData class


## -description


The <b>PathData</b> class is a helper class for the 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> and 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspathiterator">GraphicsPathIterator</a> classes. A 
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
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-pathdata-pathdata(constpathdata_)">PathData::PathData()</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-pathdata-pathdata(constpathdata_)">PathData::PathData</a> object. The <b>Count</b> data member is initialized to 0. The <b>Points</b> and <b>Types</b> data members are initialized to <b>NULL</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-constructing-and-drawing-paths-use">Constructing and Drawing Paths</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathpoints(outpoint_inint)">GetPathPoints Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathdata">GraphicsPath::GetPathData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpathtypes">GraphicsPath::GetPathTypes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-getpointcount">GraphicsPath::GetPointCount</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-pathpointtype">PathPointType</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-paths-about">Paths</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a>
 

 

