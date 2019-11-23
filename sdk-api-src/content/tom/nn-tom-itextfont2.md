---
UID: NN:tom.ITextFont2
title: ITextFont2 (tom.h)

description: In the Text Object Model (TOM), applications access text-range attributes by using a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\itextfont2.htm
tech.root: Controls
ms.assetid: d2d43bfd-7cdf-458a-822d-e3965bfe2284

ms.date: 12/05/2018
ms.keywords: ITextFont2, ITextFont2 interface [Windows Controls], ITextFont2 interface [Windows Controls],described, controls.itextfont2, tom/ITextFont2
ms.topic: interface
f1_keywords: 
 - "tom/ITextFont2"
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
 - ITextFont2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextFont2 interface


## -description


In the Text Object Model (TOM), applications access text-range attributes by using a pair of dual interfaces, <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> and <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>.

The <b>ITextFont2</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>, providing the programming equivalent of the Microsoft Word format-font dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextFont2</b> interface inherits from <b>ITextFont</b>. <b>ITextFont2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextFont2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getautoligatures">GetAutoLigatures</a>
</td>
<td align="left" width="63%">
Gets whether support for automatic ligatures is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getautospacealpha">GetAutospaceAlpha</a>
</td>
<td align="left" width="63%">
Gets the East Asian "autospace alphabetics" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getautospacenumeric">GetAutospaceNumeric</a>
</td>
<td align="left" width="63%">
Gets the East Asian "autospace numeric" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getautospaceparens">GetAutospaceParens</a>
</td>
<td align="left" width="63%">
Gets the East Asian "autospace parentheses" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getcharrep">GetCharRep</a>
</td>
<td align="left" width="63%">
Gets the character repertoire (writing system).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getcompressionmode">GetCompressionMode</a>
</td>
<td align="left" width="63%">
Gets the East Asian compression mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getcookie">GetCookie</a>
</td>
<td align="left" width="63%">
Gets the client cookie.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the count of extra properties in this character formatting collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getdoublestrike">GetDoubleStrike</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed with double horizontal lines through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getduplicate2">GetDuplicate2</a>
</td>
<td align="left" width="63%">
Gets a duplicate of this character format object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-geteffects">GetEffects</a>
</td>
<td align="left" width="63%">
Gets the character format effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-geteffects2">GetEffects2</a>
</td>
<td align="left" width="63%">
Gets the additional character format effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getlinktype">GetLinkType</a>
</td>
<td align="left" width="63%">
Gets the link type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getmathzone">GetMathZone</a>
</td>
<td align="left" width="63%">
Gets whether a math zone is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getmodwidthpairs">GetModWidthPairs</a>
</td>
<td align="left" width="63%">
Gets whether "decrease widths on pairs" is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getmodwidthspace">GetModWidthSpace</a>
</td>
<td align="left" width="63%">
Gets whether "increase width of whitespace" is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getoldnumbers">GetOldNumbers</a>
</td>
<td align="left" width="63%">
Gets whether old-style numbers are active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getoverlapping">GetOverlapping</a>
</td>
<td align="left" width="63%">
Gets whether overlapping text is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getpositionsubsuper">GetPositionSubSuper</a>
</td>
<td align="left" width="63%">
Gets the subscript or superscript position relative to the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getpropertyinfo">GetPropertyInfo</a>
</td>
<td align="left" width="63%">
Gets the property type and value of the specified extra propety.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getscaling">GetScaling</a>
</td>
<td align="left" width="63%">
Gets the font horizontal scaling percentage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getspaceextension">GetSpaceExtension</a>
</td>
<td align="left" width="63%">
Gets the East Asian space extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-getunderlinepositionmode">GetUnderlinePositionMode</a>
</td>
<td align="left" width="63%">
Gets the underline position mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-isequal2">IsEqual2</a>
</td>
<td align="left" width="63%">
Determines whether this text font object has the same properties as the specified text font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setautoligatures">SetAutoLigatures</a>
</td>
<td align="left" width="63%">
Sets whether support for automatic ligatures is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setautospacealpha">SetAutospaceAlpha</a>
</td>
<td align="left" width="63%">
Sets the East Asian "autospace alpha" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setautospacenumeric">SetAutospaceNumeric</a>
</td>
<td align="left" width="63%">
Sets the East Asian "autospace numeric" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setautospaceparens">SetAutospaceParens</a>
</td>
<td align="left" width="63%">
Sets the East Asian "autospace parentheses" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setcharrep">SetCharRep</a>
</td>
<td align="left" width="63%">
Sets the character repertoire (writing system).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setcompressionmode">SetCompressionMode</a>
</td>
<td align="left" width="63%">
Sets the East Asian compression mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setcookie">SetCookie</a>
</td>
<td align="left" width="63%">
Sets the client cookie.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setdoublestrike">SetDoubleStrike</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed with double horizontal lines through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setduplicate2">SetDuplicate2</a>
</td>
<td align="left" width="63%">
Sets the properties of this object by copying the properties of another text font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-seteffects">SetEffects</a>
</td>
<td align="left" width="63%">
Sets the character format effects. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-seteffects2">SetEffects2</a>
</td>
<td align="left" width="63%">
Sets the additional character format effects. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setmathzone">SetMathZone</a>
</td>
<td align="left" width="63%">
Sets whether a math zone is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setmodwidthpairs">SetModWidthPairs</a>
</td>
<td align="left" width="63%">
Sets whether "decrease widths on pairs" is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setmodwidthspace">SetModWidthSpace</a>
</td>
<td align="left" width="63%">
Sets whether "increase width of whitespace" is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setoldnumbers">SetOldNumbers</a>
</td>
<td align="left" width="63%">
Sets whether old-style numbers are active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setoverlapping">SetOverlapping</a>
</td>
<td align="left" width="63%">
Sets whether overlapping text is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setpositionsubsuper">SetPositionSubSuper</a>
</td>
<td align="left" width="63%">
Sets the position of a subscript or superscript relative to the baseline, as a percentage of the font height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setscaling">SetScaling</a>
</td>
<td align="left" width="63%">
Sets the font horizontal scaling percentage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setspaceextension">SetSpaceExtension</a>
</td>
<td align="left" width="63%">
Sets the East Asian space extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont2-setunderlinepositionmode">SetUnderlinePositionMode</a>
</td>
<td align="left" width="63%">
Sets the underline position mode.

</td>
</tr>
</table> 

