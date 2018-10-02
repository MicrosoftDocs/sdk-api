---
UID: NN:tom.ITextFont
title: ITextFont
author: windows-sdk-content
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\ITextFont.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextfont.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITextFont, ITextFont interface [Windows Controls], ITextFont interface [Windows Controls],described, _win32_ITextFont, _win32_ITextFont_cpp, controls.ITextFont, controls._win32_ITextFont, tom/ITextFont
ms.prod: windows
ms.technology: windows-sdk
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


Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <b>ITextFont</b> and <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>.


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
<a href="https://msdn.microsoft.com/e9daaf98-80c0-4015-84a3-cb78dfa29ab2">CanChange</a>
</td>
<td align="left" width="63%">
Determines whether the font can be changed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25e5c089-55fc-4557-8a84-42ec56bcae37">GetAllCaps</a>
</td>
<td align="left" width="63%">
Gets whether the characters are all uppercase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/996f4ca0-bb7b-4a6a-84d5-3c5a9a178c09">GetAnimation</a>
</td>
<td align="left" width="63%">
Gets the animation type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5925136-b883-4036-acee-29f640e8ee56">GetBackColor</a>
</td>
<td align="left" width="63%">
Gets the text background (highlight) color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77c4371c-d73f-4867-91e9-0c1dcc9f9e65">GetBold</a>
</td>
<td align="left" width="63%">
Gets whether the characters are bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63911719-9ce2-482f-ba66-bc04eaa5d965">GetDuplicate</a>
</td>
<td align="left" width="63%">
Gets a duplicate of this text font object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eeb1d10d-c326-4052-813b-ee435b88e835">GetEmboss</a>
</td>
<td align="left" width="63%">
Gets whether characters are embossed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e4174160-7e4d-4d05-ae37-bf1396ba0102">GetEngrave</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as imprinted characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f25279b5-001b-4e46-9b46-dde5fb4114b6">GetForeColor</a>
</td>
<td align="left" width="63%">
Gets the foreground, or text, color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/083b54f6-3335-415e-b1ab-b5fcae628a15">GetHidden</a>
</td>
<td align="left" width="63%">
Gets whether characters are hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5eaf9103-f389-443a-bd7e-aebeb7fee18c">GetItalic</a>
</td>
<td align="left" width="63%">
Gets whether characters are in italics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7af7356-ada6-424c-bd8f-32c40a8c095c">GetKerning</a>
</td>
<td align="left" width="63%">
Gets the minimum font size at which kerning occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/422f94bc-44ef-44db-be8c-50fe1acc2320">GetLanguageID</a>
</td>
<td align="left" width="63%">
Gets the  language ID or LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4b5d82a-c47d-498e-97a7-d475f3c7ae91">GetName</a>
</td>
<td align="left" width="63%">
Gets the font name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da49dc25-6e84-4bce-8390-73d9dc69bb0d">GetOutline</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as outlined characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/feb68cd1-7bca-4de7-bf8f-5fa2312aff9e">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the amount that characters are  offset vertically relative to the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c0696172-e6c2-4b26-9bb3-e58d31100e5b">GetProtected</a>
</td>
<td align="left" width="63%">
Gets whether characters are protected against attempts to modify them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf572173-afa2-4c49-a62d-25fbf1d828d4">GetShadow</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as shadowed characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78b4070b-462a-4b19-8958-e2695b0ccf6a">GetSize</a>
</td>
<td align="left" width="63%">
Gets the font size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f498fb97-7165-45dd-ac19-e1ae02ad5185">GetSmallCaps</a>
</td>
<td align="left" width="63%">
Gets whether characters are in small capital letters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3392f160-4fe0-41f4-8069-c11576ddb83d">GetSpacing</a>
</td>
<td align="left" width="63%">
Gets the amount of horizontal spacing between characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/659ef990-3449-4e69-8728-b648d8ddf3a2">GetStrikeThrough</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed with a horizontal line through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ebe767e-1f64-4d12-bf11-85b6253d86ce">GetStyle</a>
</td>
<td align="left" width="63%">
Gets the character style handle of the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/048f7ccb-13b3-47b6-ac47-d337e89e3189">GetSubscript</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as subscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c800f5ee-d847-4065-8f47-4147955017b7">GetSuperscript</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed as superscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5eb1920-278f-4b23-8d27-25090ebb18a2">GetUnderline</a>
</td>
<td align="left" width="63%">
Gets the

			type of underlining for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bbbcd2d-3d40-4c87-a786-13acbf2be502">GetWeight</a>
</td>
<td align="left" width="63%">
Gets the font weight for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c567d78-a915-4b44-bf52-61e72101c08b">IsEqual</a>
</td>
<td align="left" width="63%">
Determines whether this text font object has the same properties as the specified text font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b0517bf-f27e-42ff-901d-9d6a797f0c82">Reset</a>
</td>
<td align="left" width="63%">
Resets the character formatting to the specified values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/463aee02-5d5a-472f-b10d-63a9591cbfdc">SetAllCaps</a>
</td>
<td align="left" width="63%">
Sets whether the characters are all uppercase.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3edc0c9-0f75-4b6a-a4c4-b7659bbb89cf">SetAnimation</a>
</td>
<td align="left" width="63%">
Sets the animation type. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4bf6e7e-bcfd-43d1-8808-9c876549c674">SetBackColor</a>
</td>
<td align="left" width="63%">
Sets the background color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e2bcd5a-badd-4ba4-8d8b-d054ec4ac539">SetBold</a>
</td>
<td align="left" width="63%">
Sets whether characters are bold.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb71e34a-adf9-4700-b6f0-42f8b1c30881">SetDuplicate</a>
</td>
<td align="left" width="63%">
Sets the character formatting by copying another text font object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/560f934d-94e6-40ff-ac1e-899cbedf5f9d">SetEmboss</a>
</td>
<td align="left" width="63%">
Sets whether characters are embossed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbc2b175-e0bb-4d10-87ad-b8c07cadab5c">SetEngrave</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as imprinted characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac2db646-b9f5-46fb-a9c2-e789bec8a4de">SetForeColor</a>
</td>
<td align="left" width="63%">
Sets the foreground (text) color.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d655c8b-3686-4c32-84aa-77e4b09e2965">SetHidden</a>
</td>
<td align="left" width="63%">
Sets whether characters are hidden.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14b7868e-414c-489b-a8fa-6f3afaa24337">SetItalic</a>
</td>
<td align="left" width="63%">
Sets whether characters are in italics.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/debac049-f6d8-4094-acf6-aaf8f9867671">SetKerning</a>
</td>
<td align="left" width="63%">
Sets the minimum font size at which kerning occurs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c45a2f7-d2c3-4a7a-b5bb-b06ba59d5adf">SetLanguageID</a>
</td>
<td align="left" width="63%">
Sets the  language ID or LCID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8190e20b-2371-46fb-b113-0e9baedf294c">SetName</a>
</td>
<td align="left" width="63%">
Sets the font name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e080903-0a3d-4686-83ab-b50864354347">SetOutline</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as outlined characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e55684d8-d75d-46bf-a8bc-81bc9c46a1e0">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the amount that characters are  offset vertically relative to the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d564e889-d8ea-4ff3-b765-b7c204287e63">SetProtected</a>
</td>
<td align="left" width="63%">
Sets whether characters are protected against attempts to modify them.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2d07b7c-7528-40c0-9d07-7e384fae0d0c">SetShadow</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as shadowed characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/268900f8-d7a7-41e3-adb1-32bf2af5d5db">SetSize</a>
</td>
<td align="left" width="63%">
Sets the font size.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6ff7f24-1fe2-4bf8-b92e-2bc2673402e0">SetSmallCaps</a>
</td>
<td align="left" width="63%">
Sets whether characters are in small capital letters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a1ba236-3696-4a68-80bf-30e6a9b53437">SetSpacing</a>
</td>
<td align="left" width="63%">
Sets the amount of horizontal spacing between characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f0721b3-b28e-4df8-b2a8-98ccbfd6e93d">SetStrikeThrough</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed with a horizontal line through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2b39405-dd54-4873-a516-e4b7a865b465">SetStyle</a>
</td>
<td align="left" width="63%">
Sets the character style handle of the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/077f8962-4ce2-4dc0-9222-a93dbb2ed83b">SetSubscript</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as subscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51588d20-b664-4380-aa51-625bbeb214b4">SetSuperscript</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed as superscript.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a58baee4-6264-49ed-bd2c-15ce22cdba94">SetUnderline</a>
</td>
<td align="left" width="63%">
Sets the

			type of underlining for the characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12ca699b-8e9c-4071-aac9-783480541526">SetWeight</a>
</td>
<td align="left" width="63%">
Sets the font weight for the characters in a range.

</td>
</tr>
</table> 


## -remarks



The <b>ITextFont</b> and <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a> interfaces encapsulate the functionality of the Microsoft Word Format <b>Font</b> and <b>Paragraph</b> dialog boxes, respectively. Both interfaces include a duplicate (<b>Value</b>) property that can return a duplicate of the attributes in a range object or transfer a set of attributes to a range. As such, they act like programmable format painters. For example, you could transfer all attributes from range r1 to range r2 except for making r2 bold and the font size 12 points by using the following subroutine.

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
See <a href="https://msdn.microsoft.com/15630fec-83b2-4169-b141-8ce253dd25fe">SetFont</a> for a similar example written in C++.

The <b>ITextFont</b> attribute interface represents the traditional Microsoft Visual Basic for Applications (VBA) way of setting properties and it gives the desired VBA notation.

<b>ITextFont</b> uses the "tomBool" type for rich-text attributes that have binary states. For more information, see <a href="About_Text_Object_Model.htm">The tomBool Type</a>.

The rich edit control is able to accept and return all <b>ITextFont</b> properties intact, that is, without modification, both through TOM and through its Rich Text Format (RTF) converters. However, it cannot display the All Caps, Animation, Embossed, Imprint, Shadow, Small Caps, Hidden, Kerning, Outline, and Style font properties.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>



<a href="https://msdn.microsoft.com/5d9ab4fa-e9a0-4031-bbaa-311aff912eba">Using The Text Object Model</a>
 

 

