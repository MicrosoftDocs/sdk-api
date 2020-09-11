---
UID: NN:tom.ITextPara
title: ITextPara (tom.h)
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara.
helpviewer_keywords: ["ITextPara","ITextPara interface [Windows Controls]","ITextPara interface [Windows Controls]","described","_win32_ITextPara","_win32_ITextPara_cpp","controls.ITextPara","controls._win32_ITextPara","tom/ITextPara"]
old-location: controls\ITextPara.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara.htm
ms.date: 12/05/2018
ms.keywords: ITextPara, ITextPara interface [Windows Controls], ITextPara interface [Windows Controls],described, _win32_ITextPara, _win32_ITextPara_cpp, controls.ITextPara, controls._win32_ITextPara, tom/ITextPara
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextPara
 - tom/ITextPara
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
 - ITextPara
---

# ITextPara interface


## -description

Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> and <b>ITextPara</b>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextPara</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITextPara</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextPara</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-addtab">AddTab</a>
</td>
<td align="left" width="63%">
Adds a tab at the displacement 
			<i>tbPos</i>, with type 
			<i>tbAlign</i>, and leader style, 
			<i>tbLeader</i>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-canchange">CanChange</a>
</td>
<td align="left" width="63%">
Determines whether the paragraph formatting can be changed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-clearalltabs">ClearAllTabs</a>
</td>
<td align="left" width="63%">
Clears all tabs, reverting to equally spaced tabs with the default tab spacing. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-deletetab">DeleteTab</a>
</td>
<td align="left" width="63%">
Deletes a tab at a specified displacement. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getalignment">GetAlignment</a>
</td>
<td align="left" width="63%">
Retrieves the current paragraph alignment value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getduplicate">GetDuplicate</a>
</td>
<td align="left" width="63%">
Creates a duplicate of the specified paragraph format object. The duplicate property is the default property of an <b>ITextPara</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getfirstlineindent">GetFirstLineIndent</a>
</td>
<td align="left" width="63%">
Retrieves the amount used to indent the first line of a paragraph relative to the left indent. The left indent is the indent for all lines of the paragraph except the first line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-gethyphenation">GetHyphenation</a>
</td>
<td align="left" width="63%">
Determines whether automatic hyphenation is enabled for the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getkeeptogether">GetKeepTogether</a>
</td>
<td align="left" width="63%">
Determines whether page breaks are allowed within paragraphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getkeepwithnext">GetKeepWithNext</a>
</td>
<td align="left" width="63%">
Determines whether page breaks are allowed between paragraphs in the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getleftindent">GetLeftIndent</a>
</td>
<td align="left" width="63%">
Retrieves the distance used to indent all lines except the first line of a paragraph. The distance is relative to the left margin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getlinespacing">GetLineSpacing</a>
</td>
<td align="left" width="63%">
Retrieves the line-spacing value for the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getlinespacingrule">GetLineSpacingRule</a>
</td>
<td align="left" width="63%">
Retrieves the line-spacing rule for the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getlistalignment">GetListAlignment</a>
</td>
<td align="left" width="63%">
Retrieves the kind of alignment to use for bulleted and numbered lists. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getlistlevelindex">GetListLevelIndex</a>
</td>
<td align="left" width="63%">
Retrieves the list level index used with paragraphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getliststart">GetListStart</a>
</td>
<td align="left" width="63%">
Retrieves the starting value or code of a list numbering sequence. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getlisttab">GetListTab</a>
</td>
<td align="left" width="63%">
Retrieves the list tab setting, which is the distance between the first-line indent and the text on the first line. The numbered or bulleted text is left-justified, centered, or right-justified at the first-line indent value. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getlisttype">GetListType</a>
</td>
<td align="left" width="63%">
Retrieves the kind of numbering to use with paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getnolinenumber">GetNoLineNumber</a>
</td>
<td align="left" width="63%">
Determines whether paragraph numbering is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getpagebreakbefore">GetPageBreakBefore</a>
</td>
<td align="left" width="63%">
Determines whether each paragraph in the range must begin on a new page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getrightindent">GetRightIndent</a>
</td>
<td align="left" width="63%">
Retrieves the size of the right margin indent of a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getspaceafter">GetSpaceAfter</a>
</td>
<td align="left" width="63%">
Retrieves the amount of vertical space below a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getspacebefore">GetSpaceBefore</a>
</td>
<td align="left" width="63%">
Retrieves the amount of vertical space above a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getstyle">GetStyle</a>
</td>
<td align="left" width="63%">
Retrieves the style handle to the paragraphs in the specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-gettab">GetTab</a>
</td>
<td align="left" width="63%">
Retrieves tab parameters (displacement, alignment, and leader style) for a specified tab. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-gettabcount">GetTabCount</a>
</td>
<td align="left" width="63%">
Retrieves the tab count. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-getwidowcontrol">GetWidowControl</a>
</td>
<td align="left" width="63%">
Retrieves the widow and orphan control state for the paragraphs in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-isequal">IsEqual</a>
</td>
<td align="left" width="63%">
Determines if the current range has the same properties as a specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the paragraph formatting to a choice of default values. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setalignment">SetAlignment</a>
</td>
<td align="left" width="63%">
Sets the paragraph alignment. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setduplicate">SetDuplicate</a>
</td>
<td align="left" width="63%">
Sets the formatting for an existing paragraph by copying a given format. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-sethyphenation">SetHyphenation</a>
</td>
<td align="left" width="63%">
Controls hyphenation for the paragraphs in the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setindents">SetIndents</a>
</td>
<td align="left" width="63%">
Sets the first-line indent, the left indent, and the right indent for a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setkeeptogether">SetKeepTogether</a>
</td>
<td align="left" width="63%">
Controls whether page breaks are allowed within a paragraph in a range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setkeepwithnext">SetKeepWithNext</a>
</td>
<td align="left" width="63%">
Controls whether page breaks are allowed between the paragraphs in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setlinespacing">SetLineSpacing</a>
</td>
<td align="left" width="63%">
Sets the paragraph line-spacing rule and the line spacing for a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setlistalignment">SetListAlignment</a>
</td>
<td align="left" width="63%">
Sets the alignment of bulleted or numbered text used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setlistlevelindex">SetListLevelIndex</a>
</td>
<td align="left" width="63%">
Sets the list level index used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setliststart">SetListStart</a>
</td>
<td align="left" width="63%">
Sets the starting number or Unicode value for a numbered list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setlisttab">SetListTab</a>
</td>
<td align="left" width="63%">
Sets the list tab setting, which is the distance between the first indent and the start of the text on the first line. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setlisttype">SetListType</a>
</td>
<td align="left" width="63%">
Sets the type of list to be used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setnolinenumber">SetNoLineNumber</a>
</td>
<td align="left" width="63%">
Determines whether to suppress line numbering of paragraphs in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setpagebreakbefore">SetPageBreakBefore</a>
</td>
<td align="left" width="63%">
Controls whether there is a page break before each paragraph in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setrightindent">SetRightIndent</a>
</td>
<td align="left" width="63%">
Sets the right margin of paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setspaceafter">SetSpaceAfter</a>
</td>
<td align="left" width="63%">
Sets the amount of space that follows a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setspacebefore">SetSpaceBefore</a>
</td>
<td align="left" width="63%">
Sets the amount of space preceding a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setstyle">SetStyle</a>
</td>
<td align="left" width="63%">
Sets the paragraph style for the paragraphs in a range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextpara-setwidowcontrol">SetWidowControl</a>
</td>
<td align="left" width="63%">
Controls the suppression of widows and orphans.

</td>
</tr>
</table>

## -remarks

The <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> and <b>ITextPara</b> interfaces encapsulate the functionality of the Microsoft Word Format <b>Font</b> and <b>Paragraph</b> dialog boxes, respectively. Both interfaces include a duplicate (<b>Value</b>) property that can return a duplicate of the attributes in a range object or transfer a set of attributes to a range. As such, they act like programmable format painters. For example, you could transfer all attributes from range r1 to range r2 except for making r2 bold and the font size 12 points by using the following subroutine.


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

The <b>ITextPara</b> interface encapsulates the Word Paragraph dialog box. All measurements are given in floating-point points. The rich edit control is able to accept and return all <b>ITextPara</b> properties intact (that is, without modification), both through TOM and through its Rich Text Format (RTF) converters. However, the following properties have no effect on what the control displays:

<ul>
<li>DoNotHyphen</li>
<li>KeepTogether</li>
<li>KeepWithNext</li>
<li>LineSpacing</li>
<li>LineSpacingRule</li>
<li>NoLineNumber</li>
<li>PageBreakBefore</li>
<li>Tab alignments</li>
<li>Tab styles (other than tomAlignLeft and tomSpaces)</li>
<li>Style WidowControl</li>
</ul>

## -see-also

<b>Conceptual</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/text-object-model">Text Object Model</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/using-the-text-object-model">Using The Text Object Model</a>

