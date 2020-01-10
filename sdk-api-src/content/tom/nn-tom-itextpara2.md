---
UID: NN:tom.ITextPara2
title: ITextPara2 (tom.h)
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\itextpara2.htm
tech.root: Controls
ms.assetid: 31a0849f-c651-4178-b1ff-a4333bcde5d9
ms.date: 12/05/2018
ms.keywords: ITextPara2, ITextPara2 interface [Windows Controls], ITextPara2 interface [Windows Controls],described, controls.itextpara2, tom/ITextPara2
f1_keywords:
- tom/ITextPara2
dev_langs:
- c++
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Msftedit.dll
api_name:
- ITextPara2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextPara2 interface


## -description


Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> and <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>.

The <b>ITextPara2</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>, providing the equivalent of the Microsoft Word format-paragraph dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextPara2</b> interface inherits from <b>ITextPara</b>. <b>ITextPara2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextPara2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-getborders">GetBorders</a>
</td>
<td align="left" width="63%">
Gets the borders collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-getduplicate2">GetDuplicate2</a>
</td>
<td align="left" width="63%">
Gets a duplicate of this text paragraph format object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-geteffects">GetEffects</a>
</td>
<td align="left" width="63%">
Gets the paragraph format effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-getfontalignment">GetFontAlignment</a>
</td>
<td align="left" width="63%">
Gets the paragraph font alignment state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-gethangingpunctuation">GetHangingPunctuation</a>
</td>
<td align="left" width="63%">
Gets whether to hang
 punctuation symbols on the right margin when the paragraph is justified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-getsnaptogrid">GetSnapToGrid</a>
</td>
<td align="left" width="63%">
Gets whether paragraph lines snap to a vertical grid that could be defined for the whole document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-gettrimpunctuationatstart">GetTrimPunctuationAtStart</a>
</td>
<td align="left" width="63%">
Gets whether to trim the leading space of a punctuation symbol at the start of a line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-isequal2">IsEqual2</a>
</td>
<td align="left" width="63%">
Determines whether this text paragraph object has the same properties as the specified text paragraph object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-setduplicate2">SetDuplicate2</a>
</td>
<td align="left" width="63%">
Sets the properties of this object by copying the properties of another text paragraph object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-seteffects">SetEffects</a>
</td>
<td align="left" width="63%">
Sets the paragraph format effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-setfontalignment">SetFontAlignment</a>
</td>
<td align="left" width="63%">
Sets the paragraph font alignment for CJK text.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-sethangingpunctuation">SetHangingPunctuation</a>
</td>
<td align="left" width="63%">
Sets whether to hang
 punctuation symbols on the right margin when the paragraph is justified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-setsnaptogrid">SetSnapToGrid</a>
</td>
<td align="left" width="63%">
Sets whether paragraph lines snap to a vertical grid that could be defined for the whole document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara2-settrimpunctuationatstart">SetTrimPunctuationAtStart</a>
</td>
<td align="left" width="63%">
Sets whether to trim the leading space of a punctuation symbol at the start of a line.

</td>
</tr>
</table> 

