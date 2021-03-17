---
UID: NS:richedit._tableRowParms
title: TABLEROWPARMS (richedit.h)
description: Defines the attributes of rows in a table.
helpviewer_keywords: ["PFA_CENTER","PFA_LEFT","PFA_RIGHT","TABLEROWPARMS","TABLEROWPARMS structure [Windows Controls]","controls.tablerowparms","richedit/TABLEROWPARMS"]
old-location: controls\tablerowparms.htm
tech.root: Controls
ms.assetid: 8b538d72-1210-4344-b673-592ef9a8cc85
ms.date: 12/05/2018
ms.keywords: PFA_CENTER, PFA_LEFT, PFA_RIGHT, TABLEROWPARMS, TABLEROWPARMS structure [Windows Controls], controls.tablerowparms, richedit/TABLEROWPARMS
req.header: richedit.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TABLEROWPARMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tableRowParms
 - richedit/_tableRowParms
 - TABLEROWPARMS
 - richedit/TABLEROWPARMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Richedit.h
api_name:
 - TABLEROWPARMS
---

# TABLEROWPARMS structure


## -description

Defines the attributes of rows in a table. The definitions include the corresponding Rich Text Format (RTF) control words, which are defined in the Rich Text Format (RTF) Specification.

## -struct-fields

### -field cbRow

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The count of bytes in this structure.

### -field cbCell

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The count of bytes in <a href="/windows/desktop/api/richedit/ns-richedit-tablecellparms">TABLECELLPARMS</a>.

### -field cCell

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The count of cells in a row, up to the maximum specified by MAX_TABLE_CELLS.

### -field cRow

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The count of rows.

### -field dxCellMargin

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The size of the left and right margins in a cell (\trgaph).

### -field dxIndent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The amount of left indentation, or right indentation if the <b>fRTL</b> member is <b>TRUE</b> (similar to \trleft).

### -field dyHeight

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The height of a row (\trrh).

### -field nAlignment

### -field fRTL

### -field fKeep

### -field fKeepFollow

### -field fWrap

### -field fIdentCells

### -field cpStartRow

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The character position that indicates where to insert table. A value of –1 indicates the character position of the selection.

### -field bTableLevel

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The table nesting level (<a href="/windows/desktop/Controls/em-gettableparms">EM_GETTABLEPARMS</a> only).

### -field iCell

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

The index of the cell to insert or delete (<a href="/windows/desktop/Controls/em-settableparms">EM_SETTABLEPARMS</a> only).

### -field fIdentCells:1

Type: <b>DWORD</b>

 Indent cells.

### -field fKeep:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Keep rows together (\trkeep).

### -field fKeepFollow:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Keep the row on the same page as the following row (\trkeepfollow).

### -field fRTL:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Display cells in right-to-left order (\rtlrow).

### -field fWrap:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Wrap text to the right or left, depending on <b>bAlignment</b>(see \tdfrmtxtLeftN and \tdfrmtxtRightN).

### -field nAlignment:3

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>


Row alignment \trql, trqr, \trqc)



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PFA_CENTER"></a><a id="pfa_center"></a><dl>
<dt><b>PFA_CENTER</b></dt>
</dl>
</td>
<td width="60%">
The rows are centered.

</td>
</tr>
<tr>
<td width="40%"><a id="PFA_LEFT"></a><a id="pfa_left"></a><dl>
<dt><b>PFA_LEFT</b></dt>
</dl>
</td>
<td width="60%">
The rows are aligned with the left margin.

</td>
</tr>
<tr>
<td width="40%"><a id="PFA_RIGHT"></a><a id="pfa_right"></a><dl>
<dt><b>PFA_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
The rows are aligned with the right margin.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Controls/em-inserttable">EM_INSERTTABLE</a>



<a href="/windows/desktop/api/richedit/ns-richedit-tablecellparms">TABLECELLPARMS</a>