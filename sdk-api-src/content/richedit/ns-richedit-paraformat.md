---
UID: NS:richedit._paraformat
title: PARAFORMAT (richedit.h)
description: Contains information about paragraph formatting attributes in a rich edit control. (PARAFORMAT)
helpviewer_keywords: ["0","1","2","3","4","5","PARAFORMAT","PARAFORMAT structure [Windows Controls]","PFA_CENTER","PFA_LEFT","PFA_RIGHT","PFE_RLTPARA","PFM_ALIGNMENT","PFM_NUMBERING","PFM_OFFSET","PFM_OFFSETINDENT","PFM_RIGHTINDENT","PFM_RTLPARA","PFM_STARTINDENT","PFM_TABSTOPS","_win32_PARAFORMAT_str","_win32_PARAFORMAT_str_cpp","controls.PARAFORMAT","controls._win32_PARAFORMAT_str","richedit/PARAFORMAT"]
old-location: controls\PARAFORMAT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\paraformat.htm
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 3, 4, 5, PARAFORMAT, PARAFORMAT structure [Windows Controls], PFA_CENTER, PFA_LEFT, PFA_RIGHT, PFE_RLTPARA, PFM_ALIGNMENT, PFM_NUMBERING, PFM_OFFSET, PFM_OFFSETINDENT, PFM_RIGHTINDENT, PFM_RTLPARA, PFM_STARTINDENT, PFM_TABSTOPS, _win32_PARAFORMAT_str, _win32_PARAFORMAT_str_cpp, controls.PARAFORMAT, controls._win32_PARAFORMAT_str, richedit/PARAFORMAT
req.header: richedit.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PARAFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _paraformat
 - richedit/_paraformat
 - PARAFORMAT
 - richedit/PARAFORMAT
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
 - PARAFORMAT
---

# PARAFORMAT structure


## -description

Contains information about paragraph formatting attributes in a rich edit control. This structure is used with the <a href="/windows/win32/controls/em-getparaformat">EM_GETPARAFORMAT</a> and <a href="/windows/win32/controls/em-setparaformat">EM_SETPARAFORMAT</a> messages.
        

In Microsoft Rich Edit 2.0, the <a href="/windows/win32/api/richedit/ns-richedit-paraformat2">PARAFORMAT2</a> structure is a Microsoft Rich Edit 2.0 extension of the <b>PARAFORMAT</b> structure. Microsoft Rich Edit 2.0 allows you to use either structure with <a href="/windows/win32/controls/em-getparaformat">EM_GETPARAFORMAT</a> and <a href="/windows/win32/controls/em-setparaformat">EM_SETPARAFORMAT</a>.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Structure size, in bytes. The member must be filled before passing to the rich edit control.

### -field dwMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Members containing valid information or attributes to set. This parameter can be none or a combination of the following values. If both PFM_STARTINDENT and PFM_OFFSETINDENT are specified, PFM_STARTINDENT takes precedence. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PFM_ALIGNMENT"></a><a id="pfm_alignment"></a><dl>
<dt><b>PFM_ALIGNMENT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>wAlignment</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_NUMBERING"></a><a id="pfm_numbering"></a><dl>
<dt><b>PFM_NUMBERING</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>wNumbering</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_OFFSET"></a><a id="pfm_offset"></a><dl>
<dt><b>PFM_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>dxOffset</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_OFFSETINDENT"></a><a id="pfm_offsetindent"></a><dl>
<dt><b>PFM_OFFSETINDENT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>dxStartIndent</b> member is valid and specifies a relative value.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_RIGHTINDENT"></a><a id="pfm_rightindent"></a><dl>
<dt><b>PFM_RIGHTINDENT</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>dxRightIndent</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_RTLPARA"></a><a id="pfm_rtlpara"></a><dl>
<dt><b>PFM_RTLPARA</b></dt>
</dl>
</td>
<td width="60%">
<b>Rich Edit 2.0:</b> The <b>wEffects</b> member is valid

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_STARTINDENT"></a><a id="pfm_startindent"></a><dl>
<dt><b>PFM_STARTINDENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>dxStartIndent</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_TABSTOPS"></a><a id="pfm_tabstops"></a><dl>
<dt><b>PFM_TABSTOPS</b></dt>
</dl>
</td>
<td width="60%">
The <i>cTabStobs</i> and <i>rgxTabStops</i> members are valid.

</td>
</tr>
</table>

### -field wNumbering

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Value specifying numbering options. This member can be zero or PFN_BULLET.

### -field wReserved

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

<b>Rich Edit 1.0:</b>: This member is named <b>wReserved</b>. Reserved; the value must be zero. 
                

<b>Rich Edit 2.0:</b> This member is named <b>wEffects</b>. A bit flag that specifies a paragraph effect. It is included only for compatibility with TOM interfaces; the rich edit control stores the value but does not use it to display the text. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Displays text using left-to-right reading order. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_RLTPARA"></a><a id="pfe_rltpara"></a><dl>
<dt><b>PFE_RLTPARA</b></dt>
</dl>
</td>
<td width="60%">
Displays text using right-to-left reading order.

</td>
</tr>
</table>

### -field wEffects

### -field dxStartIndent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Indentation of the first line in the paragraph, in twips. If the paragraph formatting is being set and PFM_OFFSETINDENT is specified, this member is treated as a relative value that is added to the starting indentation of each affected paragraph.

### -field dxRightIndent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Size, of the right indentation relative to the right margin, in twips.

### -field dxOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Indentation of the second and subsequent lines of a paragraph relative to the starting indentation, in twips. The first line is indented if this member is negative or outdented if this member is positive.

### -field wAlignment

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Value specifying the paragraph alignment. This member can be one of the following values. 

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
Paragraphs are centered.

</td>
</tr>
<tr>
<td width="40%"><a id="PFA_LEFT"></a><a id="pfa_left"></a><dl>
<dt><b>PFA_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Paragraphs are aligned with the left margin.

</td>
</tr>
<tr>
<td width="40%"><a id="PFA_RIGHT"></a><a id="pfa_right"></a><dl>
<dt><b>PFA_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Paragraphs are aligned with the right margin.

</td>
</tr>
</table>

### -field cTabCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Number of tab stops.

### -field rgxTabs

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Array of absolute tab stop positions. Each element in the array specifies information about a tab stop. The 24 low-order bits specify the absolute offset, in twips. To use this member, set the PFM_TABSTOPS flag in the 
					<b>dwMask</b> member.
                    

<b>Rich Edit 2.0:</b> For compatibility with TOM interfaces, you can use the eight high-order bits to store additional information about each tab stop. 


Bits 24-27 can specify one of the following values to indicate the tab alignment. These bits do not affect the rich edit control display for versions earlier than Microsoft Rich Edit 3.0. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Ordinary tab

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Center tab

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Right-aligned tab

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Decimal tab

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
Word bar tab (vertical bar)

</td>
</tr>
</table>
 


Bits 28-31 can specify one of the following values to indicate the type of tab leader. These bits do not affect the rich edit control display.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
No leader

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Dotted leader

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Dashed leader

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Underlined leader

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
Thick line leader

</td>
</tr>
<tr>
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">
Double line leader

</td>
</tr>
</table>

## -see-also

<a href="/windows/win32/controls/em-getparaformat">EM_GETPARAFORMAT</a>



<a href="/windows/win32/controls/em-setparaformat">EM_SETPARAFORMAT</a>



<a href="/windows/win32/api/richedit/ns-richedit-paraformat2">PARAFORMAT2</a>



<b>Reference</b>
