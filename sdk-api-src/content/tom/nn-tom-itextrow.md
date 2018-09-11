---
UID: NN:tom.ITextRow
title: ITextRow
author: windows-sdk-content
description: The ITextRow interface provides methods to insert one or more identical table rows, and to retrieve and change table row properties. To insert nonidentical rows, call ITextRow::Insert for each different row configuration.
old-location: controls\itextrow.htm
tech.root: controls
ms.assetid: 49f5ffc1-d615-4d07-9f41-1c5f0dd9045b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextRow, ITextRow interface [Windows Controls], ITextRow interface [Windows Controls],described, controls.itextrow, tom/ITextRow
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
 - ITextRow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow interface


## -description


The <b>ITextRow</b> interface provides methods to insert one or more identical table rows, and to retrieve and change table row properties. To insert nonidentical rows, call <a href="https://msdn.microsoft.com/en-us/library/Hh768694(v=VS.85).aspx">ITextRow::Insert</a> for each different row configuration. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextRow</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITextRow</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f09f73d3-c71f-43f1-b671-aba392e1fb49">Apply</a>
</td>
<td align="left" width="63%">
Applies the formatting attributes of this text row object to the specified rows in the associated <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/721f3841-a50b-4569-b988-71a9fb96f16f">CanChange</a>
</td>
<td align="left" width="63%">
Determines whether changes can be made to this row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c7279b0-6329-4abd-a719-da4ed4d71c71">GetAlignment</a>
</td>
<td align="left" width="63%">
Gets the horizontal alignment of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/379d6fa5-ea73-4b72-9251-942f66925d8a">GetCellAlignment</a>
</td>
<td align="left" width="63%">
Gets the vertical alignment of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cc0a3b0-3988-4dff-9553-a86d37f4011f">GetCellBorderColors</a>
</td>
<td align="left" width="63%">
Gets the border colors of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0ab26ca-ffb6-4f75-846b-e267e4ad6572">GetCellBorderWidths</a>
</td>
<td align="left" width="63%">
Gets the border widths of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d199c4d7-17fd-4d1d-9d6d-b11db71f1363">GetCellColorBack</a>
</td>
<td align="left" width="63%">
Gets the background color of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/92c8bff3-a56b-4adc-9f49-728f22c1089b">GetCellColorFore</a>
</td>
<td align="left" width="63%">
Gets the foreground color of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4aae4fe5-5a54-4f32-9f89-01752701c871">GetCellCount</a>
</td>
<td align="left" width="63%">
Gets the count of cells in this row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e94abbcb-2a7a-4904-a832-0d2158d49010">GetCellCountCache</a>
</td>
<td align="left" width="63%">
Gets the count of cells cached for this row. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7768e073-929c-43a4-8c4f-a67f89a0e7ee">GetCellIndex</a>
</td>
<td align="left" width="63%">
Gets the index of the active cell to get or set parameters for.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc477a0f-2368-40c8-9b75-caec3afedea0">GetCellMargin</a>
</td>
<td align="left" width="63%">
Gets the cell margin of this row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e3c0cf4-b371-4622-a183-61d213fc9291">GetCellMergeFlags</a>
</td>
<td align="left" width="63%">
Gets the merge flags of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/450f97ea-b5b4-44e4-92b8-155c1a9c9c1b">GetCellShading</a>
</td>
<td align="left" width="63%">
Gets the shading of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c94a4af-0212-4422-bee2-7a9148a40b28">GetCellVerticalText</a>
</td>
<td align="left" width="63%">
Gets the vertical-text setting of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc73fdf4-29ce-4432-825d-725d61717b7a">GetCellWidth</a>
</td>
<td align="left" width="63%">
Gets the width of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6befda1a-1a47-4668-b0cf-4fd66e7b633d">GetHeight</a>
</td>
<td align="left" width="63%">
Gets the height of the row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9caea02f-f8db-4366-aea6-d40759b8f792">GetIndent</a>
</td>
<td align="left" width="63%">
Gets the indent of this row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f40c910-2636-4412-ae05-7a630c1f4806">GetKeepTogether</a>
</td>
<td align="left" width="63%">
Gets whether this row is allowed to be broken across pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67c5f06c-9f45-430b-ae9f-0ca1931df411">GetKeepWithNext</a>
</td>
<td align="left" width="63%">
Gets  whether this row should appear on the same page as the row that follows it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b689344-6748-49d7-aa98-a87435b7cb0b">GetNestLevel</a>
</td>
<td align="left" width="63%">
Gets the nest level of a table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed47033f-14b2-4ca1-89be-f2eab3d148ef">GetProperty</a>
</td>
<td align="left" width="63%">
Gets the value of the specified property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60261327-71f1-4bc3-97ac-b9c5ee3d44c0">GetRTL</a>
</td>
<td align="left" width="63%">
Gets whether this row has right-to-left orientation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b46a6391-7332-4cca-8199-d801a1e4c299">Insert</a>
</td>
<td align="left" width="63%">
Inserts a row, or rows, at the location identified by the associated <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e516a4d-0f3b-475b-969d-661662bfaeef">IsEqual</a>
</td>
<td align="left" width="63%">
Compares two table rows to determine if they have the same properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49f057ba-6376-496b-b0b0-97c6a00111c4">Reset</a>
</td>
<td align="left" width="63%">
Resets a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfcc900d-2bec-4314-a2c5-09f55e27a626">SetAlignment</a>
</td>
<td align="left" width="63%">
Sets the horizontal alignment of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd47cb2f-ddcf-4131-99fd-0981d3c4ec6f">SetCellAlignment</a>
</td>
<td align="left" width="63%">
Sets the vertical alignment of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a8762ba-a92b-46aa-99bc-57406a872174">SetCellBorderColors</a>
</td>
<td align="left" width="63%">
Sets the border colors of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/343270e6-8f92-4429-9350-4031ae8bb0e0">SetCellBorderWidths</a>
</td>
<td align="left" width="63%">
Sets the border widths of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e0a7bb6-e146-4e51-abc0-e89f9faed235">SetCellColorBack</a>
</td>
<td align="left" width="63%">
Sets the background color of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2eff9f39-b79d-4fcb-b8ee-ef067cff2c78">SetCellColorFore</a>
</td>
<td align="left" width="63%">
Sets the foreground color of the active cell. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2e1436a-ef36-41cd-9ea1-fb7abfad7631">SetCellCount</a>
</td>
<td align="left" width="63%">
Sets the count of cells in a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54b9a0a0-1822-4cd6-afef-8ed9403e750a">SetCellCountCache</a>
</td>
<td align="left" width="63%">
Sets the count of cells cached for a row. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b31ed10-f153-4614-ba96-95271fe4b218">SetCellIndex</a>
</td>
<td align="left" width="63%">
Sets the index of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/826be963-ccac-4bb3-b5e0-1df5554e1c8c">SetCellMargin</a>
</td>
<td align="left" width="63%">
Sets the cell margin of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a60966cc-03c6-4cb9-b424-eb59f68d1fd1">SetCellMergeFlags</a>
</td>
<td align="left" width="63%">
Sets the merge flags of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9163a9a3-6f8c-4318-a5a1-4b00a9037f6a">SetCellShading</a>
</td>
<td align="left" width="63%">
Sets the shading of the active cell.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa4c60c0-9c8f-4743-aff6-b87134ba2dd0">SetCellVerticalText</a>
</td>
<td align="left" width="63%">
Sets the vertical-text setting of the active cell. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/321c5255-9cd5-46ea-a592-165d288bc452">SetCellWidth</a>
</td>
<td align="left" width="63%">
Sets the active cell width in twips. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c377bdef-d906-4f7b-98f0-13633906ced9">SetHeight</a>
</td>
<td align="left" width="63%">
Sets the height of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9846fbd5-c210-49c4-8abe-dfb9cb85f7ae">SetIndent</a>
</td>
<td align="left" width="63%">
Sets the indent of a row.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca2130b4-3e29-43d7-b03d-a6c45897e447">SetKeepTogether</a>
</td>
<td align="left" width="63%">
Sets whether this row is allowed to be broken across pages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b73ca91-39a1-4dee-8414-57ee45653c07">SetKeepWithNext</a>
</td>
<td align="left" width="63%">
Sets whether a row should appear on the same page as the row that follows it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d43172b9-c717-41b2-ba22-aa164a595140">SetProperty</a>
</td>
<td align="left" width="63%">
Sets the value of the specified property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e260f989-6028-4cd2-a1e0-0eca2a5bd553">SetRTL</a>
</td>
<td align="left" width="63%">
Sets whether this row has right-to-left orientation.

</td>
</tr>
</table> 


## -remarks



To select a table, a row, or a cell, use <a href="https://msdn.microsoft.com/en-us/library/Bb787781(v=VS.85).aspx">ITextRange::Expand</a>, with the <i>Unit</i> parameter set to <b>tomTable</b>, <b>tomRow</b>, or <b>tomCell</b>, respectively. These units can also be used with the <a href="https://msdn.microsoft.com/en-us/library/Bb774064(v=VS.85).aspx">ITextRange::Move</a> methods to navigate and select multiple rows or cells.

Some of the <b>ITextRow</b> properties apply to the whole row, such as the row alignment. In addition, there are a number of properties, such as cell alignment, that apply to a cell with the index set via the <a href="https://msdn.microsoft.com/en-us/library/Hh768705(v=VS.85).aspx">ITextRow::SetCellIndex</a> method. This cell is referred to as the active cell.


<b>ITextRow</b> works similarly to <a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>, but doesn't modify the document until either the <a href="https://msdn.microsoft.com/en-us/library/Hh768671(v=VS.85).aspx">ITextRow::Apply</a> or <a href="https://msdn.microsoft.com/en-us/library/Hh768694(v=VS.85).aspx">ITextRow::Insert</a> methods are called. In addition, the row and cell parameters are always active, that is, they cannot have the value <b>tomDefault</b>.

On initialization, the <b>ITextRow</b> object acquires the table row properties, if any, at the active end of the associated <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>. The <a href="https://msdn.microsoft.com/en-us/library/Hh768696(v=VS.85).aspx">ITextRow::Reset</a> method can be used to update these properties to the current values for <b>ITextRange2</b> object.


A rich edit control table consists of a sequence of table rows, which, in turn, consist of sequences of paragraphs. A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D. Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is. The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters. The cell parameters are stored in an expanded version of the tabs array. This format allows tables to be nested within other tables and is allowed to go fifteen levels deep.

The architecture is quite flexible in that each table row can have any valid table-row parameters, regardless of the parameters for other rows (except for vertical merge flags). For example, the number of cells and the start indents of table rows can differ, unlike in HTML which has n×m rectangular format with all rows starting at the same indent. 

On the other hand, no formal table description is stored anywhere. Information such as the number of rows must be figured out by navigating through the table.
For example, the count of rows in a table can be obtained by calling <a href="https://msdn.microsoft.com/en-us/library/Bb787835(v=VS.85).aspx">ITextRange::StartOf</a> (<b>tomTable</b>, <b>tomFalse</b>, <b>NULL</b>) to move to the start of the current table and then calling <a href="https://msdn.microsoft.com/en-us/library/Bb774064(v=VS.85).aspx">ITextRange::Move</a> (<b>tomRow</b>, <b>tomForward</b>, <i>&amp;dcRow</i>). The quantity <i>&amp;dcRow</i> + 1 then contains the count of rows in the table, because moving by <b>tomRow</b> increments doesn't move beyond the last table row.


For additional information about the rich edit control's support for tables, see <a href="http://go.microsoft.com/fwlink/p/?linkid=239678">RichEdit's Nested Table Facility</a>. 




