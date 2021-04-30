---
UID: NL:gdiplustypes.Point
title: Point (gdiplustypes.h)
description: The Point class encapsulates a point in a 2-D coordinate system.
helpviewer_keywords: ["Point","Point class [GDI+]","Point class [GDI+]","described","_gdiplus_CLASS_Point_Class","gdiplus._gdiplus_CLASS_Point_Class","gdiplustypes/Point"]
old-location: gdiplus\_gdiplus_CLASS_Point_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\point.htm
ms.date: 12/05/2018
ms.keywords: Point, Point class [GDI+], Point class [GDI+],described, _gdiplus_CLASS_Point_Class, gdiplus._gdiplus_CLASS_Point_Class, gdiplustypes/Point
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
 - Point
 - gdiplustypes/Point
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
 - Point
---

# Point class


## -description

The <b>Point</b> class encapsulates a point in a 2-D coordinate system.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Point</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Point</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-point-point(inconstpoint_)">Point::Point()</a>
</td>
<td align="left" width="63%">
Creates a <b>Point</b> object and initializes the 
			<b>X</b> and 
			<b>Y</b> data members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-point-point(inint_inint)">Point::Point(INT,INT)</a>
</td>
<td align="left" width="63%">
Creates a <b>Point</b> object using two integers to initialize the 
			<b>X</b> and 
			<b>Y</b> data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-point-point(inconstpoint_)">Point::Point(Point&)</a>
</td>
<td align="left" width="63%">
Creates a new <b>Point</b> object and copies the data members from another <b>Point</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-point-point(inconstsize_)">Point::Point(Size&)</a>
</td>
<td align="left" width="63%">
Creates a <b>Point</b> object using a 
			<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-size">Size</a> object to initialize the 
			<b>X</b> and 
			<b>Y</b> data members.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>Point</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-point-equals">Point::Equals</a>
</td>
<td align="left" width="63%">
The <a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-point-equals">Point::Equals</a> method determines whether two 
			<b>Point</b> objects are equal. Two points are considered equal if they have the same 
			<b>X</b> and 
			<b>Y</b>  data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/ms535009(v=vs.85)">Point::operator-(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/ms535009(v=vs.85)">Point::operator-</a> method subtracts the <b>X</b> and <b>Y</b> data members of two <b>Point</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/ms535008(v=vs.85)">Point::operator+(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="/previous-versions/ms535008(v=vs.85)">Point::operator+</a> method adds the <b>X</b> and <b>Y</b> data members of two <b>Point</b> objects.

</td>
</tr>
</table>