---
UID: NL:gdiplustypes.CharacterRange
title: CharacterRange (gdiplustypes.h)
description: A CharacterRange object specifies a range of character positions within a string.
helpviewer_keywords: ["CharacterRange","CharacterRange class [GDI+]","CharacterRange class [GDI+]","described","_gdiplus_CLASS_CharacterRange_Class","gdiplus._gdiplus_CLASS_CharacterRange_Class","gdiplustypes/CharacterRange"]
old-location: gdiplus\_gdiplus_CLASS_CharacterRange_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\characterrange.htm
ms.date: 12/05/2018
ms.keywords: CharacterRange, CharacterRange class [GDI+], CharacterRange class [GDI+],described, _gdiplus_CLASS_CharacterRange_Class, gdiplus._gdiplus_CLASS_CharacterRange_Class, gdiplustypes/CharacterRange
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
 - CharacterRange
 - gdiplustypes/CharacterRange
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
 - CharacterRange
---

# CharacterRange class


## -description

A <a href="/previous-versions/ms536266(v=vs.85)">CharacterRange</a> object specifies a range of character positions within a string.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CharacterRange</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CharacterRange</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-characterrange-characterrange~r2">CharacterRange::CharacterRange()</a>
</td>
<td align="left" width="63%">
Creates a <a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-characterrange-characterrange~r2">CharacterRange::CharacterRange</a> object with the data members set to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-characterrange-characterrange(int_int)">CharacterRange::CharacterRange(INT,INT)</a>
</td>
<td align="left" width="63%">
Creates a <a href="/windows/desktop/api/gdiplustypes/nf-gdiplustypes-characterrange-characterrange(int_int)">CharacterRange::CharacterRange</a> object and initializes the data members to the values specified.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CharacterRange</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
[CharacterRange::operator=](./nf-gdiplustypes-characterrange-operator-assign.md)
</td>
<td align="left" width="63%">
The [CharacterRange::operator=](./nf-gdiplustypes-characterrange-operator-assign.md) method sets this <b>CharacterRange</b> object equal to the specified <b>CharacterRange</b> object.

</td>
</tr>
</table>

## -remarks

A character range is a range of character positions within a string of text. The area of the display that is occupied by a group of characters that are specified by the character range is the bounding region. A character range is set by 
				<b>StringFormat::SetMeasurableCharacterRanges</b>. The number of ranges that are currently set can be determined by calling 
				<b>StringFormat::GetMeasurableCharacterRangeCount</b>. This number is also the number of regions expected to be obtained by the 
				<b>MeasureCharacterRanges</b> method.