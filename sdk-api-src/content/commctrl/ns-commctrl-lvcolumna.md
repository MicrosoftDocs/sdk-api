---
UID: NS:commctrl.tagLVCOLUMNA
title: LVCOLUMNA (commctrl.h)
description: Contains information about a column in report view. This structure is used both for creating and manipulating columns. This structure supersedes the LV_COLUMN structure. (ANSI)
helpviewer_keywords: ["*LPLVCOLUMNA","LPLVCOLUMN","LPLVCOLUMN structure pointer [Windows Controls]","LVCFMT_BITMAP_ON_RIGHT","LVCFMT_CENTER","LVCFMT_COL_HAS_IMAGES","LVCFMT_FIXED_RATIO","LVCFMT_FIXED_WIDTH","LVCFMT_IMAGE","LVCFMT_JUSTIFYMASK","LVCFMT_LEFT","LVCFMT_NO_DPI_SCALE","LVCFMT_RIGHT","LVCFMT_SPLITBUTTON","LVCF_DEFAULTWIDTH","LVCF_FMT","LVCF_IDEALWIDTH","LVCF_IMAGE","LVCF_MINWIDTH","LVCF_ORDER","LVCF_SUBITEM","LVCF_TEXT","LVCF_WIDTH","LVCOLUMN","LVCOLUMN structure [Windows Controls]","LVCOLUMNA","LVCOLUMNW","_win32_LVCOLUMN","_win32_LVCOLUMN_cpp","commctrl/LPLVCOLUMN","commctrl/LVCOLUMN","commctrl/LVCOLUMNA","commctrl/LVCOLUMNW","controls.LVCOLUMN","controls._win32_LVCOLUMN"]
old-location: controls\LVCOLUMN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvcolumn.htm
ms.date: 12/05/2018
ms.keywords: '*LPLVCOLUMNA, LPLVCOLUMN, LPLVCOLUMN structure pointer [Windows Controls], LVCFMT_BITMAP_ON_RIGHT, LVCFMT_CENTER, LVCFMT_COL_HAS_IMAGES, LVCFMT_FIXED_RATIO, LVCFMT_FIXED_WIDTH, LVCFMT_IMAGE, LVCFMT_JUSTIFYMASK, LVCFMT_LEFT, LVCFMT_NO_DPI_SCALE, LVCFMT_RIGHT, LVCFMT_SPLITBUTTON, LVCF_DEFAULTWIDTH, LVCF_FMT, LVCF_IDEALWIDTH, LVCF_IMAGE, LVCF_MINWIDTH, LVCF_ORDER, LVCF_SUBITEM, LVCF_TEXT, LVCF_WIDTH, LVCOLUMN, LVCOLUMN structure [Windows Controls], LVCOLUMNA, LVCOLUMNW, _win32_LVCOLUMN, _win32_LVCOLUMN_cpp, commctrl/LPLVCOLUMN, commctrl/LVCOLUMN, commctrl/LVCOLUMNA, commctrl/LVCOLUMNW, controls.LVCOLUMN, controls._win32_LVCOLUMN'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LVCOLUMNW (Unicode) and LVCOLUMNA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LVCOLUMNA, *LPLVCOLUMNA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVCOLUMNA
 - commctrl/tagLVCOLUMNA
 - LPLVCOLUMNA
 - commctrl/LPLVCOLUMNA
 - LVCOLUMNA
 - commctrl/LVCOLUMNA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - LVCOLUMN
 - LVCOLUMNA
 - LVCOLUMNW
---

# LVCOLUMNA structure


## -description

Contains information about a column in report view. This structure is used both for creating and manipulating columns. This structure supersedes the LV_COLUMN structure.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Variable specifying which members contain valid information. This member can be zero, or one or more of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVCF_FMT"></a><a id="lvcf_fmt"></a><dl>
<dt><b>LVCF_FMT</b></dt>
</dl>
</td>
<td width="60%">
The <b>fmt</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCF_WIDTH"></a><a id="lvcf_width"></a><dl>
<dt><b>LVCF_WIDTH</b></dt>
</dl>
</td>
<td width="60%">
The <b>cx</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCF_TEXT"></a><a id="lvcf_text"></a><dl>
<dt><b>LVCF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszText</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCF_SUBITEM"></a><a id="lvcf_subitem"></a><dl>
<dt><b>LVCF_SUBITEM</b></dt>
</dl>
</td>
<td width="60%">
The <b>iSubItem</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCF_IMAGE"></a><a id="lvcf_image"></a><dl>
<dt><b>LVCF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. The <b>iImage</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCF_ORDER"></a><a id="lvcf_order"></a><dl>
<dt><b>LVCF_ORDER</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. The <b>iOrder</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCF_MINWIDTH"></a><a id="lvcf_minwidth"></a><dl>
<dt><b>LVCF_MINWIDTH</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b>The <b>cxMin</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCF_DEFAULTWIDTH"></a><a id="lvcf_defaultwidth"></a><dl>
<dt><b>LVCF_DEFAULTWIDTH</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b>The <b>cxDefault</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCF_IDEALWIDTH"></a><a id="lvcf_idealwidth"></a><dl>
<dt><b>LVCF_IDEALWIDTH</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b>The <b>cxIdeal</b> member is valid.

</td>
</tr>
</table>

### -field fmt

Type: <b>int</b>

Alignment of the column header and the subitem text in the column. The alignment of the leftmost column is always LVCFMT_LEFT; it cannot be changed. This member can be a combination of the following values. Note that not all combinations are valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_LEFT"></a><a id="lvcfmt_left"></a><dl>
<dt><b>LVCFMT_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Text is left-aligned.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_RIGHT"></a><a id="lvcfmt_right"></a><dl>
<dt><b>LVCFMT_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Text is right-aligned.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_CENTER"></a><a id="lvcfmt_center"></a><dl>
<dt><b>LVCFMT_CENTER</b></dt>
</dl>
</td>
<td width="60%">
Text is centered.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_JUSTIFYMASK"></a><a id="lvcfmt_justifymask"></a><dl>
<dt><b>LVCFMT_JUSTIFYMASK</b></dt>
</dl>
</td>
<td width="60%">
A bitmask used to select those bits of <b>fmt</b> that control field justification. To check the format of a column, use a logical "and" to combine LCFMT_JUSTIFYMASK with <b>fmt</b>. You can then use a switch statement to determine whether the LVCFMT_LEFT, LVCFMT_RIGHT, or LVCFMT_CENTER bits are set.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_IMAGE"></a><a id="lvcfmt_image"></a><dl>
<dt><b>LVCFMT_IMAGE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. The item displays an image from an image list. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_BITMAP_ON_RIGHT"></a><a id="lvcfmt_bitmap_on_right"></a><dl>
<dt><b>LVCFMT_BITMAP_ON_RIGHT</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. The bitmap appears to the right of text. This does not affect an image from an image list assigned to the header item.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_COL_HAS_IMAGES"></a><a id="lvcfmt_col_has_images"></a><dl>
<dt><b>LVCFMT_COL_HAS_IMAGES</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. The header item contains an image in the image list.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_FIXED_WIDTH"></a><a id="lvcfmt_fixed_width"></a><dl>
<dt><b>LVCFMT_FIXED_WIDTH</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b> Can't resize the column; same as HDF_FIXEDWIDTH.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_NO_DPI_SCALE"></a><a id="lvcfmt_no_dpi_scale"></a><dl>
<dt><b>LVCFMT_NO_DPI_SCALE</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b> If not set, CCM_DPISCALE will govern scaling up fixed width.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_FIXED_RATIO"></a><a id="lvcfmt_fixed_ratio"></a><dl>
<dt><b>LVCFMT_FIXED_RATIO</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b> Width will augment with the row height.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_SPLITBUTTON"></a><a id="lvcfmt_splitbutton"></a><dl>
<dt><b>LVCFMT_SPLITBUTTON</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00</a> and <b>Windows Vista.</b> Column is a split button (same as HDF_SPLITBUTTON). The header of the column displays a split button (same as HDF_SPLITBUTTON).

</td>
</tr>
</table>

### -field cx

Type: <b>int</b>

Width of the column, in pixels.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

If column information is being set, this member is the address of a null-terminated string that contains the column header text. If the structure is receiving information about a column, this member specifies the address of the buffer that receives the column header text.

### -field cchTextMax

Type: <b>int</b>

Size in <b>TCHAR</b>s of the buffer pointed to by the <b>pszText</b> member. If the structure is not receiving information about a column, this member is ignored.

### -field iSubItem

Type: <b>int</b>

Index of subitem associated with the column.

### -field iImage

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. Zero-based index of an image within the image list. The specified image will appear within the column.

### -field iOrder

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. Zero-based column offset. Column offset is in left-to-right order. For example, zero indicates the leftmost column.

### -field cxMin

Type: <b>int</b>

<b>Windows Vista</b>. Minimum width of the column in pixels.

### -field cxDefault

Type: <b>int</b>

<b>Windows Vista</b>. Application-defined value typically used to store the default width of the column. This member is ignored by the list-view control.

### -field cxIdeal

Type: <b>int</b>

<b>Windows Vista</b>. Read-only. The ideal width of the column in pixels, as the column may currently be autosized to a lesser width.

## -remarks

If a column is added to a list-view control with index 0 (the leftmost column), it is always LVCFMT_LEFT. Setting other flags on column 0 does not override that alignment. Therefore if you keep inserting columns with index 0, the text in all columns are left-aligned. If you want the first column to be right-aligned or centered you can make a dummy column, then insert one or more columns with index 1 or higher and specify the alignment you require. Finally delete the dummy column.





> [!NOTE]
> The commctrl.h header defines LVCOLUMN as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Controls/lvm-deletecolumn">LVM_DELETECOLUMN</a>



<a href="/windows/desktop/Controls/lvm-getcolumn">LVM_GETCOLUMN</a>



<a href="/windows/desktop/Controls/lvm-insertcolumn">LVM_INSERTCOLUMN</a>



<a href="/windows/desktop/Controls/lvm-setcolumn">LVM_SETCOLUMN</a>



<b>Reference</b>
