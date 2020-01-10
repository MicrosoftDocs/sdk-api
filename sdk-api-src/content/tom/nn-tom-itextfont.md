---
UID: NN:tom.ITextFont
title: ITextFont (tom.h)
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\ITextFont.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont.htm
ms.date: 12/05/2018
ms.keywords: ITextFont, ITextFont interface [Windows Controls], ITextFont interface [Windows Controls],described, _win32_ITextFont, _win32_ITextFont_cpp, controls.ITextFont, controls._win32_ITextFont, tom/ITextFont
f1_keywords:
- tom/ITextFont
dev_langs:
- c++
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- ITextFont
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextFont interface


## -description


Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <b>ITextFont</b> and <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextFont</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITextFont</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextFont</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-canchange">CanChange</a>
</td>
<td align="left" width="63%">
Determines whether the font can be changed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getallcaps">GetAllCaps</a>
</td>
<td align="left" width="63%">
Gets whether the characters are all uppercase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getanimation">GetAnimation</a>
</td>
<td align="left" width="63%">
Gets the animation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getbackcolor">GetBackColor</a>
</td>
<td align="left" width="63%">
Gets the text background (highlight) color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getbold">GetBold</a>
</td>
<td align="left" width="63%">
Gets whether the characters are bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getduplicate">GetDuplicate</a>
</td>
<td align="left" width="63%">
Gets a duplicate of this text font object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getemboss">GetEmboss</a>
</td>
<td align="left" width="63%">
Gets whether characters are embossed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getengrave">GetEngrave</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as imprinted characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getforecolor">GetForeColor</a>
</td>
<td align="left" width="63%">
Gets the foreground, or text, color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-gethidden">GetHidden</a>
</td>
<td align="left" width="63%">
Gets whether characters are hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getitalic">GetItalic</a>
</td>
<td align="left" width="63%">
Gets whether characters are in italics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getkerning">GetKerning</a>
</td>
<td align="left" width="63%">
Gets the minimum font size at which kerning occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getlanguageid">GetLanguageID</a>
</td>
<td align="left" width="63%">
Gets the  language ID or LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getname">GetName</a>
</td>
<td align="left" width="63%">
Gets the font name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getoutline">GetOutline</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as outlined characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getposition">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the amount that characters are  offset vertically relative to the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getprotected">GetProtected</a>
</td>
<td align="left" width="63%">
Gets whether characters are protected against attempts to modify them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getshadow">GetShadow</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as shadowed characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Gets the font size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getsmallcaps">GetSmallCaps</a>
</td>
<td align="left" width="63%">
Gets whether characters are in small capital letters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getspacing">GetSpacing</a>
</td>
<td align="left" width="63%">
Gets the amount of horizontal spacing between characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getstrikethrough">GetStrikeThrough</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed with a horizontal line through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getstyle">GetStyle</a>
</td>
<td align="left" width="63%">
Gets the character style handle of the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getsubscript">GetSubscript</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as subscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getsuperscript">GetSuperscript</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as superscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getunderline">GetUnderline</a>
</td>
<td align="left" width="63%">
Gets the

			type of underlining for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-getweight">GetWeight</a>
</td>
<td align="left" width="63%">
Gets the font weight for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-isequal">IsEqual</a>
</td>
<td align="left" width="63%">
Determines whether this text font object has the same properties as the specified text font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the character formatting to the specified values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setallcaps">SetAllCaps</a>
</td>
<td align="left" width="63%">
Sets whether the characters are all uppercase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setanimation">SetAnimation</a>
</td>
<td align="left" width="63%">
Sets the animation type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setbackcolor">SetBackColor</a>
</td>
<td align="left" width="63%">
Sets the background color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setbold">SetBold</a>
</td>
<td align="left" width="63%">
Sets whether characters are bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setduplicate">SetDuplicate</a>
</td>
<td align="left" width="63%">
Sets the character formatting by copying another text font object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setemboss">SetEmboss</a>
</td>
<td align="left" width="63%">
Sets whether characters are embossed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setengrave">SetEngrave</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as imprinted characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setforecolor">SetForeColor</a>
</td>
<td align="left" width="63%">
Sets the foreground (text) color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-sethidden">SetHidden</a>
</td>
<td align="left" width="63%">
Sets whether characters are hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setitalic">SetItalic</a>
</td>
<td align="left" width="63%">
Sets whether characters are in italics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setkerning">SetKerning</a>
</td>
<td align="left" width="63%">
Sets the minimum font size at which kerning occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setlanguageid">SetLanguageID</a>
</td>
<td align="left" width="63%">
Sets the  language ID or LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setname">SetName</a>
</td>
<td align="left" width="63%">
Sets the font name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setoutline">SetOutline</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as outlined characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setposition">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the amount that characters are  offset vertically relative to the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setprotected">SetProtected</a>
</td>
<td align="left" width="63%">
Sets whether characters are protected against attempts to modify them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setshadow">SetShadow</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as shadowed characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setsize">SetSize</a>
</td>
<td align="left" width="63%">
Sets the font size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setsmallcaps">SetSmallCaps</a>
</td>
<td align="left" width="63%">
Sets whether characters are in small capital letters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setspacing">SetSpacing</a>
</td>
<td align="left" width="63%">
Sets the amount of horizontal spacing between characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setstrikethrough">SetStrikeThrough</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed with a horizontal line through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setstyle">SetStyle</a>
</td>
<td align="left" width="63%">
Sets the character style handle of the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setsubscript">SetSubscript</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as subscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setsuperscript">SetSuperscript</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as superscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setunderline">SetUnderline</a>
</td>
<td align="left" width="63%">
Sets the

			type of underlining for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextfont-setweight">SetWeight</a>
</td>
<td align="left" width="63%">
Sets the font weight for the characters in a range.

</td>
</tr>
</table> 


## -remarks



The <b>ITextFont</b> and <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> interfaces encapsulate the functionality of the Microsoft Word Format <b>Font</b> and <b>Paragraph</b> dialog boxes, respectively. Both interfaces include a duplicate (<b>Value</b>) property that can return a duplicate of the attributes in a range object or transfer a set of attributes to a range. As such, they act like programmable format painters. For example, you could transfer all attributes from range r1 to range r2 except for making r2 bold and the font size 12 points by using the following subroutine.


```
Sub AttributeCopy(r1 As ITextRange, r2 As ITextRange)
    Dim tf As ITextFont
    tf = r1.Font                ' Value is the default property    
    tf.Bold = tomTrue           ' You can make some modifications
    tf.Size = 12
    tf.Animation = tomSparkleText
    r2.Font = tf                ' Apply font attributes all at once
End Sub
```


See <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange-setfont">SetFont</a> for a similar example written in C++.

The <b>ITextFont</b> attribute interface represents the traditional Microsoft Visual Basic for Applications (VBA) way of setting properties and it gives the desired VBA notation.

<b>ITextFont</b> uses the "tomBool" type for rich-text attributes that have binary states. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/about-text-object-model">The tomBool Type</a>.

The rich edit control is able to accept and return all <b>ITextFont</b> properties intact, that is, without modification, both through TOM and through its Rich Text Format (RTF) converters. However, it cannot display the All Caps, Animation, Embossed, Imprint, Shadow, Small Caps, Hidden, Kerning, Outline, and Style font properties.




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/using-the-text-object-model">Using The Text Object Model</a>
 

 

