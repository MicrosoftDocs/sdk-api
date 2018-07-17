---
UID: NN:tom.ITextPara
title: ITextPara
author: windows-sdk-content
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\ITextPara.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: ITextPara, ITextPara interface [Windows Controls], ITextPara interface [Windows Controls],described, _win32_ITextPara, _win32_ITextPara_cpp, controls.ITextPara, controls._win32_ITextPara, tom/ITextPara
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
 - ITextPara
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara interface


## -description


Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <a href="https://msdn.microsoft.com/library/Bb774054(v=VS.85).aspx">ITextFont</a> and <b>ITextPara</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextPara</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITextPara</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/Bb787728(v=VS.85).aspx">AddTab</a>
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
<a href="https://msdn.microsoft.com/library/Bb787842(v=VS.85).aspx">CanChange</a>
</td>
<td align="left" width="63%">
Determines whether the paragraph formatting can be changed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787738(v=VS.85).aspx">ClearAllTabs</a>
</td>
<td align="left" width="63%">
Clears all tabs, reverting to equally spaced tabs with the default tab spacing. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787748(v=VS.85).aspx">DeleteTab</a>
</td>
<td align="left" width="63%">
Deletes a tab at a specified displacement. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773927(v=VS.85).aspx">GetAlignment</a>
</td>
<td align="left" width="63%">
Retrieves the current paragraph alignment value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787843(v=VS.85).aspx">GetDuplicate</a>
</td>
<td align="left" width="63%">
Creates a duplicate of the specified paragraph format object. The duplicate property is the default property of an <b>ITextPara</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773951(v=VS.85).aspx">GetFirstLineIndent</a>
</td>
<td align="left" width="63%">
Retrieves the amount used to indent the first line of a paragraph relative to the left indent. The left indent is the indent for all lines of the paragraph except the first line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773962(v=VS.85).aspx">GetHyphenation</a>
</td>
<td align="left" width="63%">
Determines whether automatic hyphenation is enabled for the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773968(v=VS.85).aspx">GetKeepTogether</a>
</td>
<td align="left" width="63%">
Determines whether page breaks are allowed within paragraphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773971(v=VS.85).aspx">GetKeepWithNext</a>
</td>
<td align="left" width="63%">
Determines whether page breaks are allowed between paragraphs in the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773977(v=VS.85).aspx">GetLeftIndent</a>
</td>
<td align="left" width="63%">
Retrieves the distance used to indent all lines except the first line of a paragraph. The distance is relative to the left margin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773979(v=VS.85).aspx">GetLineSpacing</a>
</td>
<td align="left" width="63%">
Retrieves the line-spacing value for the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773981(v=VS.85).aspx">GetLineSpacingRule</a>
</td>
<td align="left" width="63%">
Retrieves the line-spacing rule for the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773983(v=VS.85).aspx">GetListAlignment</a>
</td>
<td align="left" width="63%">
Retrieves the kind of alignment to use for bulleted and numbered lists. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773985(v=VS.85).aspx">GetListLevelIndex</a>
</td>
<td align="left" width="63%">
Retrieves the list level index used with paragraphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773987(v=VS.85).aspx">GetListStart</a>
</td>
<td align="left" width="63%">
Retrieves the starting value or code of a list numbering sequence. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773989(v=VS.85).aspx">GetListTab</a>
</td>
<td align="left" width="63%">
Retrieves the list tab setting, which is the distance between the first-line indent and the text on the first line. The numbered or bulleted text is left-justified, centered, or right-justified at the first-line indent value. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773991(v=VS.85).aspx">GetListType</a>
</td>
<td align="left" width="63%">
Retrieves the kind of numbering to use with paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773993(v=VS.85).aspx">GetNoLineNumber</a>
</td>
<td align="left" width="63%">
Determines whether paragraph numbering is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb773997(v=VS.85).aspx">GetPageBreakBefore</a>
</td>
<td align="left" width="63%">
Determines whether each paragraph in the range must begin on a new page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774009(v=VS.85).aspx">GetRightIndent</a>
</td>
<td align="left" width="63%">
Retrieves the size of the right margin indent of a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774021(v=VS.85).aspx">GetSpaceAfter</a>
</td>
<td align="left" width="63%">
Retrieves the amount of vertical space below a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774023(v=VS.85).aspx">GetSpaceBefore</a>
</td>
<td align="left" width="63%">
Retrieves the amount of vertical space above a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787845(v=VS.85).aspx">GetStyle</a>
</td>
<td align="left" width="63%">
Retrieves the style handle to the paragraphs in the specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774034(v=VS.85).aspx">GetTab</a>
</td>
<td align="left" width="63%">
Retrieves tab parameters (displacement, alignment, and leader style) for a specified tab. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774035(v=VS.85).aspx">GetTabCount</a>
</td>
<td align="left" width="63%">
Retrieves the tab count. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774042(v=VS.85).aspx">GetWidowControl</a>
</td>
<td align="left" width="63%">
Retrieves the widow and orphan control state for the paragraphs in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926880">IsEqual</a>
</td>
<td align="left" width="63%">
Determines if the current range has the same properties as a specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the paragraph formatting to a choice of default values. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774123(v=VS.85).aspx">SetAlignment</a>
</td>
<td align="left" width="63%">
Sets the paragraph alignment. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787851(v=VS.85).aspx">SetDuplicate</a>
</td>
<td align="left" width="63%">
Sets the formatting for an existing paragraph by copying a given format. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774153(v=VS.85).aspx">SetHyphenation</a>
</td>
<td align="left" width="63%">
Controls hyphenation for the paragraphs in the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774155(v=VS.85).aspx">SetIndents</a>
</td>
<td align="left" width="63%">
Sets the first-line indent, the left indent, and the right indent for a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774161(v=VS.85).aspx">SetKeepTogether</a>
</td>
<td align="left" width="63%">
Controls whether page breaks are allowed within a paragraph in a range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774163(v=VS.85).aspx">SetKeepWithNext</a>
</td>
<td align="left" width="63%">
Controls whether page breaks are allowed between the paragraphs in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774169(v=VS.85).aspx">SetLineSpacing</a>
</td>
<td align="left" width="63%">
Sets the paragraph line-spacing rule and the line spacing for a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774171(v=VS.85).aspx">SetListAlignment</a>
</td>
<td align="left" width="63%">
Sets the alignment of bulleted or numbered text used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774173(v=VS.85).aspx">SetListLevelIndex</a>
</td>
<td align="left" width="63%">
Sets the list level index used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774175(v=VS.85).aspx">SetListStart</a>
</td>
<td align="left" width="63%">
Sets the starting number or Unicode value for a numbered list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb774177(v=VS.85).aspx">SetListTab</a>
</td>
<td align="left" width="63%">
Sets the list tab setting, which is the distance between the first indent and the start of the text on the first line. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787786(v=VS.85).aspx">SetListType</a>
</td>
<td align="left" width="63%">
Sets the type of list to be used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787790(v=VS.85).aspx">SetNoLineNumber</a>
</td>
<td align="left" width="63%">
Determines whether to suppress line numbering of paragraphs in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787795(v=VS.85).aspx">SetPageBreakBefore</a>
</td>
<td align="left" width="63%">
Controls whether there is a page break before each paragraph in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787807(v=VS.85).aspx">SetRightIndent</a>
</td>
<td align="left" width="63%">
Sets the right margin of paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787817(v=VS.85).aspx">SetSpaceAfter</a>
</td>
<td align="left" width="63%">
Sets the amount of space that follows a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787820(v=VS.85).aspx">SetSpaceBefore</a>
</td>
<td align="left" width="63%">
Sets the amount of space preceding a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787853(v=VS.85).aspx">SetStyle</a>
</td>
<td align="left" width="63%">
Sets the paragraph style for the paragraphs in a range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/Bb787834(v=VS.85).aspx">SetWidowControl</a>
</td>
<td align="left" width="63%">
Controls the suppression of widows and orphans.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/library/Bb774054(v=VS.85).aspx">ITextFont</a> and <b>ITextPara</b> interfaces encapsulate the functionality of the Microsoft Word Format <b>Font</b> and <b>Paragraph</b> dialog boxes, respectively. Both interfaces include a duplicate (<b>Value</b>) property that can return a duplicate of the attributes in a range object or transfer a set of attributes to a range. As such, they act like programmable format painters. For example, you could transfer all attributes from range r1 to range r2 except for making r2 bold and the font size 12 points by using the following subroutine.

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
See <a href="https://msdn.microsoft.com/library/Bb774145(v=VS.85).aspx">SetFont</a> for a similar example written in C++.

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



<a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/library/Bb787607(v=VS.85).aspx">Text Object Model</a>



<a href="https://msdn.microsoft.com/library/Bb787726(v=VS.85).aspx">Using The Text Object Model</a>
 

 

