---
UID: NN:tom.ITextRange2
title: ITextRange2 (tom.h)
description: The ITextRange2 interface is derived from ITextRange, and its objects are powerful editing and data-binding tools that enable a program to select text in a story and then examine or change that text.
helpviewer_keywords: ["ITextRange2","ITextRange2 interface [Windows Controls]","ITextRange2 interface [Windows Controls]","described","controls.itextrange2","tom/ITextRange2"]
old-location: controls\itextrange2.htm
tech.root: Controls
ms.assetid: 905f0967-8b99-45ed-a1cc-19d49e919a65
ms.date: 12/05/2018
ms.keywords: ITextRange2, ITextRange2 interface [Windows Controls], ITextRange2 interface [Windows Controls],described, controls.itextrange2, tom/ITextRange2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRange2
 - tom/ITextRange2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2
---

# ITextRange2 interface


## -description

The <b>ITextRange2</b> interface is derived from <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>, and its objects are powerful editing and data-binding tools that enable a program to select text in a story and then examine or change that text.

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
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-addsubrange">AddSubrange</a>
</td>
<td align="left" width="63%">
Adds a subrange to this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-buildupmath">BuildUpMath</a>
</td>
<td align="left" width="63%">
Converts the linear-format math in a range to a built-up form, or modifies the current built-up form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-deletesubrange">DeleteSubrange</a>
</td>
<td align="left" width="63%">
Deletes a subrange from a range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-find">Find</a>
</td>
<td align="left" width="63%">
Searchs for math inline functions in text as specified by a source range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getcch">GetCch</a>
</td>
<td align="left" width="63%">
Gets the count of characters in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getcells">GetCells</a>
</td>
<td align="left" width="63%">
Gets a cells object with the parameters of cells in the currently selected table row or column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getchar2">GetChar2</a>
</td>
<td align="left" width="63%">
Gets the character at the specified offset from the end of this range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getcolumn">GetColumn</a>
</td>
<td align="left" width="63%">
Gets the column properties for the currently selected column.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getcount">GetCount</a>
</td>
<td align="left" width="63%">
Gets the count of subranges, including the  active subrange in the current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getdropcap">GetDropCap</a>
</td>
<td align="left" width="63%">
Gets the drop-cap parameters of the paragraph that contains this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getduplicate2">GetDuplicate2</a>
</td>
<td align="left" width="63%">
Gets a duplicate of a range object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getfont2">GetFont2</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a> object with the character attributes of the current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getformattedtext2">GetFormattedText2</a>
</td>
<td align="left" width="63%">
Gets an <b>ITextRange2</b> object with the current range's formatted text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getgravity">GetGravity</a>
</td>
<td align="left" width="63%">
Gets the gravity of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">GetInlineObject</a>
</td>
<td align="left" width="63%">
Gets the properties of the inline object at the range active end.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getmathfunctiontype">GetMathFunctionType</a>
</td>
<td align="left" width="63%">
Retrieves the math function type associated with the specified math function name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getpara2">GetPara2</a>
</td>
<td align="left" width="63%">
Gets an <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a> object with the paragraph attributes of a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of a property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getrect">GetRect</a>
</td>
<td align="left" width="63%">
Retrieves a rectangle of the specified type for the current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getrow">GetRow</a>
</td>
<td align="left" width="63%">
Gets the row properties in the currently selected row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getstartpara">GetStartPara</a>
</td>
<td align="left" width="63%">
Gets the character position of the start of the paragraph that contains the range's start character position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-getsubrange">GetSubrange</a>
</td>
<td align="left" width="63%">
Retrieves a subrange in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-gettable">GetTable</a>
</td>
<td align="left" width="63%">
Gets the table properties in the currently selected table. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-gettext2">GetText2</a>
</td>
<td align="left" width="63%">
Gets the text in this range according to the specified conversion flags.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-geturl">GetURL</a>
</td>
<td align="left" width="63%">
Returns the URL text associated with a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-hextounicode">HexToUnicode</a>
</td>
<td align="left" width="63%">
Converts and replaces the hexadecimal number at the end of this range to a Unicode character.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-insertimage">InsertImage</a>
</td>
<td align="left" width="63%">
Inserts an image into this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-inserttable">InsertTable</a>
</td>
<td align="left" width="63%">
Inserts a table in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-linearize">Linearize</a>
</td>
<td align="left" width="63%">
Translates the built-up math, ruby, and other inline objects in this range to linearized form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-setactivesubrange">SetActiveSubrange</a>
</td>
<td align="left" width="63%">
Makes the specified  subrange the active subrange of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-setdropcap">SetDropCap</a>
</td>
<td align="left" width="63%">
Sets the drop-cap parameters for the paragraph that contains the current range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-setfont2">SetFont2</a>
</td>
<td align="left" width="63%">
Sets the character formatting attributes of the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-setformattedtext2">SetFormattedText2</a>
</td>
<td align="left" width="63%">
Sets the text of this range to the formatted text of the specified range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-setgravity">SetGravity</a>
</td>
<td align="left" width="63%">
Sets the gravity of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-setinlineobject">SetInlineObject</a>
</td>
<td align="left" width="63%">
Sets or inserts the properties of an inline object for a degenerate range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-setpara2">SetPara2</a>
</td>
<td align="left" width="63%">
Sets the paragraph format attributes of a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-settext2">SetText2</a>
</td>
<td align="left" width="63%">
Sets the text of this range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-seturl">SetURL</a>
</td>
<td align="left" width="63%">
Sets the text in this range to that of the specified URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange2-unicodetohex">UnicodeToHex</a>
</td>
<td align="left" width="63%">
Converts the Unicode character(s) preceding the start position of this text range to a hexadecimal number, and selects it.

</td>
</tr>
</table>

