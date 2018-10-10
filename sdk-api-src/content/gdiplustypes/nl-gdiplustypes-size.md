---
UID: NL:gdiplustypes.Size
title: Size
author: windows-sdk-content
description: The Size class encapsulates a Width and Height dimension in a 2-D coordinate system.
old-location: gdiplus\_gdiplus_CLASS_Size_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\size.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Size, Size class [GDI+], Size class [GDI+],described, _gdiplus_CLASS_Size_Class, gdiplus._gdiplus_CLASS_Size_Class, gdiplustypes/Size
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
 - Size
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Size class


## -description


The <b>Size</b> class encapsulates a 
			<b>Width</b> and 
			<b>Height</b> dimension in a 2-D coordinate system.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Size</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Size</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534753(v=VS.85).aspx">Size::Size()</a>
</td>
<td align="left" width="63%">
Creates a new <b>Size</b> object and initializes the members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534754(v=VS.85).aspx">Size::Size(INT,INT)</a>
</td>
<td align="left" width="63%">
Creates a <b>Size</b> object and initializes its 
			<b>Width</b> and 
			<b>Height</b> data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534755(v=VS.85).aspx">Size::Size(Size&)</a>
</td>
<td align="left" width="63%">
Creates a <b>Size</b> object and initializes its members by copying the members of another <b>Size</b> object.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>Size</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534749(v=VS.85).aspx">Size::Empty</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534749(v=VS.85).aspx">Size::Empty</a> method determines whether a 
			<b>Size</b> object is empty.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534750(v=VS.85).aspx">Size::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534750(v=VS.85).aspx">Size::Equals</a> method determines whether two 
			<b>Size</b> objects are equal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534752(v=VS.85).aspx">Size::operator-(Size&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534752(v=VS.85).aspx">Size::operator-</a> method subtracts the <b>Width</b> and <b>Height</b> data members of two <b>Size</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms534751(v=VS.85).aspx">Size::operator+(Size&)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms534751(v=VS.85).aspx">Size::operator+</a> method adds the <b>Width</b> and <b>Height</b> data members of two <b>Size</b> objects.

</td>
</tr>
</table> 

