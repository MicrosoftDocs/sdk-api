---
UID: NS:commctrl.tagLVITEMW
title: LVITEMW (commctrl.h)
description: Specifies or receives the attributes of a list-view item. This structure has been updated to support a new mask value (LVIF_INDENT) that enables item indenting. This structure supersedes the LV_ITEM structure. (Unicode)
helpviewer_keywords: ["*LPLVITEMW","I_GROUPIDCALLBACK","I_GROUPIDNONE","LPLVITEM","LPLVITEM structure pointer [Windows Controls]","LVCFMT_FILL","LVCFMT_LINE_BREAK","LVCFMT_NO_TITLE","LVCFMT_TILE_PLACEMENTMASK","LVCFMT_WRAP","LVIF_COLFMT","LVIF_COLUMNS","LVIF_DI_SETITEM","LVIF_GROUPID","LVIF_IMAGE","LVIF_INDENT","LVIF_NORECOMPUTE","LVIF_PARAM","LVIF_STATE","LVIF_TEXT","LVITEM","LVITEM structure [Windows Controls]","LVITEMA","LVITEMW","_win32_LVITEM","_win32_LVITEM_cpp","commctrl/LPLVITEM","commctrl/LVITEM","commctrl/LVITEMA","commctrl/LVITEMW","controls.LVITEM","controls._win32_LVITEM"]
old-location: controls\LVITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvitem.htm
ms.date: 12/05/2018
ms.keywords: '*LPLVITEMW, I_GROUPIDCALLBACK, I_GROUPIDNONE, LPLVITEM, LPLVITEM structure pointer [Windows Controls], LVCFMT_FILL, LVCFMT_LINE_BREAK, LVCFMT_NO_TITLE, LVCFMT_TILE_PLACEMENTMASK, LVCFMT_WRAP, LVIF_COLFMT, LVIF_COLUMNS, LVIF_DI_SETITEM, LVIF_GROUPID, LVIF_IMAGE, LVIF_INDENT, LVIF_NORECOMPUTE, LVIF_PARAM, LVIF_STATE, LVIF_TEXT, LVITEM, LVITEM structure [Windows Controls], LVITEMA, LVITEMW, _win32_LVITEM, _win32_LVITEM_cpp, commctrl/LPLVITEM, commctrl/LVITEM, commctrl/LVITEMA, commctrl/LVITEMW, controls.LVITEM, controls._win32_LVITEM'
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LVITEMW (Unicode) and LVITEMA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: LVITEMW, *LPLVITEMW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVITEMW
 - commctrl/tagLVITEMW
 - LPLVITEMW
 - commctrl/LPLVITEMW
 - LVITEMW
 - commctrl/LVITEMW
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
 - LVITEM
 - LVITEMA
 - LVITEMW
---

# LVITEMW structure


## -description

Specifies or receives the attributes of a list-view item. This structure has been updated to support a new mask value (LVIF_INDENT) that enables item indenting. This structure supersedes the <b>LV_ITEM</b> structure.

## -struct-fields

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Set of flags that specify which members of this structure contain data to be set or which members are being requested. This member can have one or more of the following flags set: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVIF_COLFMT"></a><a id="lvif_colfmt"></a><dl>
<dt><b>LVIF_COLFMT</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later.</b> The <b>piColFmt</b> member is valid or must be set. If this flag is used, the <b>cColumns</b> member is valid or must be set. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_COLUMNS"></a><a id="lvif_columns"></a><dl>
<dt><b>LVIF_COLUMNS</b></dt>
</dl>
</td>
<td width="60%">
The <b>cColumns</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_DI_SETITEM"></a><a id="lvif_di_setitem"></a><dl>
<dt><b>LVIF_DI_SETITEM</b></dt>
</dl>
</td>
<td width="60%">
The operating system should store the requested list item information and not ask for it again. This flag is used only with the <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> notification code.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_GROUPID"></a><a id="lvif_groupid"></a><dl>
<dt><b>LVIF_GROUPID</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>iGroupId</b> member is valid or must be set. If this flag is not set when an <a href="/windows/desktop/Controls/lvm-insertitem">LVM_INSERTITEM</a> message is sent, the value of <b>iGroupId</b> is assumed to be I_GROUPIDCALLBACK.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_IMAGE"></a><a id="lvif_image"></a><dl>
<dt><b>LVIF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iImage</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_INDENT"></a><a id="lvif_indent"></a><dl>
<dt><b>LVIF_INDENT</b></dt>
</dl>
</td>
<td width="60%">
The <b>iIndent</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_NORECOMPUTE"></a><a id="lvif_norecompute"></a><dl>
<dt><b>LVIF_NORECOMPUTE</b></dt>
</dl>
</td>
<td width="60%">
The control will not generate <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> to retrieve text information if it receives an <a href="/windows/desktop/Controls/lvm-getitem">LVM_GETITEM</a> message. Instead, the <b>pszText</b> member will contain LPSTR_TEXTCALLBACK.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_PARAM"></a><a id="lvif_param"></a><dl>
<dt><b>LVIF_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>lParam</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_STATE"></a><a id="lvif_state"></a><dl>
<dt><b>LVIF_STATE</b></dt>
</dl>
</td>
<td width="60%">
The <b>state</b> member is valid or must be set.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIF_TEXT"></a><a id="lvif_text"></a><dl>
<dt><b>LVIF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszText</b> member is valid or must be set.

</td>
</tr>
</table>

### -field iItem

Type: <b>int</b>

Zero-based index of the item to which this structure refers.

### -field iSubItem

Type: <b>int</b>

One-based index of the subitem to which this structure refers, or zero if this structure refers to an item rather than a subitem.

### -field state

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Indicates the item's state, state image, and overlay image. The 
					<b>stateMask</b> member indicates the valid bits of this member. 



Bits 0 through 7 of this member contain the item state flags. This can be one or more of the <a href="/windows/desktop/Controls/list-view-item-states">item state</a> values.



Bits 8 through 11 of this member specify the one-based overlay image index. Both the full-sized icon image list and the small icon image list can have overlay images. The overlay image is superimposed over the item's icon image. If these bits are zero, the item has no overlay image. To isolate these bits, use the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_OVERLAYMASK</a> mask. To set the overlay image index in this member, you should use the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask">INDEXTOOVERLAYMASK</a> macro. The image list's overlay images are set with the <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_setoverlayimage">ImageList_SetOverlayImage</a> function.



Bits 12 through 15 of this member specify the state image index. The state image is displayed next to an item's icon to indicate an application-defined state. If these bits are zero, the item has no state image. To isolate these bits, use the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_STATEIMAGEMASK</a> mask. To set the state image index, use the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextostateimagemask">INDEXTOSTATEIMAGEMASK</a> macro. The state image index specifies the index of the image in the state image list that should be drawn. The state image list is specified with the <a href="/windows/desktop/Controls/lvm-setimagelist">LVM_SETIMAGELIST</a> message.

### -field stateMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Value specifying which bits of the 
					<b>state</b> member will be retrieved or modified. For example, setting this member to <a href="/windows/desktop/Controls/list-view-item-states">LVIS_SELECTED</a> will cause only the item's selection state to be retrieved. 



This member allows you to modify one or more item states without having to retrieve all of the item states first. For example, setting this member to <b>LVIS_SELECTED</b> and <b>state</b> to zero will cause the item's selection state to be cleared, but none of the other states will be affected. 



To retrieve or modify all of the states, set this member to (<b>UINT</b>)-1.



You can use the macro <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setitemstate">ListView_SetItemState</a> both to set and to clear bits.

### -field pszText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

If the structure specifies item attributes, <b>pszText</b> is a pointer to a null-terminated string containing the item text. When responding to an <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> notification, be sure that this pointer remains valid until after the next notification has been received.



If the structure receives item attributes, <b>pszText</b> is a pointer to a buffer that receives the item text. Note that although the list-view control allows any length string to be stored as item text, only the first 260 <b>TCHAR</b>s are displayed.



If the value of  <b>pszText</b> is LPSTR_TEXTCALLBACK, the item is a <a href="/windows/desktop/Controls/list-view-controls-overview">callback item</a>. If the callback text changes, you must explicitly set <b>pszText</b> to LPSTR_TEXTCALLBACK and notify the list-view control of the change by sending an <a href="/windows/desktop/Controls/lvm-setitem">LVM_SETITEM</a> or <a href="/windows/desktop/Controls/lvm-setitemtext">LVM_SETITEMTEXT</a> message.



Do not set <b>pszText</b> to LPSTR_TEXTCALLBACK if the list-view control has the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_SORTASCENDING</a> or <a href="/windows/desktop/Controls/list-view-window-styles">LVS_SORTDESCENDING</a> style.

### -field cchTextMax

Type: <b>int</b>

Number of <b>TCHAR</b><b>s</b> in the buffer pointed to by <b>pszText</b>,  including the terminating <b>NULL</b>.



This member is only used when the structure receives item attributes. It is ignored when the structure specifies item attributes. For example, <b>cchTextMax</b> is ignored during <a href="/windows/desktop/Controls/lvm-setitem">LVM_SETITEM</a> and <a href="/windows/desktop/Controls/lvm-insertitem">LVM_INSERTITEM</a>. It is read-only during <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> and other LVN_ notifications.



<div class="alert"><b>Note</b>  Never copy more than <b>cchTextMax</b> <b>TCHAR</b><b>s</b>—where <b>cchTextMax</b> includes the terminating <b>NULL</b>—into <b>pszText</b> during an LVN_  notification, otherwise your program can fail.</div>
<div> </div>

### -field iImage

Type: <b>int</b>

Index of the item's icon in the control's image list. This applies to both the large and small image list. If this member is the I_IMAGECALLBACK value, the parent window is responsible for storing the index. In this case, the list-view control sends the parent an <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> notification code to retrieve the index when it needs to display the image.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Value specific to the item. If you use the <a href="/windows/desktop/Controls/lvm-sortitems">LVM_SORTITEMS</a> message, the list-view control passes this value to the application-defined comparison function. You can also use the <a href="/windows/desktop/Controls/lvm-finditem">LVM_FINDITEM</a> message to search a list-view control for an item with a specified <b>lParam</b> value.

### -field iIndent

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. Number of image widths to indent the item. A single indentation equals the width of an item image. Therefore, the value 1 indents the item by the width of one image, the value 2 indents by two images, and so on. Note that this field is supported only for items. Attempting to set subitem indentation will cause the calling function to fail.

### -field iGroupId

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0</a> Identifier of the group that the item belongs to, or one of the following values.
                

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="I_GROUPIDCALLBACK"></a><a id="i_groupidcallback"></a><dl>
<dt><b>I_GROUPIDCALLBACK</b></dt>
</dl>
</td>
<td width="60%">
The listview control sends the parent an <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> notification code to retrieve the index of the group.

</td>
</tr>
<tr>
<td width="40%"><a id="I_GROUPIDNONE"></a><a id="i_groupidnone"></a><dl>
<dt><b>I_GROUPIDNONE</b></dt>
</dl>
</td>
<td width="60%">
The item does not belong to a group.

</td>
</tr>
</table>

### -field cColumns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0 </a> Number of data columns (subitems) to display for this item in tile view. The maximum value is 20. If this value is I_COLUMNSCALLBACK, the size of the column array and the array itself (<b>puColumns</b>) are obtained by sending a <a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a> notification.

### -field puColumns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">PUINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0 </a> A pointer to an array of column indices, specifying which columns are displayed for this item, and the order of those columns.

### -field piColFmt

Type: <b>int*</b>

<b>Windows Vista:</b> Not implemented. <b>Windows 7 and later:</b> A pointer to an array of the following flags (alone or in combination), specifying the format of each subitem in extended tile view.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_LINE_BREAK"></a><a id="lvcfmt_line_break"></a><dl>
<dt><b>LVCFMT_LINE_BREAK</b></dt>
</dl>
</td>
<td width="60%">
Forces the column to wrap to the top of the next list of columns.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_FILL"></a><a id="lvcfmt_fill"></a><dl>
<dt><b>LVCFMT_FILL</b></dt>
</dl>
</td>
<td width="60%">
Fills the remainder of the tile area. Might have a title.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_WRAP"></a><a id="lvcfmt_wrap"></a><dl>
<dt><b>LVCFMT_WRAP</b></dt>
</dl>
</td>
<td width="60%">
Allows the column to wrap within the remaining space in its list of columns.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_NO_TITLE"></a><a id="lvcfmt_no_title"></a><dl>
<dt><b>LVCFMT_NO_TITLE</b></dt>
</dl>
</td>
<td width="60%">
Removes the title from the subitem.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCFMT_TILE_PLACEMENTMASK"></a><a id="lvcfmt_tile_placementmask"></a><dl>
<dt><b>LVCFMT_TILE_PLACEMENTMASK</b></dt>
</dl>
</td>
<td width="60%">
Equivalent to a combination of LVCFMT_LINE_BREAK and LVCFMT_FILL.

</td>
</tr>
</table>

### -field iGroup

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Windows Vista</a>: Group index of the item. Valid only for owner data/callback (single item in multiple groups).

## -remarks

The <b>LVITEM</b> structure is used with several messages, including <a href="/windows/desktop/Controls/lvm-getitem">LVM_GETITEM</a>, <a href="/windows/desktop/Controls/lvm-setitem">LVM_SETITEM</a>, <a href="/windows/desktop/Controls/lvm-insertitem">LVM_INSERTITEM</a>, and <a href="/windows/desktop/Controls/lvm-deleteitem">LVM_DELETEITEM</a>.

In tile view, the item name is displayed to the right of the icon. You can specify additional subitems (corresponding to columns in the details view), to be displayed on lines below the item name. The <b>puColumns</b> array contains the indices of subitems to be displayed. Indices should be greater than 0, because subitem 0, the item name, is already displayed. Column information can also be set in the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvtileinfo">LVTILEINFO</a> structure when modifying the list item.

For example code, see <a href="/windows/desktop/Controls/using-list-view-controls">Using List-View Controls</a>.

<div class="alert"><b>Note</b>  Comctl32.dll version 6 is not redistributable but it is included in Windows or later. To use Comctl32.dll version 6, specify it in a manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>



> [!NOTE]
> The commctrl.h header defines LVITEM as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
