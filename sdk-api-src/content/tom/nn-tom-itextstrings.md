---
UID: NN:tom.ITextStrings
title: ITextStrings
author: windows-driver-content
description: The ITextStrings interface represents a collection of rich-text strings that are useful for manipulating rich text.
old-location: controls\itextstrings.htm
old-project: Controls
ms.assetid: c878d0db-ac13-4ac9-8601-d1c1ba76cd85
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITextStrings, ITextStrings interface [Windows Controls], ITextStrings interface [Windows Controls], described, controls.itextstrings, tom/ITextStrings
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextStrings
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStrings interface


## -description


The <b>ITextStrings</b> interface represents a collection of rich-text strings that are useful for manipulating rich text. In particular, you can use the collection to convert linearly formatted math expressions into built-up form and vice versa. You can also use the collection to collect the concatenation of a set of rich-text strings, or to manipulate a string without changing a primary story. The collection is efficiently implemented by concatenating the strings in a scratch story and maintaining an array of the string counts that identify the strings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStrings</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITextStrings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStrings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds a string to the end of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e280008b-b41e-43e3-9f16-6fe1f88e10ea">Append</a>
</td>
<td align="left" width="63%">
Appends a string to the string at the specified index in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9691d04f-5c87-42a3-81f2-efb051e2ed30">Cat2</a>
</td>
<td align="left" width="63%">
Concatenates two strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50cc7bbb-51c2-40fd-9ef9-3b06ee9aca1d">CatTop2</a>
</td>
<td align="left" width="63%">
Inserts text between the top two strings in a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2dd6312a-77ab-4538-a51b-7de49a5457ff">DeleteRange</a>
</td>
<td align="left" width="63%">
Deletes the contents of a given range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f22bb343-4fcc-4473-84cc-807011b5a7b0">EncodeFunction</a>
</td>
<td align="left" width="63%">
Encodes an object, given a set of argument strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73b88019-f74b-4345-95f3-9f924c999b8a">GetCch</a>
</td>
<td align="left" width="63%">
Gets the count of characters for a selected string index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of strings in a string collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc269f41-f65c-4335-ac5c-5c57187f20aa">InsertNullStr</a>
</td>
<td align="left" width="63%">
Inserts a <b>NULL</b> string in the collection at a selected string index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object for a selected index in a string collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db0eff33-f20a-481e-bcae-8a72674ab906">MoveBoundary</a>
</td>
<td align="left" width="63%">
Moves the start boundary of a string, by index, for a selected number of characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbdae612-1d6e-4f10-9b55-5ee038f27b79">PrefixTop</a>
</td>
<td align="left" width="63%">
Prefixes a string to the top  string in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes a string from a string collection, starting at an index. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ebf7b46-8398-4751-b8b3-19e94fdbce87">SetFormattedText</a>
</td>
<td align="left" width="63%">
Replaces text with formatted text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c869a42a-0937-4051-9cb0-d454255989d2">SetOpCp</a>
</td>
<td align="left" width="63%">
Sets the character position in the source range's story that has desired character formatting attributes.  The <a href="https://msdn.microsoft.com/f22bb343-4fcc-4473-84cc-807011b5a7b0">ITextStrings::EncodeFunction</a> method applies those character formatting attributes to the operators specified by the <i>Char</i>, <i>Char1</i>, and <i>Char2</i> parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66f4e5c6-e97b-48a5-9c71-3efb1eba12d6">SuffixTop</a>
</td>
<td align="left" width="63%">
Suffixes a string to the top string in the collection. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06759b26-672c-4a3d-a2d4-085bfd09e50a">Swap</a>
</td>
<td align="left" width="63%">
Swaps the top two strings in the collection.

</td>
</tr>
</table> 

