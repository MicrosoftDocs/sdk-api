---
UID: NS:richedit.PARAFORMAT2
title: PARAFORMAT2 (richedit.h)
description: Contains information about paragraph formatting attributes in a rich edit control. (PARAFORMAT2)
helpviewer_keywords: ["0","1","10","11","12","13","14","15","16","2","3","32","4","5","6","64","7","8","9","PARAFORMAT2","PARAFORMAT2 structure [Windows Controls]","PFA_CENTER","PFA_FULL_INTERWORD","PFA_JUSTIFY","PFA_LEFT","PFA_RIGHT","PFE_DONOTHYPHEN","PFE_KEEP","PFE_KEEPNEXT","PFE_NOLINENUMBER","PFE_NOWIDOWCONTROL","PFE_PAGEBREAKBEFORE","PFE_RTLPARA","PFE_SIDEBYSIDE","PFE_TABLE","PFE_TABLEROWDELIMITER","PFM_ALIGNMENT","PFM_ALL","PFM_ALL2","PFM_BORDER","PFM_DONOTHYPHEN","PFM_EFFECTS","PFM_KEEP","PFM_KEEPNEXT","PFM_LINESPACING","PFM_NOLINENUMBER","PFM_NOWIDOWCONTROL","PFM_NUMBERING","PFM_NUMBERINGSTART","PFM_NUMBERINGSTYLE","PFM_NUMBERINGTAB","PFM_OFFSET","PFM_OFFSETINDENT","PFM_OUTLINELEVEL","PFM_PAGEBREAKBEFORE","PFM_RIGHTINDENT","PFM_RTLPARA","PFM_SHADING","PFM_SIDEBYSIDE","PFM_SPACEAFTER","PFM_SPACEBEFORE","PFM_STARTINDENT","PFM_STYLE","PFM_TABLE","PFM_TABLEROWDELIMITER","PFM_TABSTOPS","PFNS_NEWNUMBER","PFNS_NONUMBER","PFNS_PAREN","PFNS_PARENS","PFNS_PERIOD","PFNS_PLAIN","PFN_ARABIC","PFN_BULLET","PFN_LCLETTER","PFN_LCROMAN","PFN_UCLETTER","PFN_UCROMAN","_win32_PARAFORMAT2_str","_win32_PARAFORMAT2_str_cpp","controls.PARAFORMAT2","controls._win32_PARAFORMAT2_str","richedit/PARAFORMAT2","zero"]
old-location: controls\PARAFORMAT2.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditstructures\paraformat2.htm
ms.date: 12/05/2018
ms.keywords: 0, 1, 10, 11, 12, 13, 14, 15, 16, 2, 3, 32, 4, 5, 6, 64, 7, 8, 9, PARAFORMAT2, PARAFORMAT2 structure [Windows Controls], PFA_CENTER, PFA_FULL_INTERWORD, PFA_JUSTIFY, PFA_LEFT, PFA_RIGHT, PFE_DONOTHYPHEN, PFE_KEEP, PFE_KEEPNEXT, PFE_NOLINENUMBER, PFE_NOWIDOWCONTROL, PFE_PAGEBREAKBEFORE, PFE_RTLPARA, PFE_SIDEBYSIDE, PFE_TABLE, PFE_TABLEROWDELIMITER, PFM_ALIGNMENT, PFM_ALL, PFM_ALL2, PFM_BORDER, PFM_DONOTHYPHEN, PFM_EFFECTS, PFM_KEEP, PFM_KEEPNEXT, PFM_LINESPACING, PFM_NOLINENUMBER, PFM_NOWIDOWCONTROL, PFM_NUMBERING, PFM_NUMBERINGSTART, PFM_NUMBERINGSTYLE, PFM_NUMBERINGTAB, PFM_OFFSET, PFM_OFFSETINDENT, PFM_OUTLINELEVEL, PFM_PAGEBREAKBEFORE, PFM_RIGHTINDENT, PFM_RTLPARA, PFM_SHADING, PFM_SIDEBYSIDE, PFM_SPACEAFTER, PFM_SPACEBEFORE, PFM_STARTINDENT, PFM_STYLE, PFM_TABLE, PFM_TABLEROWDELIMITER, PFM_TABSTOPS, PFNS_NEWNUMBER, PFNS_NONUMBER, PFNS_PAREN, PFNS_PARENS, PFNS_PERIOD, PFNS_PLAIN, PFN_ARABIC, PFN_BULLET, PFN_LCLETTER, PFN_LCROMAN, PFN_UCLETTER, PFN_UCROMAN, _win32_PARAFORMAT2_str, _win32_PARAFORMAT2_str_cpp, controls.PARAFORMAT2, controls._win32_PARAFORMAT2_str, richedit/PARAFORMAT2, zero
f1_keywords:
- richedit/PARAFORMAT2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Richedit.h
api_name:
- PARAFORMAT2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PARAFORMAT2 structure overview


## -description


Contains information about paragraph formatting attributes in a rich edit control. <b>PARAFORMAT2</b> is a Microsoft Rich Edit 2.0 extension of the <a href="/windows/win32/api/richedit/ns-richedit-paraformat">PARAFORMAT</a> structure. Microsoft Rich Edit 2.0 allows you to use either structure with the <a href="/windows/win32/controls/em-getparaformat">EM_GETPARAFORMAT</a> and <a href="/windows/win32/controls/em-setparaformat">EM_SETPARAFORMAT</a> messages. 


## -struct-fields




### -field dySpaceBefore

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Size of the spacing above the paragraph, in twips. To use this member, set the PFM_SPACEBEFORE flag in the 
					<b>dwMask</b> member. The value must be greater than or equal to zero. 


### -field dySpaceAfter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Specifies the size of the spacing below the paragraph, in twips. To use this member, set the PFM_SPACEAFTER flag in the 
					<b>dwMask</b> member. The value must be greater than or equal to zero. 


### -field dyLineSpacing

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Spacing between lines. For a description of how this value is interpreted, see the 
					<b>bLineSpacingRule</b> member. To use this member, set the PFM_LINESPACING flag in the 
					<b>dwMask</b> member. 


### -field sStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Text style. To use this member, set the PFM_STYLE flag in the 
					<b>dwMask</b> member. This member is included only for compatibility with TOM interfaces and Word; the rich edit control stores the value but does not use it to display the text. 


### -field bLineSpacingRule

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Type of line spacing. To use this member, set the PFM_LINESPACING flag in the 
					<b>dwMask</b> member. This member can be one of the following values. 

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
Single spacing. The 
						<b>dyLineSpacing</b> member is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
One-and-a-half spacing. The 
						<b>dyLineSpacing</b> member is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Double spacing. The 
						<b>dyLineSpacing</b> member is ignored.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>dyLineSpacing</b> member specifies the spacingfrom one line to the next, in twips. However, if 
						<b>dyLineSpacing</b> specifies a value that is less than single spacing, the control displays single-spaced text.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>dyLineSpacing</b> member specifies the spacing from one line to the next, in twips. The control uses the exact spacing specified, even if 
						<b>dyLineSpacing</b> specifies a value that is less than single spacing.

</td>
</tr>
<tr>
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">
The value of 
						<b>dyLineSpacing</b> / 20 is the spacing, in lines, from one line to the next. Thus, setting 
						<b>dyLineSpacing</b> to 20 produces single-spaced text, 40 is double spaced, 60 is triple spaced, and so on.

</td>
</tr>
</table>
 


### -field bOutlineLevel

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a></b>

Reserved; must be zero. 


### -field wShadingWeight

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Percentage foreground color used in shading. The 
					<b>wShadingStyle</b> member specifies the foreground and background shading colors. A value of 5 indicates a shading color consisting of 5 percent foreground color and 95 percent background color. To use these members, set the PFM_SHADING flag in the 
					<b>dwMask</b> member. This member is included only for compatibility with Word; the rich edit control stores the value but does not use it to display the text. 


### -field wShadingStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Style and colors used for background shading. Bits 0 to 3 contain the shading style, bits 4 to 7 contain the foreground color index, and bits 8 to 11 contain the background color index. To use this member, set the PFM_SHADING flag in the 
					<b>dwMask</b> member. This member is included only for compatibility with Word; the rich edit control stores the value but does not use it to display the text. 


The shading style can be one of the following values.



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
None

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Dark horizontal

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Dark vertical

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Dark down diagonal

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
Dark up diagonal

</td>
</tr>
<tr>
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">
Dark grid

</td>
</tr>
<tr>
<td width="40%"><a id="6"></a><dl>
<dt><b>6</b></dt>
</dl>
</td>
<td width="60%">
Dark trellis

</td>
</tr>
<tr>
<td width="40%"><a id="7"></a><dl>
<dt><b>7</b></dt>
</dl>
</td>
<td width="60%">
Light horizontal

</td>
</tr>
<tr>
<td width="40%"><a id="8"></a><dl>
<dt><b>8</b></dt>
</dl>
</td>
<td width="60%">
Light vertical

</td>
</tr>
<tr>
<td width="40%"><a id="9"></a><dl>
<dt><b>9</b></dt>
</dl>
</td>
<td width="60%">
Light down diagonal

</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
Light up diagonal

</td>
</tr>
<tr>
<td width="40%"><a id="11"></a><dl>
<dt><b>11</b></dt>
</dl>
</td>
<td width="60%">
Light grid

</td>
</tr>
<tr>
<td width="40%"><a id="12"></a><dl>
<dt><b>12</b></dt>
</dl>
</td>
<td width="60%">
Light trellis

</td>
</tr>
</table>
 


The foreground and background color indexes can be one of the following values.



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
Black

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Blue

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Cyan

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Green

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
Magenta

</td>
</tr>
<tr>
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">
Red

</td>
</tr>
<tr>
<td width="40%"><a id="6"></a><dl>
<dt><b>6</b></dt>
</dl>
</td>
<td width="60%">
Yellow

</td>
</tr>
<tr>
<td width="40%"><a id="7"></a><dl>
<dt><b>7</b></dt>
</dl>
</td>
<td width="60%">
White

</td>
</tr>
<tr>
<td width="40%"><a id="8"></a><dl>
<dt><b>8</b></dt>
</dl>
</td>
<td width="60%">
Dark blue

</td>
</tr>
<tr>
<td width="40%"><a id="9"></a><dl>
<dt><b>9</b></dt>
</dl>
</td>
<td width="60%">
Dark cyan

</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
Dark green

</td>
</tr>
<tr>
<td width="40%"><a id="11"></a><dl>
<dt><b>11</b></dt>
</dl>
</td>
<td width="60%">
Dark magenta

</td>
</tr>
<tr>
<td width="40%"><a id="12"></a><dl>
<dt><b>12</b></dt>
</dl>
</td>
<td width="60%">
Dark red

</td>
</tr>
<tr>
<td width="40%"><a id="13"></a><dl>
<dt><b>13</b></dt>
</dl>
</td>
<td width="60%">
Dark yellow

</td>
</tr>
<tr>
<td width="40%"><a id="14"></a><dl>
<dt><b>14</b></dt>
</dl>
</td>
<td width="60%">
Dark gray

</td>
</tr>
<tr>
<td width="40%"><a id="15"></a><dl>
<dt><b>15</b></dt>
</dl>
</td>
<td width="60%">
Light gray

</td>
</tr>
</table>
 


### -field wNumberingStart

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Starting number or Unicode value used for numbered paragraphs. Use this member in conjunction with the 
					<b>wNumbering</b> member. This member is included only for compatibility with TOM interfaces; the rich edit control stores the value but does not use it to display the text or bullets. To use this member, set the PFM_NUMBERINGSTART flag in the 
					<b>dwMask</b> member. 


### -field wNumberingStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Numbering style used with numbered paragraphs. Use this member in conjunction with the 
					<b>wNumbering</b> member. This member is included only for compatibility with TOM interfaces; the rich edit control stores the value but rich edit versions earlier than 3.0 do not use it to display the text or bullets. To use this member, set the PFM_NUMBERINGSTYLE flag in the 
					<b>dwMask</b> member. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PFNS_PAREN"></a><a id="pfns_paren"></a><dl>
<dt><b>PFNS_PAREN</b></dt>
</dl>
</td>
<td width="60%">
Follows the number with a right parenthesis.

</td>
</tr>
<tr>
<td width="40%"><a id="PFNS_PARENS"></a><a id="pfns_parens"></a><dl>
<dt><b>PFNS_PARENS</b></dt>
</dl>
</td>
<td width="60%">
Encloses the number in parentheses.

</td>
</tr>
<tr>
<td width="40%"><a id="PFNS_PERIOD"></a><a id="pfns_period"></a><dl>
<dt><b>PFNS_PERIOD</b></dt>
</dl>
</td>
<td width="60%">
Follows the number with a period.

</td>
</tr>
<tr>
<td width="40%"><a id="PFNS_PLAIN"></a><a id="pfns_plain"></a><dl>
<dt><b>PFNS_PLAIN</b></dt>
</dl>
</td>
<td width="60%">
Displays only the number.

</td>
</tr>
<tr>
<td width="40%"><a id="PFNS_NONUMBER"></a><a id="pfns_nonumber"></a><dl>
<dt><b>PFNS_NONUMBER</b></dt>
</dl>
</td>
<td width="60%">
Continues a numbered list without applying the next number or bullet. 

</td>
</tr>
<tr>
<td width="40%"><a id="PFNS_NEWNUMBER"></a><a id="pfns_newnumber"></a><dl>
<dt><b>PFNS_NEWNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Starts a new number with 
						<b>wNumberingStart</b>.

</td>
</tr>
</table>
 


### -field wNumberingTab

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Minimum space between a paragraph number and the paragraph text, in twips. Use this member in conjunction with the 
					<b>wNumbering</b> member. The 
					<b>wNumberingTab</b> member is included for compatibility with TOM interfaces; previous to Microsoft Rich Edit 3.0, the rich edit control stores the value but does not use it to display text. To use this member, set the PFM_NUMBERINGTAB flag in the 
					<b>dwMask</b> member. 


### -field wBorderSpace

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

The space between the border and the paragraph text, in twips. The 
					<b>wBorderSpace</b> member is included for compatibility with Word; the rich edit control stores the values but does not use them to display text. To use this member, set the PFM_BORDER flag in the 
					<b>dwMask</b> member. 


### -field wBorderWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Border width, in twips. To use this member, set the PFM_BORDER flag in the 
					<b>dwMask</b> member. 


### -field wBorders

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Border location, style, and color. Bits 0 to 7 specify the border locations, bits 8 to 11 specify the border style, and bits 12 to 15 specify the border color index. To use this member, set the PFM_BORDER flag in the 
					<b>dwMask</b> member.


Specify the border locations using a combination of the following values in bits 0 to 7. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Left border.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Right border.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
Top border.

</td>
</tr>
<tr>
<td width="40%"><a id="8"></a><dl>
<dt><b>8</b></dt>
</dl>
</td>
<td width="60%">
Bottom border.

</td>
</tr>
<tr>
<td width="40%"><a id="16"></a><dl>
<dt><b>16</b></dt>
</dl>
</td>
<td width="60%">
Inside borders.

</td>
</tr>
<tr>
<td width="40%"><a id="32"></a><dl>
<dt><b>32</b></dt>
</dl>
</td>
<td width="60%">
Outside borders.

</td>
</tr>
<tr>
<td width="40%"><a id="64"></a><dl>
<dt><b>64</b></dt>
</dl>
</td>
<td width="60%">
Autocolor. If this bit is set, the color index in bits 12 to 15 is not used.

</td>
</tr>
</table>
 


Specify the border style using one of the following values for bits 8 to 11. 



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
None

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
<b>3</b>/<b>4</b> point

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
1<b>1</b>/<b>2</b> point

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
2<b>1</b>/<b>4</b> point

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
3 point

</td>
</tr>
<tr>
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">
4<b>1</b>/<b>2</b> point

</td>
</tr>
<tr>
<td width="40%"><a id="6"></a><dl>
<dt><b>6</b></dt>
</dl>
</td>
<td width="60%">
6 point

</td>
</tr>
<tr>
<td width="40%"><a id="7"></a><dl>
<dt><b>7</b></dt>
</dl>
</td>
<td width="60%">
<b>3</b>/<b>4</b> point double

</td>
</tr>
<tr>
<td width="40%"><a id="8"></a><dl>
<dt><b>8</b></dt>
</dl>
</td>
<td width="60%">
1<b>1</b>/<b>2</b> point double

</td>
</tr>
<tr>
<td width="40%"><a id="9"></a><dl>
<dt><b>9</b></dt>
</dl>
</td>
<td width="60%">
2<b>1</b>/<b>4</b> point double

</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
<b>3</b>/<b>4</b> point gray

</td>
</tr>
<tr>
<td width="40%"><a id="11"></a><dl>
<dt><b>11</b></dt>
</dl>
</td>
<td width="60%">
<b>3</b>/<b>4</b> point gray dashed

</td>
</tr>
</table>
 


Specify the border color using one of the following values for bits 12 to 15. This value is ignored if the autocolor bit (bit 6) is set. 



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
Black

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Blue

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Cyan

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Green

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
</dl>
</td>
<td width="60%">
Magenta

</td>
</tr>
<tr>
<td width="40%"><a id="5"></a><dl>
<dt><b>5</b></dt>
</dl>
</td>
<td width="60%">
Red

</td>
</tr>
<tr>
<td width="40%"><a id="6"></a><dl>
<dt><b>6</b></dt>
</dl>
</td>
<td width="60%">
Yellow

</td>
</tr>
<tr>
<td width="40%"><a id="7"></a><dl>
<dt><b>7</b></dt>
</dl>
</td>
<td width="60%">
White

</td>
</tr>
<tr>
<td width="40%"><a id="8"></a><dl>
<dt><b>8</b></dt>
</dl>
</td>
<td width="60%">
Dark blue

</td>
</tr>
<tr>
<td width="40%"><a id="9"></a><dl>
<dt><b>9</b></dt>
</dl>
</td>
<td width="60%">
Dark cyan

</td>
</tr>
<tr>
<td width="40%"><a id="10"></a><dl>
<dt><b>10</b></dt>
</dl>
</td>
<td width="60%">
Dark green

</td>
</tr>
<tr>
<td width="40%"><a id="11"></a><dl>
<dt><b>11</b></dt>
</dl>
</td>
<td width="60%">
Dark magenta

</td>
</tr>
<tr>
<td width="40%"><a id="12"></a><dl>
<dt><b>12</b></dt>
</dl>
</td>
<td width="60%">
Dark red

</td>
</tr>
<tr>
<td width="40%"><a id="13"></a><dl>
<dt><b>13</b></dt>
</dl>
</td>
<td width="60%">
Dark yellow

</td>
</tr>
<tr>
<td width="40%"><a id="14"></a><dl>
<dt><b>14</b></dt>
</dl>
</td>
<td width="60%">
Dark gray

</td>
</tr>
<tr>
<td width="40%"><a id="15"></a><dl>
<dt><b>15</b></dt>
</dl>
</td>
<td width="60%">
Light gray

</td>
</tr>
</table>
 


### -field _paraformat

 




### -field cTabCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SHORT</a></b>

Number of tab stops defined in the 
					<b>rgxTabs</b> array.


### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Structure size, in bytes. Before passing this structure to a rich edit control, set <b>cbSize</b> to the size of the <a href="/windows/win32/api/richedit/ns-richedit-paraformat">PARAFORMAT</a> or <b>PARAFORMAT2</b> structure. If <b>cbSize</b> equals the size of a <b>PARAFORMAT</b> structure, the control uses only the <b>PARAFORMAT</b> members. 


### -field dwMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The members of the <b>PARAFORMAT2</b> structure that contain valid information. The 
					<b>dwMask</b> member can be a combination of the values from two sets of bit flags. One set indicates the structure members that are valid; another set indicates the valid attributes in the 
					<b>wEffects</b> member. 


Set the following values to indicate the valid structure members.



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
The <b>wAlignment</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_ALL"></a><a id="pfm_all"></a><dl>
<dt><b>PFM_ALL</b></dt>
</dl>
</td>
<td width="60%">
A combination of the following values: PFM_STARTINDENT, PFM_RIGHTINDENT, PFM_OFFSET, PFM_ALIGNMENT, PFM_TABSTOPS, PFM_NUMBERING, PFM_OFFSETINDENT, and PFM_RTLPARA.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_ALL2"></a><a id="pfm_all2"></a><dl>
<dt><b>PFM_ALL2</b></dt>
</dl>
</td>
<td width="60%">
A combination of the following values: PFM_ALL, PFM_EFFECTS, PFM_SPACEBEFORE, PFM_SPACEAFTER, PFM_LINESPACING, PFM_STYLE, PFM_SHADING, PFM_BORDER, PFM_NUMBERINGTAB, PFM_NUMBERINGSTART, and PFM_NUMBERINGSTYLE.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_BORDER"></a><a id="pfm_border"></a><dl>
<dt><b>PFM_BORDER</b></dt>
</dl>
</td>
<td width="60%">
The <b>wBorderSpace</b>, <b>wBorderWidth</b>, and <b>wBorders</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_LINESPACING"></a><a id="pfm_linespacing"></a><dl>
<dt><b>PFM_LINESPACING</b></dt>
</dl>
</td>
<td width="60%">
The <b>dyLineSpacing</b> and <b>bLineSpacingRule</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_NUMBERING"></a><a id="pfm_numbering"></a><dl>
<dt><b>PFM_NUMBERING</b></dt>
</dl>
</td>
<td width="60%">
The <b>wNumbering</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_NUMBERINGSTART"></a><a id="pfm_numberingstart"></a><dl>
<dt><b>PFM_NUMBERINGSTART</b></dt>
</dl>
</td>
<td width="60%">
The <b>wNumberingStart</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_NUMBERINGSTYLE"></a><a id="pfm_numberingstyle"></a><dl>
<dt><b>PFM_NUMBERINGSTYLE</b></dt>
</dl>
</td>
<td width="60%">
The <b>wNumberingStyle</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_NUMBERINGTAB"></a><a id="pfm_numberingtab"></a><dl>
<dt><b>PFM_NUMBERINGTAB</b></dt>
</dl>
</td>
<td width="60%">
The <b>wNumberingTab</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_OFFSET"></a><a id="pfm_offset"></a><dl>
<dt><b>PFM_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
The <b>dxOffset</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_OFFSETINDENT"></a><a id="pfm_offsetindent"></a><dl>
<dt><b>PFM_OFFSETINDENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>dxStartIndent</b> member is valid. If you are setting the indentation, <b>dxStartIndent</b> specifies the amount to indent relative to the current indentation.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_OUTLINELEVEL"></a><a id="pfm_outlinelevel"></a><dl>
<dt><b>PFM_OUTLINELEVEL</b></dt>
</dl>
</td>
<td width="60%">
The <b>bOutlineLevel</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_RIGHTINDENT"></a><a id="pfm_rightindent"></a><dl>
<dt><b>PFM_RIGHTINDENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>dxRightIndent</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_SHADING"></a><a id="pfm_shading"></a><dl>
<dt><b>PFM_SHADING</b></dt>
</dl>
</td>
<td width="60%">
The <b>wShadingWeight</b> and <b>wShadingStyle</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_SPACEAFTER"></a><a id="pfm_spaceafter"></a><dl>
<dt><b>PFM_SPACEAFTER</b></dt>
</dl>
</td>
<td width="60%">
The <b>dySpaceAfter</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_SPACEBEFORE"></a><a id="pfm_spacebefore"></a><dl>
<dt><b>PFM_SPACEBEFORE</b></dt>
</dl>
</td>
<td width="60%">
The <b>dySpaceBefore</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_STARTINDENT"></a><a id="pfm_startindent"></a><dl>
<dt><b>PFM_STARTINDENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>dxStartIndent</b> member is valid and specifies the indentation from the left margin. If both PFM_STARTINDENT and PFM_OFFSETINDENT are specified, PFM_STARTINDENT takes precedence.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_STYLE"></a><a id="pfm_style"></a><dl>
<dt><b>PFM_STYLE</b></dt>
</dl>
</td>
<td width="60%">
The <b>sStyle</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_TABSTOPS"></a><a id="pfm_tabstops"></a><dl>
<dt><b>PFM_TABSTOPS</b></dt>
</dl>
</td>
<td width="60%">
The <b>cTabCount</b> and <b>rgxTabs</b> members are valid.

</td>
</tr>
</table>
 


Set the following values to indicate the valid attributes of the <b>wEffects</b> member.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PFM_DONOTHYPHEN"></a><a id="pfm_donothyphen"></a><dl>
<dt><b>PFM_DONOTHYPHEN</b></dt>
</dl>
</td>
<td width="60%">
The PFE_DONOTHYPHEN value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_EFFECTS"></a><a id="pfm_effects"></a><dl>
<dt><b>PFM_EFFECTS</b></dt>
</dl>
</td>
<td width="60%">
A combination of the following values: PFM_RTLPARA, PFM_KEEP, PFM_KEEPNEXT, PFM_TABLE, PFM_PAGEBREAKBEFORE, PFM_NOLINENUMBER, PFM_NOWIDOWCONTROL, PFM_DONOTHYPHEN, PFM_SIDEBYSIDE, and PFM_TABLEROWDELIMITER.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_KEEP"></a><a id="pfm_keep"></a><dl>
<dt><b>PFM_KEEP</b></dt>
</dl>
</td>
<td width="60%">
The PFE_KEEP value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_KEEPNEXT"></a><a id="pfm_keepnext"></a><dl>
<dt><b>PFM_KEEPNEXT</b></dt>
</dl>
</td>
<td width="60%">
The PFE_KEEPNEXT value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_NOLINENUMBER"></a><a id="pfm_nolinenumber"></a><dl>
<dt><b>PFM_NOLINENUMBER</b></dt>
</dl>
</td>
<td width="60%">
The PFE_NOLINENUMBER value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_NOWIDOWCONTROL"></a><a id="pfm_nowidowcontrol"></a><dl>
<dt><b>PFM_NOWIDOWCONTROL</b></dt>
</dl>
</td>
<td width="60%">
The PFE_NOWIDOWCONTROL value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_PAGEBREAKBEFORE"></a><a id="pfm_pagebreakbefore"></a><dl>
<dt><b>PFM_PAGEBREAKBEFORE</b></dt>
</dl>
</td>
<td width="60%">
The PFE_PAGEBREAKBEFORE value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_RTLPARA"></a><a id="pfm_rtlpara"></a><dl>
<dt><b>PFM_RTLPARA</b></dt>
</dl>
</td>
<td width="60%">
The PFE_RTLPARA value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_SIDEBYSIDE"></a><a id="pfm_sidebyside"></a><dl>
<dt><b>PFM_SIDEBYSIDE</b></dt>
</dl>
</td>
<td width="60%">
The PFE_SIDEBYSIDE value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_TABLE"></a><a id="pfm_table"></a><dl>
<dt><b>PFM_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The PFE_TABLE value is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="PFM_TABLEROWDELIMITER"></a><a id="pfm_tablerowdelimiter"></a><dl>
<dt><b>PFM_TABLEROWDELIMITER</b></dt>
</dl>
</td>
<td width="60%">
The PFE_TABLEROWDELIMITER value is valid.

</td>
</tr>
</table>
 


### -field dxOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Indentation of the second and subsequent lines, relative to the indentation of the first line, in twips. The first line is indented if this member is negative or outdented if this member is positive. To use this member, set the PFM_OFFSET flag in the <b>dwMask</b> member. 


### -field dxRightIndent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Indentation of the right side of the paragraph, relative to the right margin, in twips. To use this member, set the PFM_RIGHTINDENT flag in the <b>dwMask</b> member. 


### -field dxStartIndent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Indentation of the paragraph's first line, in twips. The indentation of subsequent lines depends on the <b>dxOffset</b> member. To use the <b>dxStartIndent</b> member, set the PFM_STARTINDENT or PFM_OFFSETINDENT flag in the <b>dwMask</b> member. If you are setting the indentation, use the PFM_STARTINDENT flag to specify an absolute indentation from the left margin; or use the PFM_OFFSETINDENT flag to specify an indentation relative to the paragraph's current indentation. Use either flag to retrieve the current indentation. 


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
 


### -field wAlignment

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Paragraph alignment. To use this member, set the PFM_ALIGNMENT flag in the <b>dwMask</b> member. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<td width="40%"><a id="PFA_JUSTIFY"></a><a id="pfa_justify"></a><dl>
<dt><b>PFA_JUSTIFY</b></dt>
</dl>
</td>
<td width="60%">
<b>RichEdit 2.0:</b>Paragraphs are justified. Rich edit controls earlier than RichEdit 3.0 display the text aligned with the left margin. 


</td>
</tr>
<tr>
<td width="40%"><a id="PFA_FULL_INTERWORD"></a><a id="pfa_full_interword"></a><dl>
<dt><b>PFA_FULL_INTERWORD</b></dt>
</dl>
</td>
<td width="60%">
Paragraphs are justified by expanding the blanks alone. 

</td>
</tr>
</table>
 


### -field wEffects

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

This member is also known as <b>wReserved</b> for Microsoft Rich Edit 1.0 because it was reserved.


<b>Rich Edit 1.0:</b> 
						Reserved; the value must be zero. 

<b>Rich Edit 2.0:</b> A set of bit flags that specify paragraph effects. These flags are included only for compatibility with TOM interfaces; the rich edit control stores the value but does not use it to display the text. 

This member can be a combination of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PFE_DONOTHYPHEN"></a><a id="pfe_donothyphen"></a><dl>
<dt><b>PFE_DONOTHYPHEN</b></dt>
</dl>
</td>
<td width="60%">
Disables automatic hyphenation.

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_KEEP"></a><a id="pfe_keep"></a><dl>
<dt><b>PFE_KEEP</b></dt>
</dl>
</td>
<td width="60%">
No page break within the paragraph.

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_KEEPNEXT"></a><a id="pfe_keepnext"></a><dl>
<dt><b>PFE_KEEPNEXT</b></dt>
</dl>
</td>
<td width="60%">
No page break between this paragraph and the next.

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_NOLINENUMBER"></a><a id="pfe_nolinenumber"></a><dl>
<dt><b>PFE_NOLINENUMBER</b></dt>
</dl>
</td>
<td width="60%">
Disables line numbering (not implemented).

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_NOWIDOWCONTROL"></a><a id="pfe_nowidowcontrol"></a><dl>
<dt><b>PFE_NOWIDOWCONTROL</b></dt>
</dl>
</td>
<td width="60%">
Disables widow and orphan control for the selected paragraph.

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_PAGEBREAKBEFORE"></a><a id="pfe_pagebreakbefore"></a><dl>
<dt><b>PFE_PAGEBREAKBEFORE</b></dt>
</dl>
</td>
<td width="60%">
Inserts a page break before the selected paragraph.

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_RTLPARA"></a><a id="pfe_rtlpara"></a><dl>
<dt><b>PFE_RTLPARA</b></dt>
</dl>
</td>
<td width="60%">
Displays text using right-to-left reading order (in Rich Edit 2.1 and later).

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_SIDEBYSIDE"></a><a id="pfe_sidebyside"></a><dl>
<dt><b>PFE_SIDEBYSIDE</b></dt>
</dl>
</td>
<td width="60%">
Displays paragraphs side by side (not implemented).

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_TABLE"></a><a id="pfe_table"></a><dl>
<dt><b>PFE_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The paragraph is a table row.

</td>
</tr>
<tr>
<td width="40%"><a id="PFE_TABLEROWDELIMITER"></a><a id="pfe_tablerowdelimiter"></a><dl>
<dt><b>PFE_TABLEROWDELIMITER</b></dt>
</dl>
</td>
<td width="60%">
The paragraph is a start delimiter (U+FFF9 U+000D) or end delimiter (U+FFFB U+000D) of a row in a table.

</td>
</tr>
</table>
 


### -field wNumbering

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Options used for bulleted or numbered paragraphs. To use this member, set the PFM_NUMBERING flag in the 
					<b>dwMask</b> member.  


This member can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="zero"></a><a id="ZERO"></a><dl>
<dt><b>zero</b></dt>
</dl>
</td>
<td width="60%">
No paragraph numbering or bullets.

</td>
</tr>
<tr>
<td width="40%"><a id="PFN_BULLET"></a><a id="pfn_bullet"></a><dl>
<dt><b>PFN_BULLET</b></dt>
</dl>
</td>
<td width="60%">
Insert a bullet at the beginning of each selected paragraph.

</td>
</tr>
</table>
 


Rich Edit versions earlier than version 3.0 do not display paragraph numbers. However, for compatibility with Microsoft <a href="/windows/win32/controls/text-object-model">Text Object Model</a> (TOM) interfaces, 
						<b>wNumbering</b> can specify one of the following values. (The rich edit control stores the value but does not use it to display the text.) 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PFN_ARABIC"></a><a id="pfn_arabic"></a><dl>
<dt><b>PFN_ARABIC</b></dt>
</dl>
</td>
<td width="60%">
Use Arabic numbers (0, 1, 2, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="PFN_LCLETTER"></a><a id="pfn_lcletter"></a><dl>
<dt><b>PFN_LCLETTER</b></dt>
</dl>
</td>
<td width="60%">
Use lowercase letters (a, b, c, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="PFN_LCROMAN"></a><a id="pfn_lcroman"></a><dl>
<dt><b>PFN_LCROMAN</b></dt>
</dl>
</td>
<td width="60%">
Use lowercase Roman letters (i, ii, iii, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="PFN_UCLETTER"></a><a id="pfn_ucletter"></a><dl>
<dt><b>PFN_UCLETTER</b></dt>
</dl>
</td>
<td width="60%">
Use uppercase letters (A, B, C, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="PFN_UCROMAN"></a><a id="pfn_ucroman"></a><dl>
<dt><b>PFN_UCROMAN</b></dt>
</dl>
</td>
<td width="60%">
Use uppercase Roman letters (I, II, III, and so on).

</td>
</tr>
<tr>
<td width="40%"><a id="7"></a><dl>
<dt><b>7</b></dt>
</dl>
</td>
<td width="60%">
Uses a sequence of characters beginning with the Unicode character specified by the 
									<b>wNumberingStart</b> member. 

</td>
</tr>
</table>
 


## -see-also




<a href="/windows/win32/controls/em-getparaformat">EM_GETPARAFORMAT</a>



<a href="/windows/win32/controls/em-setparaformat">EM_SETPARAFORMAT</a>



<a href="/windows/win32/api/richedit/ns-richedit-paraformat">PARAFORMAT</a>
 

 
