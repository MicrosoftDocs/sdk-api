---
UID: NL:gdiplustypes.Rect
title: Rect
author: windows-sdk-content
description: A Rect object stores the upper-left corner, width, and height of a rectangle.
old-location: gdiplus\_gdiplus_CLASS_Rect_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rect.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	gdiplustypes.h
api_name:
-	Rect
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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
<a href="https://msdn.microsoft.com/f81d9728-21bd-4996-8601-cb9c1b6819a7">Rect::Rect()</a>
</td>
<td align="left" width="63%">
Creates a <b>Rect</b> object whose x-coordinate, y-coordinate, width, and height are all zero. This is the default constructor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99855883-c2ff-4752-8141-0de86331e695">Rect::Rect(INT,INT,INT,INT)</a>
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
<a href="https://msdn.microsoft.com/684f9866-4b7a-426e-8f59-f59b9fa6ec6e">Rect::Rect(Point&,Size&)</a>
</td>
<td align="left" width="63%">
Creates a <b>Rect</b> object by using a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members and a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a> object to initialize the 
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
<a href="https://msdn.microsoft.com/841f648f-0001-49c2-b395-fa69f36379e4">Rect::Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/841f648f-0001-49c2-b395-fa69f36379e4">Rect::Clone</a> method creates a new 
			<b>Rect</b> object and initializes it with the contents of this <b>Rect</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f2d6333-9e50-45eb-b61f-441cc59f8b6b">Rect::Contains(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6f2d6333-9e50-45eb-b61f-441cc59f8b6b">Rect::Contains</a> method determines whether the point (
			<i>x</i>, 
			<i>y</i>) is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4758fa07-5098-40a9-89f8-17a8fe10a67f">Rect::Contains(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4758fa07-5098-40a9-89f8-17a8fe10a67f">Rect::Contains</a> method determines whether a point is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/266efa9d-9d78-401a-93e6-caacf19b977a">Rect::Contains(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/266efa9d-9d78-401a-93e6-caacf19b977a">Rect::Contains</a> method determines whether another rectangle is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/739a00b2-a3b7-4cb8-a168-38577ef60364">Rect::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/739a00b2-a3b7-4cb8-a168-38577ef60364">Rect::Equals</a> method determines whether two rectangles are the same. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbd3dd3e-e735-4dd0-888d-ab3f3ee185f1">Rect::GetBottom</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/dbd3dd3e-e735-4dd0-888d-ab3f3ee185f1">Rect::GetBottom</a> method gets the y-coordinate of the bottom edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17cf6bf6-ec5f-4bce-9ccd-fea7340ebe40">Rect::GetBounds</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/17cf6bf6-ec5f-4bce-9ccd-fea7340ebe40">Rect::GetBounds</a> method makes a copy of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b03a86b-370b-4da6-b287-5031fe7ff285">Rect::GetLeft</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/3b03a86b-370b-4da6-b287-5031fe7ff285">Rect::GetLeft</a> method gets the x-coordinate of the left edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f9049dd-3de3-4499-ae1e-5a9833fe1e10">Rect::GetLocation</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1f9049dd-3de3-4499-ae1e-5a9833fe1e10">Rect::GetLocation</a> method gets the coordinates of the upper-left corner of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f0bc568-67a0-48ab-a4a3-5582d925b47b">Rect::GetRight</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7f0bc568-67a0-48ab-a4a3-5582d925b47b">Rect::GetRight</a> method gets the x-coordinate of the right edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82e95dab-17fa-44b2-bb73-2e4a1ac1b0bf">Rect::GetSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/82e95dab-17fa-44b2-bb73-2e4a1ac1b0bf">Rect::GetSize</a> method gets the width and height of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c23c2ab-edbe-45c4-99bb-6fb3e39ebaba">Rect::GetTop</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6c23c2ab-edbe-45c4-99bb-6fb3e39ebaba">Rect::GetTop</a> method gets the y-coordinate of the top edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0601f59d-4ded-4224-b9c8-36499c3d381f">Rect::Inflate(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0601f59d-4ded-4224-b9c8-36499c3d381f">Rect::Inflate</a> method expands the rectangle by 
			<i>dx</i> on the left and right edges, and by 
			<i>dy</i> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/598dbe05-0edb-4c3b-ba2f-5ecf0ce47ce4">Rect::Inflate(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/598dbe05-0edb-4c3b-ba2f-5ecf0ce47ce4">Rect::Inflate</a> method expands the rectangle by the value of <i>point</i>.<b>X</b> on the left and right edges, and by the value of 
			<i>point</i>.<b>Y</b> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1869cefb-48d9-461c-9e6e-3150fce0a81e">Rect::Intersect(Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/1869cefb-48d9-461c-9e6e-3150fce0a81e">Rect::Intersect</a> method replaces this rectangle with the intersection of itself and another rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/992a721f-2fef-4518-9db1-fcf70ac68b4f">Rect::Intersect(Rect&,Rect&,Rect&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/992a721f-2fef-4518-9db1-fcf70ac68b4f">Rect::Intersect</a> method determines the intersection of two rectangles and stores the result in a 
			<b>Rect</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11b08c96-99a4-43bd-9dc0-86f2dbcbd712">Rect::IntersectsWith</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/11b08c96-99a4-43bd-9dc0-86f2dbcbd712">Rect::IntersectsWith</a> method determines whether this rectangle intersects another rectangle. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/feffd409-7874-4baf-80d4-82503e9951b1">Rect::IsEmptyArea</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/feffd409-7874-4baf-80d4-82503e9951b1">Rect::IsEmptyArea</a> method determines whether this rectangle is empty.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e660ded5-05e9-4786-8c82-922b5f118e49">Rect::Offset(INT,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/e660ded5-05e9-4786-8c82-922b5f118e49">Rect::Offset</a> method moves the rectangle by 
			<i>dx</i> horizontally and by 
			<i>dy</i> vertically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b10ddcf9-c76b-4f95-9295-3fffc80c2fb0">Rect::Offset(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b10ddcf9-c76b-4f95-9295-3fffc80c2fb0">Rect::Offset</a> method moves this rectangle horizontally a distance of 
			 <i>point</i>.<b>X</b> and vertically a distance of 
			<i>point</i>.<b>Y</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbd4c747-5a0b-41c9-92c5-60b7871e27c4">Rect::Union</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/fbd4c747-5a0b-41c9-92c5-60b7871e27c4">Rect::Union</a> method determines the union of two rectangles and stores the result in a 
			<b>Rect</b> object. 

</td>
</tr>
</table> 

