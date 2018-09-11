---
UID: NN:tom.ITextPara2
title: ITextPara2
author: windows-sdk-content
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\itextpara2.htm
tech.root: controls
ms.assetid: 31a0849f-c651-4178-b1ff-a4333bcde5d9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextPara2, ITextPara2 interface [Windows Controls], ITextPara2 interface [Windows Controls],described, controls.itextpara2, tom/ITextPara2
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextPara2 interface


## -description


Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <a href="https://msdn.microsoft.com/en-us/library/Bb774054(v=VS.85).aspx">ITextFont</a> and <a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a>.

The <b>ITextPara2</b> interface extends <a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a>, providing the equivalent of the Microsoft Word format-paragraph dialog.


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
<a href="https://msdn.microsoft.com/c2a681f6-a8d6-49ad-9ccc-362050b2e8ad">GetBorders</a>
</td>
<td align="left" width="63%">
Gets the borders collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b7855ca-1e69-48c8-b186-99b191a7ee29">GetDuplicate2</a>
</td>
<td align="left" width="63%">
Gets a duplicate of this text paragraph format object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f672cc9-e8f3-416a-8f41-9b71ca1858a1">GetEffects</a>
</td>
<td align="left" width="63%">
Gets the paragraph format effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1064c033-2ae0-46ec-a670-603edd673e87">GetFontAlignment</a>
</td>
<td align="left" width="63%">
Gets the paragraph font alignment state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/781b7c53-e9a1-4c4a-84d7-ea70efc173d1">GetHangingPunctuation</a>
</td>
<td align="left" width="63%">
Gets whether to hang
 punctuation symbols on the right margin when the paragraph is justified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/628ec2d7-2553-4a76-a5e6-c3a5bef3f8d6">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee5fd1d8-cd2d-4674-bb0f-6021a3115aac">GetSnapToGrid</a>
</td>
<td align="left" width="63%">
Gets whether paragraph lines snap to a vertical grid that could be defined for the whole document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/965df0ef-b8ff-4d0e-8124-c811e74e0208">GetTrimPunctuationAtStart</a>
</td>
<td align="left" width="63%">
Gets whether to trim the leading space of a punctuation symbol at the start of a line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7817b1bd-6ade-4145-90ff-54561a639dc9">IsEqual2</a>
</td>
<td align="left" width="63%">
Determines whether this text paragraph object has the same properties as the specified text paragraph object. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/403fd23b-5d66-4e30-b1aa-eec9e4676318">SetDuplicate2</a>
</td>
<td align="left" width="63%">
Sets the properties of this object by copying the properties of another text paragraph object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7184de4-b416-4f28-8f10-c89ffcccf1a1">SetEffects</a>
</td>
<td align="left" width="63%">
Sets the paragraph format effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ed1f7f2-9523-4dda-bac0-c1eb3d217102">SetFontAlignment</a>
</td>
<td align="left" width="63%">
Sets the paragraph font alignment for CJK text.  


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c70f76f-7a4a-49b3-bc16-8e90ad7ee041">SetHangingPunctuation</a>
</td>
<td align="left" width="63%">
Sets whether to hang
 punctuation symbols on the right margin when the paragraph is justified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a95c055-5118-4c2a-8f63-3a2a3114451e">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93116780-03e2-406b-8923-b9f02f53892d">SetSnapToGrid</a>
</td>
<td align="left" width="63%">
Sets whether paragraph lines snap to a vertical grid that could be defined for the whole document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f08f67ca-5767-4986-8af1-b3a11a1065aa">SetTrimPunctuationAtStart</a>
</td>
<td align="left" width="63%">
Sets whether to trim the leading space of a punctuation symbol at the start of a line.

</td>
</tr>
</table> 

