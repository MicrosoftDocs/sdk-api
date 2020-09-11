---
UID: NL:gdiplustypes.RectF
title: RectF (gdiplustypes.h)
description: A RectF object stores the upper-left corner, width, and height of a rectangle.
helpviewer_keywords: ["RectF","RectF class [GDI+]","RectF class [GDI+]","described","_gdiplus_CLASS_RectF_Class","gdiplus._gdiplus_CLASS_RectF_Class","gdiplustypes/RectF"]
old-location: gdiplus\_gdiplus_CLASS_RectF_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectf.htm
ms.date: 12/05/2018
ms.keywords: RectF, RectF class [GDI+], RectF class [GDI+],described, _gdiplus_CLASS_RectF_Class, gdiplus._gdiplus_CLASS_RectF_Class, gdiplustypes/RectF
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RectF
 - gdiplustypes/RectF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplustypes.h
api_name:
 - RectF
---

# RectF class


## -description

A <b>RectF</b> object stores the upper-left corner, width, and height of a rectangle.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">RectF</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">RectF</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-rectf(inconstpointf__inconstsizef_)">RectF::RectF()</a>
</td>
<td align="left" width="63%">
Creates a <b>RectF</b> object and initializes the 
			<b>X</b> and 
			<b>Y</b> data members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-rectf(inconstpointf__inconstsizef_)">RectF::RectF(PointF&,SizeF&)</a>
</td>
<td align="left" width="63%">
Creates a <b>RectF</b> object by using a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-pointf">PointF</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members and uses a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object to initialize the 
			<b>Width</b> and 
			<b>Height</b> data members of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-rectf(inreal_inreal_inreal_inreal)">RectF::RectF(REAL,REAL,REAL,REAL)</a>
</td>
<td align="left" width="63%">
Creates a <b>RectF</b> object by using four integers to initialize the 
			<b>X</b>, 
			<b>Y</b>, 
			<b>Width</b>, and 
			<b>Height</b> data members.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>RectF</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-clone">RectF::Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-clone">RectF::Clone</a> method creates a new 
			<b>RectF</b> object and initializes it with the contents of this 
			<b>RectF</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-contains(inconstpointf_)">RectF::Contains(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-contains(inconstpointf_)">RectF::Contains</a> method determines whether a point is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms534956(v=vs.85)">RectF::Contains(REAL,REAL)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/ms534956(v=vs.85)">RectF::Contains</a> method determines whether the point (<i>x</i>, <i>y</i>) is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-contains(inconstrectf_)">RectF::Contains(RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-contains(inconstrectf_)">RectF::Contains</a> method determines whether another rectangle is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-equals">RectF::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-equals">RectF::Equals</a> method determines whether two rectangles are the same. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getbottom">RectF::GetBottom</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getbottom">RectF::GetBottom</a> method gets the y-coordinate of the bottom edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getbounds">RectF::GetBounds</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getbounds">RectF::GetBounds</a> method makes a copy of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getleft">RectF::GetLeft</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getleft">RectF::GetLeft</a> method gets the x-coordinate of the left edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getlocation">RectF::GetLocation</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getlocation">RectF::GetLocation</a> method gets the coordinates of the upper-left corner of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getright">RectF::GetRight</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getright">RectF::GetRight</a> method gets the x-coordinate of the right edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getsize">RectF::GetSize</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-getsize">RectF::GetSize</a> method gets the width and height of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-gettop">RectF::GetTop</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-gettop">RectF::GetTop</a> method gets the y-coordinate of the top edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-inflate(inconstpointf_)">RectF::Inflate(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-inflate(inconstpointf_)">RectF::Inflate</a> method expands the rectangle by the value of 
			<i>point</i>.<b>X</b> on the left and right edges, and by the value of 
			<i>point</i>.<b>Y</b> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms534953(v=vs.85)">RectF::Inflate(REAL,REAL)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/ms534953(v=vs.85)">RectF::Inflate</a> method expands the rectangle by 
			<i>dx</i> on the left and right edges, and by 
			<i>dy</i> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms534950(v=vs.85)">RectF::Intersect(RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/ms534950(v=vs.85)">RectF::Intersect</a> method replaces this rectangle with the intersection of itself and another rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-intersect(outrectf__inconstrectf__inconstrectf_)">RectF::Intersect(RectF&,RectF&,RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-intersect(outrectf__inconstrectf__inconstrectf_)">RectF::Intersect</a> method determines the intersection of two rectangles and stores the result in a 
			<b>RectF</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-intersectswith">RectF::IntersectsWith</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-intersectswith">RectF::IntersectsWith</a> method determines whether this rectangle intersects another rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-isemptyarea">RectF::IsEmptyArea</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-isemptyarea">RectF::IsEmptyArea</a> method determines whether this rectangle is empty.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms534948(v=vs.85)">RectF::Offset(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/ms534948(v=vs.85)">RectF::Offset</a> method moves this rectangle horizontally a distance of 
			<i>point</i>.<b>X</b> and vertically a distance of 
			<i>point</i>.<b>Y</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-offset(inreal_inreal)">RectF::Offset(REAL,REAL)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-offset(inreal_inreal)">RectF::Offset</a> method moves the rectangle by 
			<i>dx</i> horizontally and by 
			<i>dx</i> vertically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-union">RectF::Union</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rectf-union">RectF::Union</a> method determines the union of two rectangles and stores the result in a 
			<b>RectF</b> object. 

</td>
</tr>
</table>

## -remarks

The upper-left corner of the rectangle is located at (
				<i>x</i>, 
				<i>y</i>). The size of the rectangle is measured by 
				<i>width</i> and 
				<i>height</i>. There are methods for high-level functionality, such as moving, resizing, and performing or testing interactions with other rectangles.

