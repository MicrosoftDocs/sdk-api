---
UID: NL:gdiplustypes.Rect
title: Rect (gdiplustypes.h)
author: windows-sdk-content
description: A Rect object stores the upper-left corner, width, and height of a rectangle.
old-location: gdiplus\_gdiplus_CLASS_Rect_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Rect, Rect class [GDI+], Rect class [GDI+],described, _gdiplus_CLASS_Rect_Class, gdiplus._gdiplus_CLASS_Rect_Class, gdiplustypes/Rect
ms.topic: class
f1_keywords: 
 - "gdiplustypes/Rect"
dev_langs:
 - c++
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
 - Rect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Rect class


## -description


A <b>Rect</b> object stores the upper-left corner, width, and height of a rectangle.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Rect</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Rect</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-rect(inconstpoint__inconstsize_)">Rect::Rect()</a>
</td>
<td align="left" width="63%">
Creates a <b>Rect</b> object whose x-coordinate, y-coordinate, width, and height are all zero. This is the default constructor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-rect(inint_inint_inint_inint)">Rect::Rect(INT,INT,INT,INT)</a>
</td>
<td align="left" width="63%">
Creates a <b>Rect</b> object by using four integers to initialize the 
			<b>X</b>, 
			<b>Y</b>, 
			<b>Width</b>, and 
			<b>Height</b> data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-rect(inconstpoint__inconstsize_)">Rect::Rect(Point&,Size&)</a>
</td>
<td align="left" width="63%">
Creates a <b>Rect</b> object by using a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-point">Point</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members and a <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object to initialize the 
			<b>Width</b> and 
			<b>Height</b> data members.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>Rect</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-clone">Rect::Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-clone">Rect::Clone</a> method creates a new 
			<b>Rect</b> object and initializes it with the contents of this <b>Rect</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms534986(v=vs.85)">Rect::Contains(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/ms534986(v=vs.85)">Rect::Contains</a> method determines whether the point (
			<i>x</i>, 
			<i>y</i>) is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-contains(inconstpoint_)">Rect::Contains(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-contains(inconstpoint_)">Rect::Contains</a> method determines whether a point is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-contains(inrect_)">Rect::Contains(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-contains(inrect_)">Rect::Contains</a> method determines whether another rectangle is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-equals">Rect::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-equals">Rect::Equals</a> method determines whether two rectangles are the same. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getbottom">Rect::GetBottom</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getbottom">Rect::GetBottom</a> method gets the y-coordinate of the bottom edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getbounds">Rect::GetBounds</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getbounds">Rect::GetBounds</a> method makes a copy of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getleft">Rect::GetLeft</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getleft">Rect::GetLeft</a> method gets the x-coordinate of the left edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getlocation">Rect::GetLocation</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getlocation">Rect::GetLocation</a> method gets the coordinates of the upper-left corner of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getright">Rect::GetRight</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getright">Rect::GetRight</a> method gets the x-coordinate of the right edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getsize">Rect::GetSize</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-getsize">Rect::GetSize</a> method gets the width and height of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-gettop">Rect::GetTop</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-gettop">Rect::GetTop</a> method gets the y-coordinate of the top edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms534982(v=vs.85)">Rect::Inflate(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/ms534982(v=vs.85)">Rect::Inflate</a> method expands the rectangle by 
			<i>dx</i> on the left and right edges, and by 
			<i>dy</i> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inconstpoint_)">Rect::Inflate(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-inflate(inconstpoint_)">Rect::Inflate</a> method expands the rectangle by the value of <i>point</i>.<b>X</b> on the left and right edges, and by the value of 
			<i>point</i>.<b>Y</b> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms534981(v=vs.85)">Rect::Intersect(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/ms534981(v=vs.85)">Rect::Intersect</a> method replaces this rectangle with the intersection of itself and another rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-intersect(outrect__inconstrect__inconstrect_)">Rect::Intersect(Rect&,Rect&,Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-intersect(outrect__inconstrect__inconstrect_)">Rect::Intersect</a> method determines the intersection of two rectangles and stores the result in a 
			<b>Rect</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-intersectswith">Rect::IntersectsWith</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-intersectswith">Rect::IntersectsWith</a> method determines whether this rectangle intersects another rectangle. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-isemptyarea">Rect::IsEmptyArea</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-isemptyarea">Rect::IsEmptyArea</a> method determines whether this rectangle is empty.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-offset(inint_inint)">Rect::Offset(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-offset(inint_inint)">Rect::Offset</a> method moves the rectangle by 
			<i>dx</i> horizontally and by 
			<i>dy</i> vertically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/ms534979(v=vs.85)">Rect::Offset(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions/ms534979(v=vs.85)">Rect::Offset</a> method moves this rectangle horizontally a distance of 
			 <i>point</i>.<b>X</b> and vertically a distance of 
			<i>point</i>.<b>Y</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-union">Rect::Union</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-rect-union">Rect::Union</a> method determines the union of two rectangles and stores the result in a 
			<b>Rect</b> object. 

</td>
</tr>
</table> 

