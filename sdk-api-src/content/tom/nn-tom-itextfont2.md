---
UID: NN:tom.ITextFont2
title: ITextFont2
author: windows-sdk-content
description: In the Text Object Model (TOM), applications access text-range attributes by using a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\itextfont2.htm
old-project: controls
ms.assetid: d2d43bfd-7cdf-458a-822d-e3965bfe2284
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextFont2, ITextFont2 interface [Windows Controls], ITextFont2 interface [Windows Controls],described, controls.itextfont2, tom/ITextFont2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2 interface


## -description


In the Text Object Model (TOM), applications access text-range attributes by using a pair of dual interfaces, <a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a> and <a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>.

The <b>ITextFont2</b> interface extends <a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a>, providing the programming equivalent of the Microsoft Word format-font dialog.


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
<a href="https://msdn.microsoft.com/f8209c34-139c-45e6-b110-f6d3d76f5575">GetAutoLigatures</a>
</td>
<td align="left" width="63%">
Gets whether support for automatic ligatures is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f2070e9-2909-4642-ade2-54ef9af9cfc8">GetAutospaceAlpha</a>
</td>
<td align="left" width="63%">
Gets the East Asian "autospace alphabetics" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/448a461b-779a-457e-8206-2055a73c9b45">GetAutospaceNumeric</a>
</td>
<td align="left" width="63%">
Gets the East Asian "autospace numeric" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fce60349-cded-4cab-b2e5-4fad02d11195">GetAutospaceParens</a>
</td>
<td align="left" width="63%">
Gets the East Asian "autospace parentheses" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/250b9fe9-8f63-4f6f-9b14-d6fdac3580b0">GetCharRep</a>
</td>
<td align="left" width="63%">
Gets the character repertoire (writing system).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3fefba0c-54a3-4013-8922-ba556ef785a6">GetCompressionMode</a>
</td>
<td align="left" width="63%">
Gets the East Asian compression mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3e36338-8c88-4aaf-bbd0-c07a2228cb23">GetCookie</a>
</td>
<td align="left" width="63%">
Gets the client cookie.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the count of extra properties in this character formatting collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9e599c29-4b47-4043-b9c7-75a736ca64fa">GetDoubleStrike</a>
</td>
<td align="left" width="63%">
Gets whether characters are displayed with double horizontal lines through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc6b979b-f837-4945-a35d-c5585d703bd1">GetDuplicate2</a>
</td>
<td align="left" width="63%">
Gets a duplicate of this character format object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a182df7e-2024-48fc-9767-7110ffff0b4c">GetEffects</a>
</td>
<td align="left" width="63%">
Gets the character format effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b28c995-33dd-4f5b-ac89-eec367e0a4d5">GetEffects2</a>
</td>
<td align="left" width="63%">
Gets the additional character format effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5405b2ce-52c9-4630-a091-3221820a4e0b">GetLinkType</a>
</td>
<td align="left" width="63%">
Gets the link type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4da4d6d1-16e0-4891-9a60-c1330345e45a">GetMathZone</a>
</td>
<td align="left" width="63%">
Gets whether a math zone is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fcbc781-42da-46aa-b231-3a8246eccd36">GetModWidthPairs</a>
</td>
<td align="left" width="63%">
Gets whether "decrease widths on pairs" is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ce6250f-94e6-4a20-89cd-f3e9a83a9408">GetModWidthSpace</a>
</td>
<td align="left" width="63%">
Gets whether "increase width of whitespace" is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e800840-5ca2-4fbf-94c2-d51aa73bf188">GetOldNumbers</a>
</td>
<td align="left" width="63%">
Gets whether old-style numbers are active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26937777-a44b-4196-aa6b-f35787f934a9">GetOverlapping</a>
</td>
<td align="left" width="63%">
Gets whether overlapping text is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7e53a94-b218-47d1-b366-3bbf7779516e">GetPositionSubSuper</a>
</td>
<td align="left" width="63%">
Gets the subscript or superscript position relative to the baseline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1894788a-5612-43a2-af77-131d02fe1261">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bea8f6da-f781-430f-b1cd-c28e11cc61bb">GetPropertyInfo</a>
</td>
<td align="left" width="63%">
Gets the property type and value of the specified extra propety.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4508d079-6f75-4842-a7e6-c2b9a99c826c">GetScaling</a>
</td>
<td align="left" width="63%">
Gets the font horizontal scaling percentage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36623ab5-3584-49c7-aeba-c34cfc8053e6">GetSpaceExtension</a>
</td>
<td align="left" width="63%">
Gets the East Asian space extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd7a45be-05b0-4a43-90c8-0fd8393794c0">GetUnderlinePositionMode</a>
</td>
<td align="left" width="63%">
Gets the underline position mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c423bbdb-a108-4f29-8dc4-3dd35849f39a">IsEqual2</a>
</td>
<td align="left" width="63%">
Determines whether this text font object has the same properties as the specified text font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f40fecfe-3c3b-46f0-9edf-ba48236e50e7">SetAutoLigatures</a>
</td>
<td align="left" width="63%">
Sets whether support for automatic ligatures is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a01677d-74c6-437b-8ee9-350c891c6c3f">SetAutospaceAlpha</a>
</td>
<td align="left" width="63%">
Sets the East Asian "autospace alpha" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fd911c2-a765-4bbc-a14c-15665d5a4a16">SetAutospaceNumeric</a>
</td>
<td align="left" width="63%">
Sets the East Asian "autospace numeric" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a9290e0-221e-454a-af9c-9d1bf5d37b5e">SetAutospaceParens</a>
</td>
<td align="left" width="63%">
Sets the East Asian "autospace parentheses" state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c57b5e5-a5c7-416a-851c-fc8ef16b5a9a">SetCharRep</a>
</td>
<td align="left" width="63%">
Sets the character repertoire (writing system).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/834bb793-b4a8-40b6-b210-05d17332ddb8">SetCompressionMode</a>
</td>
<td align="left" width="63%">
Sets the East Asian compression mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1b4c7a8-ba4c-482f-8431-14d45474ccc0">SetCookie</a>
</td>
<td align="left" width="63%">
Sets the client cookie.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bed8ce93-5c3a-43ee-b9c7-c1fd42481bbd">SetDoubleStrike</a>
</td>
<td align="left" width="63%">
Sets whether characters are displayed with double horizontal lines through the center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aaaafed9-be20-40a2-beed-09703970452f">SetDuplicate2</a>
</td>
<td align="left" width="63%">
Sets the properties of this object by copying the properties of another text font object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/edfc882e-6f76-498f-ae3f-4978ea728d1b">SetEffects</a>
</td>
<td align="left" width="63%">
Sets the character format effects. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb4bfbe3-1e66-41ed-92e6-8d4f3877bdf0">SetEffects2</a>
</td>
<td align="left" width="63%">
Sets the additional character format effects. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e43d51a-3001-4611-8aa1-fcf8cc2655fc">SetMathZone</a>
</td>
<td align="left" width="63%">
Sets whether a math zone is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60117c84-18f9-49db-8d13-b55576874d2b">SetModWidthPairs</a>
</td>
<td align="left" width="63%">
Sets whether "decrease widths on pairs" is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df3ea127-1f47-4173-ad2c-0a7af4c8454c">SetModWidthSpace</a>
</td>
<td align="left" width="63%">
Sets whether "increase width of whitespace" is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f510781e-ede9-41dc-ae69-3b0ca52a6773">SetOldNumbers</a>
</td>
<td align="left" width="63%">
Sets whether old-style numbers are active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40addd31-5c0e-45bd-a649-c65973ae8340">SetOverlapping</a>
</td>
<td align="left" width="63%">
Sets whether overlapping text is active.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f78a91b-17a3-48ff-9ca0-1eb4f9c95be4">SetPositionSubSuper</a>
</td>
<td align="left" width="63%">
Sets the position of a subscript or superscript relative to the baseline, as a percentage of the font height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4d35fed-9bf5-431e-96c9-b1d51d51703a">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5f26c0a-a1bd-4be8-84b8-92a6d0cfafdb">SetScaling</a>
</td>
<td align="left" width="63%">
Sets the font horizontal scaling percentage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7388f414-f361-40e4-8a64-fc0643777f33">SetSpaceExtension</a>
</td>
<td align="left" width="63%">
Sets the East Asian space extension value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31dff2d0-7165-42f0-b3d0-9cb679c738c3">SetUnderlinePositionMode</a>
</td>
<td align="left" width="63%">
Sets the underline position mode.

</td>
</tr>
</table> 

