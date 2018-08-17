---
UID: NL:gdiplustypes.CharacterRange
title: CharacterRange
author: windows-sdk-content
description: A CharacterRange object specifies a range of character positions within a string.
old-location: gdiplus\_gdiplus_CLASS_CharacterRange_Class.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\characterrange.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: CharacterRange, CharacterRange class [GDI+], CharacterRange class [GDI+],described, _gdiplus_CLASS_CharacterRange_Class, gdiplus._gdiplus_CLASS_CharacterRange_Class, gdiplustypes/CharacterRange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: gdiplustypes.h
req.include-header: 
req.redist: 
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
 - CharacterRange
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# CharacterRange class


## -description


A <a href="https://msdn.microsoft.com/en-us/library/ms536266(v=VS.85).aspx">CharacterRange</a> object specifies a range of character positions within a string.

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
<a href="https://msdn.microsoft.com/en-us/library/ms536268(v=VS.85).aspx">CharacterRange::CharacterRange()</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536268(v=VS.85).aspx">CharacterRange::CharacterRange</a> object with the data members set to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536269(v=VS.85).aspx">CharacterRange::CharacterRange(INT,INT)</a>
</td>
<td align="left" width="63%">
Creates a <a href="https://msdn.microsoft.com/en-us/library/ms536269(v=VS.85).aspx">CharacterRange::CharacterRange</a> object and initializes the data members to the values specified.

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
<a href="https://msdn.microsoft.com/en-us/library/ms536267(v=VS.85).aspx">CharacterRange::operator=</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536267(v=VS.85).aspx">CharacterRange::operator=</a> method sets this <b>CharacterRange</b> object equal to the specified <b>CharacterRange</b> object.

</td>
</tr>
</table> 


## -remarks



A character range is a range of character positions within a string of text. The area of the display that is occupied by a group of characters that are specified by the character range is the bounding region. A character range is set by 
				<b>StringFormat::SetMeasurableCharacterRanges</b>. The number of ranges that are currently set can be determined by calling 
				<b>StringFormat::GetMeasurableCharacterRangeCount</b>. This number is also the number of regions expected to be obtained by the 
				<b>MeasureCharacterRanges</b> method.



