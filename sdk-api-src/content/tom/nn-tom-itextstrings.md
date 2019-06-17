---
UID: NN:tom.ITextStrings
title: ITextStrings (tom.h)
author: windows-sdk-content
description: The ITextStrings interface represents a collection of rich-text strings that are useful for manipulating rich text.
old-location: controls\itextstrings.htm
tech.root: Controls
ms.assetid: c878d0db-ac13-4ac9-8601-d1c1ba76cd85
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextStrings, ITextStrings interface [Windows Controls], ITextStrings interface [Windows Controls],described, controls.itextstrings, tom/ITextStrings
ms.topic: interface
f1_keywords: ["tom/ITextStrings"]
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
 - ITextStrings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextStrings interface


## -description


The <b>ITextStrings</b> interface represents a collection of rich-text strings that are useful for manipulating rich text. In particular, you can use the collection to convert linearly formatted math expressions into built-up form and vice versa. You can also use the collection to collect the concatenation of a set of rich-text strings, or to manipulate a string without changing a primary story. The collection is efficiently implemented by concatenating the strings in a scratch story and maintaining an array of the string counts that identify the strings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStrings</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITextStrings</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-add">Add</a>
</td>
<td align="left" width="63%">
Adds a string to the end of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-append">Append</a>
</td>
<td align="left" width="63%">
Appends a string to the string at the specified index in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-cat2">Cat2</a>
</td>
<td align="left" width="63%">
Concatenates two strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-cattop2">CatTop2</a>
</td>
<td align="left" width="63%">
Inserts text between the top two strings in a collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-deleterange">DeleteRange</a>
</td>
<td align="left" width="63%">
Deletes the contents of a given range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-encodefunction">EncodeFunction</a>
</td>
<td align="left" width="63%">
Encodes an object, given a set of argument strings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-getcch">GetCch</a>
</td>
<td align="left" width="63%">
Gets the count of characters for a selected string index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the number of strings in a string collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-insertnullstr">InsertNullStr</a>
</td>
<td align="left" width="63%">
Inserts a <b>NULL</b> string in the collection at a selected string index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-item">Item</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object for a selected index in a string collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-moveboundary">MoveBoundary</a>
</td>
<td align="left" width="63%">
Moves the start boundary of a string, by index, for a selected number of characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-prefixtop">PrefixTop</a>
</td>
<td align="left" width="63%">
Prefixes a string to the top  string in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes a string from a string collection, starting at an index. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-setformattedtext">SetFormattedText</a>
</td>
<td align="left" width="63%">
Replaces text with formatted text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-setopcp">SetOpCp</a>
</td>
<td align="left" width="63%">
Sets the character position in the source range's story that has desired character formatting attributes.  The <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-encodefunction">ITextStrings::EncodeFunction</a> method applies those character formatting attributes to the operators specified by the <i>Char</i>, <i>Char1</i>, and <i>Char2</i> parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-suffixtop">SuffixTop</a>
</td>
<td align="left" width="63%">
Suffixes a string to the top string in the collection. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextstrings-swap">Swap</a>
</td>
<td align="left" width="63%">
Swaps the top two strings in the collection.

</td>
</tr>
</table> 

