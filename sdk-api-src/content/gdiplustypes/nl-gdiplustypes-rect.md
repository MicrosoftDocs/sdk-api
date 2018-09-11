---
UID: NL:gdiplustypes.Rect
title: Rect
author: windows-sdk-content
description: A Rect object stores the upper-left corner, width, and height of a rectangle.
old-location: gdiplus\_gdiplus_CLASS_Rect_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rect.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Rect, Rect class [GDI+], Rect class [GDI+],described, _gdiplus_CLASS_Rect_Class, gdiplus._gdiplus_CLASS_Rect_Class, gdiplustypes/Rect
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/ms534987(v=VS.85).aspx">Rect::Rect()</a>
</td>
<td align="left" width="63%">
Creates a <b>Rect</b> object whose x-coordinate, y-coordinate, width, and height are all zero. This is the default constructor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534989(v=VS.85).aspx">Rect::Rect(INT,INT,INT,INT)</a>
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
<a href="https://msdn.microsoft.com/en-us/library/ms534988(v=VS.85).aspx">Rect::Rect(Point&,Size&)</a>
</td>
<td align="left" width="63%">
Creates a <b>Rect</b> object by using a <a href="https://msdn.microsoft.com/en-us/library/ms534487(v=VS.85).aspx">Point</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members and a <a href="https://msdn.microsoft.com/en-us/library/ms534504(v=VS.85).aspx">Size</a> object to initialize the 
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
<a href="https://msdn.microsoft.com/en-us/library/ms534962(v=VS.85).aspx">Rect::Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534962(v=VS.85).aspx">Rect::Clone</a> method creates a new 
			<b>Rect</b> object and initializes it with the contents of this <b>Rect</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534986(v=VS.85).aspx">Rect::Contains(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534986(v=VS.85).aspx">Rect::Contains</a> method determines whether the point (
			<i>x</i>, 
			<i>y</i>) is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534984(v=VS.85).aspx">Rect::Contains(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534984(v=VS.85).aspx">Rect::Contains</a> method determines whether a point is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534985(v=VS.85).aspx">Rect::Contains(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534985(v=VS.85).aspx">Rect::Contains</a> method determines whether another rectangle is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534963(v=VS.85).aspx">Rect::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534963(v=VS.85).aspx">Rect::Equals</a> method determines whether two rectangles are the same. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534964(v=VS.85).aspx">Rect::GetBottom</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534964(v=VS.85).aspx">Rect::GetBottom</a> method gets the y-coordinate of the bottom edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534965(v=VS.85).aspx">Rect::GetBounds</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534965(v=VS.85).aspx">Rect::GetBounds</a> method makes a copy of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534966(v=VS.85).aspx">Rect::GetLeft</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534966(v=VS.85).aspx">Rect::GetLeft</a> method gets the x-coordinate of the left edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534967(v=VS.85).aspx">Rect::GetLocation</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534967(v=VS.85).aspx">Rect::GetLocation</a> method gets the coordinates of the upper-left corner of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534968(v=VS.85).aspx">Rect::GetRight</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534968(v=VS.85).aspx">Rect::GetRight</a> method gets the x-coordinate of the right edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534969(v=VS.85).aspx">Rect::GetSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534969(v=VS.85).aspx">Rect::GetSize</a> method gets the width and height of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534970(v=VS.85).aspx">Rect::GetTop</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534970(v=VS.85).aspx">Rect::GetTop</a> method gets the y-coordinate of the top edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534982(v=VS.85).aspx">Rect::Inflate(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534982(v=VS.85).aspx">Rect::Inflate</a> method expands the rectangle by 
			<i>dx</i> on the left and right edges, and by 
			<i>dy</i> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534983(v=VS.85).aspx">Rect::Inflate(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534983(v=VS.85).aspx">Rect::Inflate</a> method expands the rectangle by the value of <i>point</i>.<b>X</b> on the left and right edges, and by the value of 
			<i>point</i>.<b>Y</b> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534981(v=VS.85).aspx">Rect::Intersect(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534981(v=VS.85).aspx">Rect::Intersect</a> method replaces this rectangle with the intersection of itself and another rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534980(v=VS.85).aspx">Rect::Intersect(Rect&,Rect&,Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534980(v=VS.85).aspx">Rect::Intersect</a> method determines the intersection of two rectangles and stores the result in a 
			<b>Rect</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534971(v=VS.85).aspx">Rect::IntersectsWith</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534971(v=VS.85).aspx">Rect::IntersectsWith</a> method determines whether this rectangle intersects another rectangle. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534972(v=VS.85).aspx">Rect::IsEmptyArea</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534972(v=VS.85).aspx">Rect::IsEmptyArea</a> method determines whether this rectangle is empty.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534978(v=VS.85).aspx">Rect::Offset(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534978(v=VS.85).aspx">Rect::Offset</a> method moves the rectangle by 
			<i>dx</i> horizontally and by 
			<i>dy</i> vertically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534979(v=VS.85).aspx">Rect::Offset(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534979(v=VS.85).aspx">Rect::Offset</a> method moves this rectangle horizontally a distance of 
			 <i>point</i>.<b>X</b> and vertically a distance of 
			<i>point</i>.<b>Y</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534977(v=VS.85).aspx">Rect::Union</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534977(v=VS.85).aspx">Rect::Union</a> method determines the union of two rectangles and stores the result in a 
			<b>Rect</b> object. 

</td>
</tr>
</table> 

