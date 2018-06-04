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
<a href="https://msdn.microsoft.com/41e53402-0fa3-472b-b3e1-cdb16d1b0947">Point::Point()</a>
</td>
<td align="left" width="63%">
Creates a <b>Point</b> object and initializes the 
			<b>X</b> and 
			<b>Y</b> data members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8081890b-5ec0-45c9-9cfe-61c0ee0787c4">Point::Point(INT,INT)</a>
</td>
<td align="left" width="63%">
Creates a <b>Point</b> object using two integers to initialize the 
			<b>X</b> and 
			<b>Y</b> data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4125bb02-471f-4694-ab36-8b3088479242">Point::Point(Point&)</a>
</td>
<td align="left" width="63%">
Creates a new <b>Point</b> object and copies the data members from another <b>Point</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16e6f406-9139-4341-8469-1d6345889c86">Point::Point(Size&)</a>
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
<a href="https://msdn.microsoft.com/b3719463-8cbf-44c4-bf0b-6673a37d322f">Point::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b3719463-8cbf-44c4-bf0b-6673a37d322f">Point::Equals</a> method determines whether two 
			<b>Point</b> objects are equal. Two points are considered equal if they have the same 
			<b>X</b> and 
			<b>Y</b>  data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcd6e8db-7584-4209-8c0a-6ce64c8724ce">Point::operator-(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/bcd6e8db-7584-4209-8c0a-6ce64c8724ce">Point::operator-</a> method subtracts the <b>X</b> and <b>Y</b> data members of two <b>Point</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/751eea61-b0c6-4112-bf0b-2936d12fb97e">Point::operator+(Point&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/751eea61-b0c6-4112-bf0b-2936d12fb97e">Point::operator+</a> method adds the <b>X</b> and <b>Y</b> data members of two <b>Point</b> objects.

</td>
</tr>
</table> 

