---
UID: NL:gdiplustypes.RectF
title: RectF
author: windows-sdk-content
description: A RectF object stores the upper-left corner, width, and height of a rectangle.
old-location: gdiplus\_gdiplus_CLASS_RectF_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\rectf.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: RectF, RectF class [GDI+], RectF class [GDI+],described, _gdiplus_CLASS_RectF_Class, gdiplus._gdiplus_CLASS_RectF_Class, gdiplustypes/RectF
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
 - RectF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/2a0687cb-d21f-4279-94e5-ec2bf3630936">RectF::RectF()</a>
</td>
<td align="left" width="63%">
Creates a <b>RectF</b> object and initializes the 
			<b>X</b> and 
			<b>Y</b> data members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba570d9e-d80b-4248-8e0b-3dea32945ace">RectF::RectF(PointF&,SizeF&)</a>
</td>
<td align="left" width="63%">
Creates a <b>RectF</b> object by using a <a href="https://msdn.microsoft.com/2d357844-19a8-4ada-ba1e-685fea2e65ce">PointF</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members and uses a <a href="https://msdn.microsoft.com/b40ade07-f89e-44ba-9185-9aec01f1051f">SizeF</a> object to initialize the 
			<b>Width</b> and 
			<b>Height</b> data members of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72c43bb0-9ab5-47d0-af4f-f7c0882b6834">RectF::RectF(REAL,REAL,REAL,REAL)</a>
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
<a href="https://msdn.microsoft.com/6080802b-c484-465e-9fad-14ac7bebe5f3">RectF::Clone</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6080802b-c484-465e-9fad-14ac7bebe5f3">RectF::Clone</a> method creates a new 
			<b>RectF</b> object and initializes it with the contents of this 
			<b>RectF</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adeb5a20-1ef0-4811-a16a-3e9d06c05cf7">RectF::Contains(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/adeb5a20-1ef0-4811-a16a-3e9d06c05cf7">RectF::Contains</a> method determines whether a point is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6aa28593-4692-44e9-984c-fd25b519dd14">RectF::Contains(REAL,REAL)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6aa28593-4692-44e9-984c-fd25b519dd14">RectF::Contains</a> method determines whether the point (<i>x</i>, <i>y</i>) is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f27723a8-173b-4eb9-b003-d74e9cb16154">RectF::Contains(RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/f27723a8-173b-4eb9-b003-d74e9cb16154">RectF::Contains</a> method determines whether another rectangle is inside this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7381200-c2d4-45c2-a388-68b9efd510f7">RectF::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c7381200-c2d4-45c2-a388-68b9efd510f7">RectF::Equals</a> method determines whether two rectangles are the same. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c511582e-53d2-4857-a1dd-8cacbc46cbf3">RectF::GetBottom</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c511582e-53d2-4857-a1dd-8cacbc46cbf3">RectF::GetBottom</a> method gets the y-coordinate of the bottom edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7287b87d-7022-49db-a216-b20f54c18809">RectF::GetBounds</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/7287b87d-7022-49db-a216-b20f54c18809">RectF::GetBounds</a> method makes a copy of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c6c814c-9663-4c7f-8230-a97409813c2a">RectF::GetLeft</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/0c6c814c-9663-4c7f-8230-a97409813c2a">RectF::GetLeft</a> method gets the x-coordinate of the left edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b7a6b31-b481-4c63-8ad9-a2f7c19dcf23">RectF::GetLocation</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/4b7a6b31-b481-4c63-8ad9-a2f7c19dcf23">RectF::GetLocation</a> method gets the coordinates of the upper-left corner of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/410d35bc-3348-42fb-8fba-dbcdfac8b9a1">RectF::GetRight</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/410d35bc-3348-42fb-8fba-dbcdfac8b9a1">RectF::GetRight</a> method gets the x-coordinate of the right edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35c271c7-742c-451e-9978-7fe7368a717a">RectF::GetSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/35c271c7-742c-451e-9978-7fe7368a717a">RectF::GetSize</a> method gets the width and height of this rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cfcb80b-6195-4eab-b319-cfb57cd294fc">RectF::GetTop</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/9cfcb80b-6195-4eab-b319-cfb57cd294fc">RectF::GetTop</a> method gets the y-coordinate of the top edge of the rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb5015a9-e0a5-4a17-9526-6e5c7968d275">RectF::Inflate(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bb5015a9-e0a5-4a17-9526-6e5c7968d275">RectF::Inflate</a> method expands the rectangle by the value of 
			<i>point</i>.<b>X</b> on the left and right edges, and by the value of 
			<i>point</i>.<b>Y</b> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b865a13e-b95d-4a07-9003-9821c878fb7b">RectF::Inflate(REAL,REAL)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b865a13e-b95d-4a07-9003-9821c878fb7b">RectF::Inflate</a> method expands the rectangle by 
			<i>dx</i> on the left and right edges, and by 
			<i>dy</i> on the top and bottom edges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6472A5EF-768E-4114-8BB0-CF641DD5337D">RectF::Intersect(RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6472A5EF-768E-4114-8BB0-CF641DD5337D">RectF::Intersect</a> method replaces this rectangle with the intersection of itself and another rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94375436-B522-454F-A66E-1D3B99CDCCF7">RectF::Intersect(RectF&,RectF&,RectF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/94375436-B522-454F-A66E-1D3B99CDCCF7">RectF::Intersect</a> method determines the intersection of two rectangles and stores the result in a 
			<b>RectF</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66b28920-fee3-49ee-b919-a9792197499c">RectF::IntersectsWith</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/66b28920-fee3-49ee-b919-a9792197499c">RectF::IntersectsWith</a> method determines whether this rectangle intersects another rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77a6f4b9-1e4c-4258-9489-5a26b6e7e566">RectF::IsEmptyArea</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/77a6f4b9-1e4c-4258-9489-5a26b6e7e566">RectF::IsEmptyArea</a> method determines whether this rectangle is empty.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DEDAC79D-94D3-4A7F-9FD0-E892CF027697">RectF::Offset(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/DEDAC79D-94D3-4A7F-9FD0-E892CF027697">RectF::Offset</a> method moves this rectangle horizontally a distance of 
			<i>point</i>.<b>X</b> and vertically a distance of 
			<i>point</i>.<b>Y</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F4FB5146-7D9E-4DF1-BE00-FDD90D3C82AE">RectF::Offset(REAL,REAL)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/F4FB5146-7D9E-4DF1-BE00-FDD90D3C82AE">RectF::Offset</a> method moves the rectangle by 
			<i>dx</i> horizontally and by 
			<i>dx</i> vertically.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82dbe9ea-62ea-4838-961e-f947b84a7a28">RectF::Union</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/82dbe9ea-62ea-4838-961e-f947b84a7a28">RectF::Union</a> method determines the union of two rectangles and stores the result in a 
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



