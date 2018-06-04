---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PointF class


## -description


The <b>PointF</b> class encapsulates a point in a 2-D coordinate system.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">PointF</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">PointF</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3e10636-81e8-48e4-b767-c325b3e8f4d8">PointF::PointF()</a>
</td>
<td align="left" width="63%">
Creates a <b>PointF</b> object and initializes the 
			<b>X</b> and 
			<b>Y</b> data members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db4d7765-892e-4f41-94a8-c82aa5155c19">PointF::PointF(PointF&)</a>
</td>
<td align="left" width="63%">
Creates a new <b>PointF</b> object and copies the data from another <b>PointF</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bb7bbb8-7d0c-41bb-a649-2ba4d62fb2c1">PointF::PointF(REAL,REAL)</a>
</td>
<td align="left" width="63%">
Creates a <b>PointF</b> object using two real numbers to specify the 
			<b>X</b> and 
			<b>Y</b> data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e571657e-e13c-4627-8a12-250358b20682">PointF::PointF(SizeF&)</a>
</td>
<td align="left" width="63%">
Creates a <b>PointF</b> object using a 
			<a href="https://msdn.microsoft.com/b40ade07-f89e-44ba-9185-9aec01f1051f">SizeF</a> object to specify the 
			<b>X</b> and 
			<b>Y</b> data members.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>PointF</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/690b3fa5-4543-45da-af37-a22333fc4db9">PointF::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/690b3fa5-4543-45da-af37-a22333fc4db9">PointF::Equals</a> method determines whether two 
			<b>PointF</b> objects are equal. Two points are considered equal if they have the same 
			<b>X</b> and 
			<b>Y</b>  data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da1f7f42-09e7-4889-9fd7-6eeed3a0b59c">PointF::operator-(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/da1f7f42-09e7-4889-9fd7-6eeed3a0b59c">PointF::operator-</a> method subtracts the <b>X</b> and <b>Y</b> data members of two <b>PointF</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38e628ec-b031-4e8a-be24-504bd56b2bd7">PointF::operator+(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/38e628ec-b031-4e8a-be24-504bd56b2bd7">PointF::operator+</a> method adds the <b>X</b> and <b>Y</b> data members of two <b>PointF</b> objects.

</td>
</tr>
</table> 

