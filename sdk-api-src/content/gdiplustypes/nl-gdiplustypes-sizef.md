---
UID: NL:gdiplustypes.SizeF
title: SizeF
author: windows-sdk-content
description: The SizeF class encapsulates a Width and Height dimension in a 2-D coordinate system. The SizeF class uses floating point coordinates.
old-location: gdiplus\_gdiplus_CLASS_SizeF_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\sizef.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: SizeF, SizeF class [GDI+], SizeF class [GDI+],described, _gdiplus_CLASS_SizeF_Class, gdiplus._gdiplus_CLASS_SizeF_Class, gdiplustypes/SizeF
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
 - SizeF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SizeF class


## -description


The <b>SizeF</b> class encapsulates a 
			<b>Width</b> and 
			<b>Height</b> dimension in a 2-D coordinate system. The <b>SizeF</b> class uses floating point coordinates.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">SizeF</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SizeF</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534744(v=VS.85).aspx">SizeF::SizeF()</a>
</td>
<td align="left" width="63%">
Creates a <b>SizeF</b> object and initializes the members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534745(v=VS.85).aspx">SizeF::SizeF(REAL,REAL)</a>
</td>
<td align="left" width="63%">
Creates a <b>SizeF</b> object and initializes its 
			<b>Width</b> and 
			<b>Height</b> data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534746(v=VS.85).aspx">SizeF::SizeF(SizeF&)</a>
</td>
<td align="left" width="63%">
Creates a <b>SizeF</b> object and initializes its members by copying the members of another <b>SizeF</b> object.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>SizeF</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534740(v=VS.85).aspx">SizeF::Empty</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534740(v=VS.85).aspx">SizeF::Empty</a> method determines whether a 
			<b>SizeF</b> object is empty.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534741(v=VS.85).aspx">SizeF::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534741(v=VS.85).aspx">SizeF::Equals</a> method determines whether two 
			<b>SizeF</b> objects are equal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534743(v=VS.85).aspx">SizeF::operator-(SizeF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534743(v=VS.85).aspx">SizeF::operator-</a> method subtracts the <b>Width</b> and <b>Height</b> data members of two <b>SizeF</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534742(v=VS.85).aspx">SizeF::operator+(SizeF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534742(v=VS.85).aspx">SizeF::operator+</a> method adds the <b>Width</b> and <b>Height</b> data members of two <b>SizeF</b> objects.

</td>
</tr>
</table> 

