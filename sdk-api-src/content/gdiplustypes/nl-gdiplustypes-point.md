---
UID: NL:gdiplustypes.Point
title: Point
author: windows-sdk-content
description: The Point class encapsulates a point in a 2-D coordinate system.
old-location: gdiplus\_gdiplus_CLASS_Point_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\point.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Point, Point class [GDI+], Point class [GDI+],described, _gdiplus_CLASS_Point_Class, gdiplus._gdiplus_CLASS_Point_Class, gdiplustypes/Point
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
 - Point
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
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
<a href="https://msdn.microsoft.com/en-us/library/ms535010(v=VS.85).aspx">Point::Point()</a>
</td>
<td align="left" width="63%">
Creates a <b>Point</b> object and initializes the 
			<b>X</b> and 
			<b>Y</b> data members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535011(v=VS.85).aspx">Point::Point(INT,INT)</a>
</td>
<td align="left" width="63%">
Creates a <b>Point</b> object using two integers to initialize the 
			<b>X</b> and 
			<b>Y</b> data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535012(v=VS.85).aspx">Point::Point(Point&)</a>
</td>
<td align="left" width="63%">
Creates a new <b>Point</b> object and copies the data members from another <b>Point</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535013(v=VS.85).aspx">Point::Point(Size&)</a>
</td>
<td align="left" width="63%">
Creates a <b>Point</b> object using a 
			<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">Size</a> object to initialize the 
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
<a href="https://msdn.microsoft.com/en-us/library/ms535007(v=VS.85).aspx">Point::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535007(v=VS.85).aspx">Point::Equals</a> method determines whether two 
			<b>Point</b> objects are equal. Two points are considered equal if they have the same 
			<b>X</b> and 
			<b>Y</b>  data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535009(v=VS.85).aspx">Point::operator-(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535009(v=VS.85).aspx">Point::operator-</a> method subtracts the <b>X</b> and <b>Y</b> data members of two <b>Point</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms535008(v=VS.85).aspx">Point::operator+(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms535008(v=VS.85).aspx">Point::operator+</a> method adds the <b>X</b> and <b>Y</b> data members of two <b>Point</b> objects.

</td>
</tr>
</table> 

