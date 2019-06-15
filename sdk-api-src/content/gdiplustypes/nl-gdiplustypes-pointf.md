---
UID: NL:gdiplustypes.PointF
title: PointF (gdiplustypes.h)
author: windows-sdk-content
description: The PointF class encapsulates a point in a 2-D coordinate system.
old-location: gdiplus\_gdiplus_CLASS_PointF_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\pointf.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PointF, PointF class [GDI+], PointF class [GDI+],described, _gdiplus_CLASS_PointF_Class, gdiplus._gdiplus_CLASS_PointF_Class, gdiplustypes/PointF
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
 - PointF
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-pointf-pointf(inconstpointf_)">PointF::PointF()</a>
</td>
<td align="left" width="63%">
Creates a <b>PointF</b> object and initializes the 
			<b>X</b> and 
			<b>Y</b> data members to zero. This is the default constructor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-pointf-pointf(inconstpointf_)">PointF::PointF(PointF&)</a>
</td>
<td align="left" width="63%">
Creates a new <b>PointF</b> object and copies the data from another <b>PointF</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-pointf-pointf(inreal_inreal)">PointF::PointF(REAL,REAL)</a>
</td>
<td align="left" width="63%">
Creates a <b>PointF</b> object using two real numbers to specify the 
			<b>X</b> and 
			<b>Y</b> data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-pointf-pointf(inconstsizef_)">PointF::PointF(SizeF&)</a>
</td>
<td align="left" width="63%">
Creates a <b>PointF</b> object using a 
			<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nl-gdiplustypes-sizef">SizeF</a> object to specify the 
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
<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-pointf-equals">PointF::Equals</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/nf-gdiplustypes-pointf-equals">PointF::Equals</a> method determines whether two 
			<b>PointF</b> objects are equal. Two points are considered equal if they have the same 
			<b>X</b> and 
			<b>Y</b>  data members.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms534998(v=vs.85)">PointF::operator-(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions//ms534998(v=vs.85)">PointF::operator-</a> method subtracts the <b>X</b> and <b>Y</b> data members of two <b>PointF</b> objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions//ms534997(v=vs.85)">PointF::operator+(PointF&)</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/previous-versions//ms534997(v=vs.85)">PointF::operator+</a> method adds the <b>X</b> and <b>Y</b> data members of two <b>PointF</b> objects.

</td>
</tr>
</table> 

