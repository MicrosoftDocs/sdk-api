---
UID: NN:tom.ITextFont
title: ITextFont
author: windows-sdk-content
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\ITextFont.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextFont, ITextFont interface [Windows Controls], ITextFont interface [Windows Controls],described, _win32_ITextFont, _win32_ITextFont_cpp, controls.ITextFont, controls._win32_ITextFont, tom/ITextFont
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextFont interface


## -description


Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <b>ITextFont</b> and <a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextFont</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextFont</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb787855(v=VS.85).aspx">CanChange</a>
</td>
<td align="left" width="63%">
Determines whether the font can be changed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773929(v=VS.85).aspx">GetAllCaps</a>
</td>
<td align="left" width="63%">
Gets whether the characters are all uppercase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773931(v=VS.85).aspx">GetAnimation</a>
</td>
<td align="left" width="63%">
Gets the animation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773933(v=VS.85).aspx">GetBackColor</a>
</td>
<td align="left" width="63%">
Gets the text background (highlight) color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773935(v=VS.85).aspx">GetBold</a>
</td>
<td align="left" width="63%">
Gets whether the characters are bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787857(v=VS.85).aspx">GetDuplicate</a>
</td>
<td align="left" width="63%">
Gets a duplicate of this text font object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773945(v=VS.85).aspx">GetEmboss</a>
</td>
<td align="left" width="63%">
Gets whether characters are embossed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773949(v=VS.85).aspx">GetEngrave</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as imprinted characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773956(v=VS.85).aspx">GetForeColor</a>
</td>
<td align="left" width="63%">
Gets the foreground, or text, color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773960(v=VS.85).aspx">GetHidden</a>
</td>
<td align="left" width="63%">
Gets whether characters are hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773966(v=VS.85).aspx">GetItalic</a>
</td>
<td align="left" width="63%">
Gets whether characters are in italics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773973(v=VS.85).aspx">GetKerning</a>
</td>
<td align="left" width="63%">
Gets the minimum font size at which kerning occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773975(v=VS.85).aspx">GetLanguageID</a>
</td>
<td align="left" width="63%">
Gets the  language ID or LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787859(v=VS.85).aspx">GetName</a>
</td>
<td align="left" width="63%">
Gets the font name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb773995(v=VS.85).aspx">GetOutline</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as outlined characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774005(v=VS.85).aspx">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the amount that characters are  offset vertically relative to the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774007(v=VS.85).aspx">GetProtected</a>
</td>
<td align="left" width="63%">
Gets whether characters are protected against attempts to modify them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774015(v=VS.85).aspx">GetShadow</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as shadowed characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774017(v=VS.85).aspx">GetSize</a>
</td>
<td align="left" width="63%">
Gets the font size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774019(v=VS.85).aspx">GetSmallCaps</a>
</td>
<td align="left" width="63%">
Gets whether characters are in small capital letters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774025(v=VS.85).aspx">GetSpacing</a>
</td>
<td align="left" width="63%">
Gets the amount of horizontal spacing between characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774031(v=VS.85).aspx">GetStrikeThrough</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed with a horizontal line through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787861(v=VS.85).aspx">GetStyle</a>
</td>
<td align="left" width="63%">
Gets the character style handle of the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774032(v=VS.85).aspx">GetSubscript</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as subscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774033(v=VS.85).aspx">GetSuperscript</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as superscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774038(v=VS.85).aspx">GetUnderline</a>
</td>
<td align="left" width="63%">
Gets the

			type of underlining for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774040(v=VS.85).aspx">GetWeight</a>
</td>
<td align="left" width="63%">
Gets the font weight for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787863(v=VS.85).aspx">IsEqual</a>
</td>
<td align="left" width="63%">
Determines whether this text font object has the same properties as the specified text font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787865(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
Resets the character formatting to the specified values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774125(v=VS.85).aspx">SetAllCaps</a>
</td>
<td align="left" width="63%">
Sets whether the characters are all uppercase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774127(v=VS.85).aspx">SetAnimation</a>
</td>
<td align="left" width="63%">
Sets the animation type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774129(v=VS.85).aspx">SetBackColor</a>
</td>
<td align="left" width="63%">
Sets the background color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774131(v=VS.85).aspx">SetBold</a>
</td>
<td align="left" width="63%">
Sets whether characters are bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787867(v=VS.85).aspx">SetDuplicate</a>
</td>
<td align="left" width="63%">
Sets the character formatting by copying another text font object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774137(v=VS.85).aspx">SetEmboss</a>
</td>
<td align="left" width="63%">
Sets whether characters are embossed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774141(v=VS.85).aspx">SetEngrave</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as imprinted characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774147(v=VS.85).aspx">SetForeColor</a>
</td>
<td align="left" width="63%">
Sets the foreground (text) color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774151(v=VS.85).aspx">SetHidden</a>
</td>
<td align="left" width="63%">
Sets whether characters are hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774159(v=VS.85).aspx">SetItalic</a>
</td>
<td align="left" width="63%">
Sets whether characters are in italics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774165(v=VS.85).aspx">SetKerning</a>
</td>
<td align="left" width="63%">
Sets the minimum font size at which kerning occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb774167(v=VS.85).aspx">SetLanguageID</a>
</td>
<td align="left" width="63%">
Sets the  language ID or LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787788(v=VS.85).aspx">SetName</a>
</td>
<td align="left" width="63%">
Sets the font name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787793(v=VS.85).aspx">SetOutline</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as outlined characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787801(v=VS.85).aspx">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the amount that characters are  offset vertically relative to the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787803(v=VS.85).aspx">SetProtected</a>
</td>
<td align="left" width="63%">
Sets whether characters are protected against attempts to modify them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787811(v=VS.85).aspx">SetShadow</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as shadowed characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787813(v=VS.85).aspx">SetSize</a>
</td>
<td align="left" width="63%">
Sets the font size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787815(v=VS.85).aspx">SetSmallCaps</a>
</td>
<td align="left" width="63%">
Sets whether characters are in small capital letters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787822(v=VS.85).aspx">SetSpacing</a>
</td>
<td align="left" width="63%">
Sets the amount of horizontal spacing between characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787826(v=VS.85).aspx">SetStrikeThrough</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed with a horizontal line through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787869(v=VS.85).aspx">SetStyle</a>
</td>
<td align="left" width="63%">
Sets the character style handle of the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787828(v=VS.85).aspx">SetSubscript</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as subscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787830(v=VS.85).aspx">SetSuperscript</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as superscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787832(v=VS.85).aspx">SetUnderline</a>
</td>
<td align="left" width="63%">
Sets the

			type of underlining for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb787833(v=VS.85).aspx">SetWeight</a>
</td>
<td align="left" width="63%">
Sets the font weight for the characters in a range.

</td>
</tr>
</table> 


## -remarks



The <b>ITextFont</b> and <a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a> interfaces encapsulate the functionality of the Microsoft Word Format <b>Font</b> and <b>Paragraph</b> dialog boxes, respectively. Both interfaces include a duplicate (<b>Value</b>) property that can return a duplicate of the attributes in a range object or transfer a set of attributes to a range. As such, they act like programmable format painters. For example, you could transfer all attributes from range r1 to range r2 except for making r2 bold and the font size 12 points by using the following subroutine.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>Sub AttributeCopy(r1 As ITextRange, r2 As ITextRange)
    Dim tf As ITextFont
    tf = r1.Font                ' Value is the default property    
    tf.Bold = tomTrue           ' You can make some modifications
    tf.Size = 12
    tf.Animation = tomSparkleText
    r2.Font = tf                ' Apply font attributes all at once
End Sub</pre>
</td>
</tr>
</table></span></div>
See <a href="https://msdn.microsoft.com/en-us/library/Bb774145(v=VS.85).aspx">SetFont</a> for a similar example written in C++.

The <b>ITextFont</b> attribute interface represents the traditional Microsoft Visual Basic for Applications (VBA) way of setting properties and it gives the desired VBA notation.

<b>ITextFont</b> uses the "tomBool" type for rich-text attributes that have binary states. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb787724(v=VS.85).aspx">The tomBool Type</a>.

The rich edit control is able to accept and return all <b>ITextFont</b> properties intact, that is, without modification, both through TOM and through its Rich Text Format (RTF) converters. However, it cannot display the All Caps, Animation, Embossed, Imprint, Shadow, Small Caps, Hidden, Kerning, Outline, and Style font properties.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787726(v=VS.85).aspx">Using The Text Object Model</a>
 

 

