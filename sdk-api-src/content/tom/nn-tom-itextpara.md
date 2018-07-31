---
UID: NN:tom.ITextPara
title: ITextPara
author: windows-sdk-content
description: Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, ITextFont and ITextPara.
old-location: controls\ITextPara.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
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


Text Object Model (TOM) rich text-range attributes are accessed through a pair of dual interfaces, <a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a> and <b>ITextPara</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextPara</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITextPara</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">AddTab</a>
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
<a href="https://msdn.microsoft.com/80f4a5f7-819b-435c-942b-155c1e4c1477">CanChange</a>
</td>
<td align="left" width="63%">
Determines whether the paragraph formatting can be changed. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61899b21-a883-440d-bb2c-0c65b6ae48c0">ClearAllTabs</a>
</td>
<td align="left" width="63%">
Clears all tabs, reverting to equally spaced tabs with the default tab spacing. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82950caa-4fbc-4f80-aae4-91feecccef65">DeleteTab</a>
</td>
<td align="left" width="63%">
Deletes a tab at a specified displacement. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d97c5efb-3007-40f5-b4f5-30a3505e01aa">GetAlignment</a>
</td>
<td align="left" width="63%">
Retrieves the current paragraph alignment value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/683bfbe3-9f8f-4b33-a2de-f9cba437e3ff">GetDuplicate</a>
</td>
<td align="left" width="63%">
Creates a duplicate of the specified paragraph format object. The duplicate property is the default property of an <b>ITextPara</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82831ef0-7ece-4d85-96f5-aa3c4591e458">GetFirstLineIndent</a>
</td>
<td align="left" width="63%">
Retrieves the amount used to indent the first line of a paragraph relative to the left indent. The left indent is the indent for all lines of the paragraph except the first line.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7064f54-5c3a-46b2-8d9c-f9dbe037f04c">GetHyphenation</a>
</td>
<td align="left" width="63%">
Determines whether automatic hyphenation is enabled for the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bcbf89da-e853-4c1d-a13c-812d5905ad77">GetKeepTogether</a>
</td>
<td align="left" width="63%">
Determines whether page breaks are allowed within paragraphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6c90681-2691-4bfb-8a6b-c1d92f276a61">GetKeepWithNext</a>
</td>
<td align="left" width="63%">
Determines whether page breaks are allowed between paragraphs in the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/032f4068-ae5d-4b4e-ae7e-8a093d348d7f">GetLeftIndent</a>
</td>
<td align="left" width="63%">
Retrieves the distance used to indent all lines except the first line of a paragraph. The distance is relative to the left margin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9d3ad53-3d64-4260-b4cf-41038e652ba8">GetLineSpacing</a>
</td>
<td align="left" width="63%">
Retrieves the line-spacing value for the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65a1b836-4f90-4b9b-8adc-68ace163df6a">GetLineSpacingRule</a>
</td>
<td align="left" width="63%">
Retrieves the line-spacing rule for the text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc6785be-4e05-48fb-97ae-6f3e3518db9f">GetListAlignment</a>
</td>
<td align="left" width="63%">
Retrieves the kind of alignment to use for bulleted and numbered lists. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37ea25ee-a41b-42d4-99c4-d316f596c040">GetListLevelIndex</a>
</td>
<td align="left" width="63%">
Retrieves the list level index used with paragraphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e797f494-bc34-4529-a773-22d1ebfe1250">GetListStart</a>
</td>
<td align="left" width="63%">
Retrieves the starting value or code of a list numbering sequence. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1fb072d7-6311-4a44-b1e1-ec6ee9ba654d">GetListTab</a>
</td>
<td align="left" width="63%">
Retrieves the list tab setting, which is the distance between the first-line indent and the text on the first line. The numbered or bulleted text is left-justified, centered, or right-justified at the first-line indent value. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df2b0821-9216-465a-b066-60807a0b3e0f">GetListType</a>
</td>
<td align="left" width="63%">
Retrieves the kind of numbering to use with paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81a22c2f-a83e-4f0e-a4aa-4df7ed860ee9">GetNoLineNumber</a>
</td>
<td align="left" width="63%">
Determines whether paragraph numbering is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f61e6f65-4709-439a-8e2a-5acc49ca7ab4">GetPageBreakBefore</a>
</td>
<td align="left" width="63%">
Determines whether each paragraph in the range must begin on a new page.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62db02a9-8fa1-48c8-91ee-71ad0e8e1e8c">GetRightIndent</a>
</td>
<td align="left" width="63%">
Retrieves the size of the right margin indent of a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/affdb197-f8c5-46b1-a2b4-f21776e362b3">GetSpaceAfter</a>
</td>
<td align="left" width="63%">
Retrieves the amount of vertical space below a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86c453b5-e839-42d6-9ef8-d2c1c0f54af3">GetSpaceBefore</a>
</td>
<td align="left" width="63%">
Retrieves the amount of vertical space above a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe85a591-6254-46a2-8f06-8079f0a602c1">GetStyle</a>
</td>
<td align="left" width="63%">
Retrieves the style handle to the paragraphs in the specified range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78e1c637-c2ae-4919-8e2f-8e8b89743ac4">GetTab</a>
</td>
<td align="left" width="63%">
Retrieves tab parameters (displacement, alignment, and leader style) for a specified tab. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4440ce51-f504-4489-851f-08895b23a22b">GetTabCount</a>
</td>
<td align="left" width="63%">
Retrieves the tab count. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/195530bb-2e51-4a1f-9e85-21b9db1b7fe6">GetWidowControl</a>
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
<a href="https://msdn.microsoft.com/7d4dbd7e-8164-4005-bcd2-36ddf5fbf9a9">SetAlignment</a>
</td>
<td align="left" width="63%">
Sets the paragraph alignment. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/054e3a0b-6a73-4830-b382-ea4f520bab03">SetDuplicate</a>
</td>
<td align="left" width="63%">
Sets the formatting for an existing paragraph by copying a given format. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0d8c426-bc6d-4175-ba56-68a9bb31bd46">SetHyphenation</a>
</td>
<td align="left" width="63%">
Controls hyphenation for the paragraphs in the range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84584a22-7e0f-431a-9c7b-f7f574459948">SetIndents</a>
</td>
<td align="left" width="63%">
Sets the first-line indent, the left indent, and the right indent for a paragraph. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c4a5f0cc-b87a-4209-8614-20adc3f3002a">SetKeepTogether</a>
</td>
<td align="left" width="63%">
Controls whether page breaks are allowed within a paragraph in a range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc90c377-bae6-4aa8-8bb8-26dc9c915bae">SetKeepWithNext</a>
</td>
<td align="left" width="63%">
Controls whether page breaks are allowed between the paragraphs in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36ef5af4-90dd-4185-92c9-5c4e88bf5ec2">SetLineSpacing</a>
</td>
<td align="left" width="63%">
Sets the paragraph line-spacing rule and the line spacing for a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fabc8f6-da0f-470c-96a2-9cd0638d3269">SetListAlignment</a>
</td>
<td align="left" width="63%">
Sets the alignment of bulleted or numbered text used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60f88971-e671-4f65-aeba-1774f732d4a9">SetListLevelIndex</a>
</td>
<td align="left" width="63%">
Sets the list level index used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ba2346a-b56a-4eda-a6f9-0563e71c9cbd">SetListStart</a>
</td>
<td align="left" width="63%">
Sets the starting number or Unicode value for a numbered list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21966279-d84f-4f1a-9e90-5e0e79b14c7e">SetListTab</a>
</td>
<td align="left" width="63%">
Sets the list tab setting, which is the distance between the first indent and the start of the text on the first line. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f9adb67-e4d6-41c9-b360-efbcead7befc">SetListType</a>
</td>
<td align="left" width="63%">
Sets the type of list to be used for paragraphs. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4c8d079-f832-4030-98eb-4a07cb7a8f05">SetNoLineNumber</a>
</td>
<td align="left" width="63%">
Determines whether to suppress line numbering of paragraphs in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f94aba1-62df-4714-ab50-a86fc679f407">SetPageBreakBefore</a>
</td>
<td align="left" width="63%">
Controls whether there is a page break before each paragraph in a range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46537c8b-1500-4416-b0a6-3c54dd3ea236">SetRightIndent</a>
</td>
<td align="left" width="63%">
Sets the right margin of paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e4fb12e-a7ac-4776-be66-ad5e4fdf9370">SetSpaceAfter</a>
</td>
<td align="left" width="63%">
Sets the amount of space that follows a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/003aa8d2-f80e-4925-8e25-dcb3ea6d95cf">SetSpaceBefore</a>
</td>
<td align="left" width="63%">
Sets the amount of space preceding a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/939e58d5-4bd8-4139-9e10-71b4850705f0">SetStyle</a>
</td>
<td align="left" width="63%">
Sets the paragraph style for the paragraphs in a range. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87bc1ef8-2422-4a4a-af15-f28aace74f34">SetWidowControl</a>
</td>
<td align="left" width="63%">
Controls the suppression of widows and orphans.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/e8e3ba98-808b-49c5-8764-96484fa33a6e">ITextFont</a> and <b>ITextPara</b> interfaces encapsulate the functionality of the Microsoft Word Format <b>Font</b> and <b>Paragraph</b> dialog boxes, respectively. Both interfaces include a duplicate (<b>Value</b>) property that can return a duplicate of the attributes in a range object or transfer a set of attributes to a range. As such, they act like programmable format painters. For example, you could transfer all attributes from range r1 to range r2 except for making r2 bold and the font size 12 points by using the following subroutine.

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



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>



<a href="https://msdn.microsoft.com/5d9ab4fa-e9a0-4031-bbaa-311aff912eba">Using The Text Object Model</a>
 

 

