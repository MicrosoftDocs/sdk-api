---
UID: NN:tom.ITextRange2
title: ITextRange2
author: windows-sdk-content
description: The ITextRange2 interface is derived from ITextRange, and its objects are powerful editing and data-binding tools that enable a program to select text in a story and then examine or change that text.
old-location: controls\itextrange2.htm
old-project: Controls
ms.assetid: 905f0967-8b99-45ed-a1cc-19d49e919a65
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ITextRange2, ITextRange2 interface [Windows Controls], ITextRange2 interface [Windows Controls],described, controls.itextrange2, tom/ITextRange2
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
 - ITextRange2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange2 interface


## -description


The <b>ITextRange2</b> interface is derived from <a href="https://msdn.microsoft.com/e19678cb-f951-458c-bf96-de4b123fd63a">ITextRange</a>, and its objects are powerful editing and data-binding tools that enable a program to select text in a story and then examine or change that text.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextRange2</b> interface inherits from <b>ITextSelection</b>. <b>ITextRange2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextRange2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffd1f166-a37c-4b39-9878-a4008260f675">AddSubrange</a>
</td>
<td align="left" width="63%">
Adds a subrange to this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6382f09-126e-4107-a4b9-288777549181">BuildUpMath</a>
</td>
<td align="left" width="63%">
Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad75725d-ad92-45fc-a0a9-3227bfb99284">DeleteSubrange</a>
</td>
<td align="left" width="63%">
Deletes a subrange from a range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4935d322-016a-4c08-858e-42009a9f59f1">Find</a>
</td>
<td align="left" width="63%">
Searchs for math inline functions in text as specified by a source range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6f06062-3c8f-40c0-9b5d-6c22a647bfbc">GetCch</a>
</td>
<td align="left" width="63%">
Gets the count of characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caaee637-d80a-44c6-9d9b-ed16a980afd9">GetCells</a>
</td>
<td align="left" width="63%">
Gets a cells object with the parameters of cells in the currently selected table row or column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ece8ca0-fd05-481c-9ce2-b2b7a3df354e">GetChar2</a>
</td>
<td align="left" width="63%">
Gets the character at the specified offset from the end of this range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8e2c985-9799-42c9-b23d-43c16bae5c69">GetColumn</a>
</td>
<td align="left" width="63%">
Gets the column properties for the currently selected column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the count of subranges, including the  active subrange in the current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c653c002-6708-4813-83ae-1ea578bdcee2">GetDropCap</a>
</td>
<td align="left" width="63%">
Gets the drop-cap parameters of the paragraph that contains this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dce56b6-463a-49d4-8e4b-397e2841544c">GetDuplicate2</a>
</td>
<td align="left" width="63%">
Gets a duplicate of a range object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24ef7fb3-4cf4-46ed-9273-6f91c77f7641">GetFont2</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a> object with the character attributes of the current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9fe5d82d-b13e-4b94-beb6-15691d4c5176">GetFormattedText2</a>
</td>
<td align="left" width="63%">
Gets an <b>ITextRange2</b> object with the current range's formatted text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a57ab2c2-1871-413a-bccd-47f5c1dd4570">GetGravity</a>
</td>
<td align="left" width="63%">
Gets the gravity of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ed4a595-c3e8-4bfa-805f-4c5dfd5e3a56">GetInlineObject</a>
</td>
<td align="left" width="63%">
Gets the properties of the inline object at the range active end.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00bae237-5853-430e-8313-563da0cf0fde">GetMathFunctionType</a>
</td>
<td align="left" width="63%">
Retrieves the math function type associated with the specified math function name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b20ebe85-f2a6-4a19-8b25-f1f16ebf5627">GetPara2</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a> object with the paragraph attributes of a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5e636b9-d02e-46ac-b224-7d1019da44eb">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of a property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14f0faab-ff37-4f86-a4ba-b6c207d7ddf0">GetRect</a>
</td>
<td align="left" width="63%">
Retrieves a rectangle of the specified type for the current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f15605a-8f81-4fc4-ad12-5300ecd03c16">GetRow</a>
</td>
<td align="left" width="63%">
Gets the row properties in the currently selected row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6a59ffd-0271-4c2a-9a9e-f31287b47ce9">GetStartPara</a>
</td>
<td align="left" width="63%">
Gets the character position of the start of the paragraph that contains the range's start character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64b031cf-9d32-4e36-8e13-f32a53f00abf">GetSubrange</a>
</td>
<td align="left" width="63%">
Retrieves a subrange in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ade77edf-6a9e-4c8d-a522-3158c802b6dd">GetTable</a>
</td>
<td align="left" width="63%">
Gets the table properties in the currently selected table. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77f39808-b39d-45bb-ba03-3a27d503fe0e">GetText2</a>
</td>
<td align="left" width="63%">
Gets the text in this range according to the specified conversion flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/mt432962">GetURL</a>
</td>
<td align="left" width="63%">
Returns the URL text associated with a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/024f9f32-2362-4f1c-b8db-9b4fb1ee157c">HexToUnicode</a>
</td>
<td align="left" width="63%">
Converts and replaces the hexadecimal number at the end of this range to a Unicode character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CBC71EDC-CBE3-4C44-84C8-6AE6DEBC8D0C">InsertImage</a>
</td>
<td align="left" width="63%">
Inserts an image into this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f62cc778-8f06-43d1-985b-d233b02d3255">InsertTable</a>
</td>
<td align="left" width="63%">
Inserts a table in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9906547b-e31c-48a6-961e-0b7f5c0c0506">Linearize</a>
</td>
<td align="left" width="63%">
Translates the built-up math, ruby, and other inline objects in this range to linearized form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a635edd3-dcb9-4f1f-bf6e-774ce3f0c505">SetActiveSubrange</a>
</td>
<td align="left" width="63%">
Makes the specified  subrange the active subrange of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/189c1a69-44eb-4de0-8ffc-9a026d9e6f16">SetDropCap</a>
</td>
<td align="left" width="63%">
Sets the drop-cap parameters for the paragraph that contains the current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff3c2bf3-efb8-454e-b0e2-e65afeb1a091">SetFont2</a>
</td>
<td align="left" width="63%">
Sets the character formatting attributes of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/151be9ee-da5d-4e50-a12e-0473cf1c7d91">SetFormattedText2</a>
</td>
<td align="left" width="63%">
Sets the text of this range to the formatted text of the specified range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10214543-36da-46e3-b926-0ba088f84a7b">SetGravity</a>
</td>
<td align="left" width="63%">
Sets the gravity of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56876a42-a972-4a19-a8f7-a5e37c0d77f0">SetInlineObject</a>
</td>
<td align="left" width="63%">
Sets or inserts the properties of an inline object for a degenerate range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ffd25a04-27a8-47c0-95a4-d66291971819">SetPara2</a>
</td>
<td align="left" width="63%">
Sets the paragraph format attributes of a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d6c2f44-40e9-48b2-850d-d74d7a50fa0d">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd7a8a16-6cb5-40ee-8f5f-e51e68785d93">SetText2</a>
</td>
<td align="left" width="63%">
Sets the text of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8e62056-5177-4c88-99d8-32ca30bc71e5">SetURL</a>
</td>
<td align="left" width="63%">
Sets the text in this range to that of the specified URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/538f7db4-0739-421c-9d51-8144b2d52334">UnicodeToHex</a>
</td>
<td align="left" width="63%">
Converts the Unicode character(s) preceding the start position of this text range to a hexadecimal number, and selects it.

</td>
</tr>
</table> 

