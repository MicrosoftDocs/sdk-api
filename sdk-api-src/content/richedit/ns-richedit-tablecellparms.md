---
UID: NS:richedit._tableCellParms
title: TABLECELLPARMS (richedit.h)
description: Defines the attributes of cells in a table row.
helpviewer_keywords: ["TABLECELLPARMS","TABLECELLPARMS structure [Windows Controls]","controls.tablecellparms","richedit/TABLECELLPARMS"]
old-location: controls\tablecellparms.htm
tech.root: Controls
ms.assetid: 75bf07bd-103b-4f35-b421-5a7559c7b90e
ms.date: 12/05/2018
ms.keywords: TABLECELLPARMS, TABLECELLPARMS structure [Windows Controls], controls.tablecellparms, richedit/TABLECELLPARMS
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
req.typenames: TABLECELLPARMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tableCellParms
 - richedit/_tableCellParms
 - TABLECELLPARMS
 - richedit/TABLECELLPARMS
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
 - TABLECELLPARMS
---

# TABLECELLPARMS structure


## -description

Defines the attributes of cells in a table row. The definitions include the corresponding Rich Text Format (RTF) control words, which are defined in the Rich Text Format (RTF) Specification.

## -struct-fields

### -field dxWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The width of a cell (\cellx).

### -field nVertAlign

### -field fMergeTop

### -field fMergePrev

### -field fVertical

### -field fMergeStart

### -field fMergeCont

### -field wShading

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Shading in .01% (\clshdng). This controls the amount of pattern foreground color (<b>crForePat</b>) and pattern background color (<b>crBackPat</b>) that is used to create the cell background color. If <b>wShading</b> is 0, the cell background is <b>crBackPat</b>. If it's 10000, the cell background is <b>crForePat</b>. Values of <b>wShading</b> in between are mixtures of the two pattern colors.

### -field dxBrdrLeft

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Left border width, in twips  (\clbrdrl\brdrwN).

### -field dyBrdrTop

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Top border width (\clbrdrt\brdrwN).

### -field dxBrdrRight

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Right border width (\clbrdrr\brdrwN).

### -field dyBrdrBottom

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Bottom border width (\clbrdrb\brdrwN).

### -field crBrdrLeft

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

Left border color (\clbrdrl\brdrcf).

### -field crBrdrTop

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

Top border color (\clbrdrt\brdrcf).

### -field crBrdrRight

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

Right border color (\clbrdrr\brdrcf).

### -field crBrdrBottom

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

Bottom border color (\clbrdrb\brdrcf).

### -field crBackPat

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

Background color (\clcbpat).

### -field crForePat

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

Foreground color (\clcfpat).

### -field fMergeCont:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Merge with the previous cell (\clmrg).

### -field fMergePrev:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Merge with the cell above (\clvmrg).

### -field fMergeStart:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Start set of horizontally merged cells (\clmgf).

### -field fMergeTop:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Top cell for vertical merge (\clvmgf).

### -field fVertical:1

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Display text top to bottom, right to left (\cltxtbrlv).

### -field nVertAlign:2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>


The vertical alignment of cells (\clvertalt (def), \clvertalc, \clvertalb). It can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The content appears at the top of a cell. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The content is centered in the cell.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The content appears at the bottom of a cell. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Controls/em-inserttable">EM_INSERTTABLE</a>



<a href="/windows/desktop/api/richedit/ns-richedit-tablerowparms">TABLEROWPARMS</a>