---
UID: NN:tom.ITextRow
title: ITextRow (tom.h)
author: windows-sdk-content
description: The ITextRow interface provides methods to insert one or more identical table rows, and to retrieve and change table row properties. To insert nonidentical rows, call ITextRow::Insert for each different row configuration.
old-location: controls\itextrow.htm
tech.root: Controls
ms.assetid: 49f5ffc1-d615-4d07-9f41-1c5f0dd9045b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextRow, ITextRow interface [Windows Controls], ITextRow interface [Windows Controls],described, controls.itextrow, tom/ITextRow
ms.topic: interface
f1_keywords: 
 - "tom/ITextRow"
dev_langs:
 - c++
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
 - ITextRow
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextRow interface


## -description


The <b>ITextRow</b> interface provides methods to insert one or more identical table rows, and to retrieve and change table row properties. To insert nonidentical rows, call <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-insert">ITextRow::Insert</a> for each different row configuration. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextRow</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITextRow</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextRow</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-apply">Apply</a>
</td>
<td align="left" width="63%">
Applies the formatting attributes of this text row object to the specified rows in the associated <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-canchange">CanChange</a>
</td>
<td align="left" width="63%">
Determines whether changes can be made to this row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getalignment">GetAlignment</a>
</td>
<td align="left" width="63%">
Gets the horizontal alignment of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellalignment">GetCellAlignment</a>
</td>
<td align="left" width="63%">
Gets the vertical alignment of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellbordercolors">GetCellBorderColors</a>
</td>
<td align="left" width="63%">
Gets the border colors of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellborderwidths">GetCellBorderWidths</a>
</td>
<td align="left" width="63%">
Gets the border widths of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellcolorback">GetCellColorBack</a>
</td>
<td align="left" width="63%">
Gets the background color of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellcolorfore">GetCellColorFore</a>
</td>
<td align="left" width="63%">
Gets the foreground color of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellcount">GetCellCount</a>
</td>
<td align="left" width="63%">
Gets the count of cells in this row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellcountcache">GetCellCountCache</a>
</td>
<td align="left" width="63%">
Gets the count of cells cached for this row. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellindex">GetCellIndex</a>
</td>
<td align="left" width="63%">
Gets the index of the active cell to get or set parameters for.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellmargin">GetCellMargin</a>
</td>
<td align="left" width="63%">
Gets the cell margin of this row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellmergeflags">GetCellMergeFlags</a>
</td>
<td align="left" width="63%">
Gets the merge flags of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellshading">GetCellShading</a>
</td>
<td align="left" width="63%">
Gets the shading of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellverticaltext">GetCellVerticalText</a>
</td>
<td align="left" width="63%">
Gets the vertical-text setting of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getcellwidth">GetCellWidth</a>
</td>
<td align="left" width="63%">
Gets the width of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getheight">GetHeight</a>
</td>
<td align="left" width="63%">
Gets the height of the row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getindent">GetIndent</a>
</td>
<td align="left" width="63%">
Gets the indent of this row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getkeeptogether">GetKeepTogether</a>
</td>
<td align="left" width="63%">
Gets whether this row is allowed to be broken across pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getkeepwithnext">GetKeepWithNext</a>
</td>
<td align="left" width="63%">
Gets  whether this row should appear on the same page as the row that follows it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getnestlevel">GetNestLevel</a>
</td>
<td align="left" width="63%">
Gets the nest level of a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getproperty">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-getrtl">GetRTL</a>
</td>
<td align="left" width="63%">
Gets whether this row has right-to-left orientation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-insert">Insert</a>
</td>
<td align="left" width="63%">
Inserts a row, or rows, at the location identified by the associated <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-isequal">IsEqual</a>
</td>
<td align="left" width="63%">
Compares two table rows to determine if they have the same properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setalignment">SetAlignment</a>
</td>
<td align="left" width="63%">
Sets the horizontal alignment of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellalignment">SetCellAlignment</a>
</td>
<td align="left" width="63%">
Sets the vertical alignment of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellbordercolors">SetCellBorderColors</a>
</td>
<td align="left" width="63%">
Sets the border colors of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellborderwidths">SetCellBorderWidths</a>
</td>
<td align="left" width="63%">
Sets the border widths of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellcolorback">SetCellColorBack</a>
</td>
<td align="left" width="63%">
Sets the background color of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellcolorfore">SetCellColorFore</a>
</td>
<td align="left" width="63%">
Sets the foreground color of the active cell. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellcount">SetCellCount</a>
</td>
<td align="left" width="63%">
Sets the count of cells in a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellcountcache">SetCellCountCache</a>
</td>
<td align="left" width="63%">
Sets the count of cells cached for a row. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellindex">SetCellIndex</a>
</td>
<td align="left" width="63%">
Sets the index of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellmargin">SetCellMargin</a>
</td>
<td align="left" width="63%">
Sets the cell margin of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellmergeflags">SetCellMergeFlags</a>
</td>
<td align="left" width="63%">
Sets the merge flags of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellshading">SetCellShading</a>
</td>
<td align="left" width="63%">
Sets the shading of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellverticaltext">SetCellVerticalText</a>
</td>
<td align="left" width="63%">
Sets the vertical-text setting of the active cell. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellwidth">SetCellWidth</a>
</td>
<td align="left" width="63%">
Sets the active cell width in twips. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setheight">SetHeight</a>
</td>
<td align="left" width="63%">
Sets the height of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setindent">SetIndent</a>
</td>
<td align="left" width="63%">
Sets the indent of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setkeeptogether">SetKeepTogether</a>
</td>
<td align="left" width="63%">
Sets whether this row is allowed to be broken across pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setkeepwithnext">SetKeepWithNext</a>
</td>
<td align="left" width="63%">
Sets whether a row should appear on the same page as the row that follows it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setproperty">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setrtl">SetRTL</a>
</td>
<td align="left" width="63%">
Sets whether this row has right-to-left orientation.

</td>
</tr>
</table> 


## -remarks



To select a table, a row, or a cell, use <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange-expand">ITextRange::Expand</a>, with the <i>Unit</i> parameter set to <b>tomTable</b>, <b>tomRow</b>, or <b>tomCell</b>, respectively. These units can also be used with the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a> methods to navigate and select multiple rows or cells.

Some of the <b>ITextRow</b> properties apply to the whole row, such as the row alignment. In addition, there are a number of properties, such as cell alignment, that apply to a cell with the index set via the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-setcellindex">ITextRow::SetCellIndex</a> method. This cell is referred to as the active cell.


<b>ITextRow</b> works similarly to <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>, but doesn't modify the document until either the <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-apply">ITextRow::Apply</a> or <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-insert">ITextRow::Insert</a> methods are called. In addition, the row and cell parameters are always active, that is, they cannot have the value <b>tomDefault</b>.

On initialization, the <b>ITextRow</b> object acquires the table row properties, if any, at the active end of the associated <a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>. The <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrow-reset">ITextRow::Reset</a> method can be used to update these properties to the current values for <b>ITextRange2</b> object.


A rich edit control table consists of a sequence of table rows, which, in turn, consist of sequences of paragraphs. A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D. Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is. The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters. The cell parameters are stored in an expanded version of the tabs array. This format allows tables to be nested within other tables and is allowed to go fifteen levels deep.

The architecture is quite flexible in that each table row can have any valid table-row parameters, regardless of the parameters for other rows (except for vertical merge flags). For example, the number of cells and the start indents of table rows can differ, unlike in HTML which has n×m rectangular format with all rows starting at the same indent. 

On the other hand, no formal table description is stored anywhere. Information such as the number of rows must be figured out by navigating through the table.
For example, the count of rows in a table can be obtained by calling <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange-startof">ITextRange::StartOf</a> (<b>tomTable</b>, <b>tomFalse</b>, <b>NULL</b>) to move to the start of the current table and then calling <a href="https://docs.microsoft.com/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a> (<b>tomRow</b>, <b>tomForward</b>, <i>&amp;dcRow</i>). The quantity <i>&amp;dcRow</i> + 1 then contains the count of rows in the table, because moving by <b>tomRow</b> increments doesn't move beyond the last table row.


For additional information about the rich edit control's support for tables, see <a href="http://go.microsoft.com/fwlink/p/?linkid=239678">RichEdit's Nested Table Facility</a>. 




