---
UID: NN:tom.ITextRow
title: ITextRow (tom.h)
description: The ITextRow interface provides methods to insert one or more identical table rows, and to retrieve and change table row properties. To insert nonidentical rows, call ITextRow::Insert for each different row configuration.
helpviewer_keywords: ["ITextRow","ITextRow interface [Windows Controls]","ITextRow interface [Windows Controls]","described","controls.itextrow","tom/ITextRow"]
old-location: controls\itextrow.htm
tech.root: Controls
ms.assetid: 49f5ffc1-d615-4d07-9f41-1c5f0dd9045b
ms.date: 12/05/2018
ms.keywords: ITextRow, ITextRow interface [Windows Controls], ITextRow interface [Windows Controls],described, controls.itextrow, tom/ITextRow
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
 - ITextRow
 - tom/ITextRow
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
 - ITextRow
---

# ITextRow interface


## -description

The <b>ITextRow</b> interface provides methods to insert one or more identical table rows, and to retrieve and change table row properties. To insert nonidentical rows, call <a href="/windows/desktop/api/tom/nf-tom-itextrow-insert">ITextRow::Insert</a> for each different row configuration.

## -inheritance

The <b>ITextRow</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITextRow</b> also has these types of members:

## -remarks

To select a table, a row, or a cell, use <a href="/windows/desktop/api/tom/nf-tom-itextrange-expand">ITextRange::Expand</a>, with the <i>Unit</i> parameter set to <b>tomTable</b>, <b>tomRow</b>, or <b>tomCell</b>, respectively. These units can also be used with the <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a> methods to navigate and select multiple rows or cells.

Some of the <b>ITextRow</b> properties apply to the whole row, such as the row alignment. In addition, there are a number of properties, such as cell alignment, that apply to a cell with the index set via the <a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellindex">ITextRow::SetCellIndex</a> method. This cell is referred to as the active cell.


<b>ITextRow</b> works similarly to <a href="/windows/desktop/api/tom/nn-tom-itextpara2">ITextPara2</a>, but doesn't modify the document until either the <a href="/windows/desktop/api/tom/nf-tom-itextrow-apply">ITextRow::Apply</a> or <a href="/windows/desktop/api/tom/nf-tom-itextrow-insert">ITextRow::Insert</a> methods are called. In addition, the row and cell parameters are always active, that is, they cannot have the value <b>tomDefault</b>.

On initialization, the <b>ITextRow</b> object acquires the table row properties, if any, at the active end of the associated <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>. The <a href="/windows/desktop/api/tom/nf-tom-itextrow-reset">ITextRow::Reset</a> method can be used to update these properties to the current values for <b>ITextRange2</b> object.


A rich edit control table consists of a sequence of table rows, which, in turn, consist of sequences of paragraphs. A table row starts with the special two-character delimiter paragraph U+FFF9 U+000D and ends with the two-character delimiter paragraph U+FFFB U+000D. Each cell is terminated by the cell mark U+0007, which is treated as a hard end-of-paragraph mark just as U+000D (CR) is. The table row and cell parameters are treated as special paragraph formatting of the table-row delimiters. The cell parameters are stored in an expanded version of the tabs array. This format allows tables to be nested within other tables and is allowed to go fifteen levels deep.

The architecture is quite flexible in that each table row can have any valid table-row parameters, regardless of the parameters for other rows (except for vertical merge flags). For example, the number of cells and the start indents of table rows can differ, unlike in HTML which has n×m rectangular format with all rows starting at the same indent. 

On the other hand, no formal table description is stored anywhere. Information such as the number of rows must be figured out by navigating through the table.
For example, the count of rows in a table can be obtained by calling <a href="/windows/desktop/api/tom/nf-tom-itextrange-startof">ITextRange::StartOf</a> (<b>tomTable</b>, <b>tomFalse</b>, <b>NULL</b>) to move to the start of the current table and then calling <a href="/windows/desktop/api/tom/nf-tom-itextrange-move">ITextRange::Move</a> (<b>tomRow</b>, <b>tomForward</b>, <i>&amp;dcRow</i>). The quantity <i>&amp;dcRow</i> + 1 then contains the count of rows in the table, because moving by <b>tomRow</b> increments doesn't move beyond the last table row.
