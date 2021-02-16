---
UID: NS:commctrl.tagLVGROUP
title: LVGROUP (commctrl.h)
description: Used to set and retrieve groups.
helpviewer_keywords: ["*PLVGROUP","LVGF_FOOTER","LVGF_HEADER","LVGF_NONE","LVGF_STATE","LVGROUP","LVGROUP structure [Windows Controls]","PLVGROUP","PLVGROUP structure pointer [Windows Controls]","commctrl/LVGROUP","commctrl/PLVGROUP","controls.LVGROUP","controls.inet_LVGROUP","inet_LVGROUP","inet_LVGROUP_cpp"]
old-location: controls\LVGROUP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lv_group.htm
ms.date: 12/05/2018
ms.keywords: '*PLVGROUP, LVGF_FOOTER, LVGF_HEADER, LVGF_NONE, LVGF_STATE, LVGROUP, LVGROUP structure [Windows Controls], PLVGROUP, PLVGROUP structure pointer [Windows Controls], commctrl/LVGROUP, commctrl/PLVGROUP, controls.LVGROUP, controls.inet_LVGROUP, inet_LVGROUP, inet_LVGROUP_cpp'
req.header: commctrl.h
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
req.typenames: LVGROUP, *PLVGROUP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVGROUP
 - commctrl/tagLVGROUP
 - PLVGROUP
 - commctrl/PLVGROUP
 - LVGROUP
 - commctrl/LVGROUP
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
 - LVGROUP
---

# LVGROUP structure


## -description

Used to set and retrieve groups.

## -struct-fields

### -field cbSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of this structure, in bytes.

### -field mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Mask that specifies which members of the structure are valid input. One or more of the following values:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVGF_NONE"></a><a id="lvgf_none"></a><dl>
<dt><b>LVGF_NONE</b></dt>
</dl>
</td>
<td width="60%">
No other items are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGF_HEADER"></a><a id="lvgf_header"></a><dl>
<dt><b>LVGF_HEADER</b></dt>
</dl>
</td>
<td width="60%">
<b>pszHeader</b> and <b>cchHeader</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGF_FOOTER"></a><a id="lvgf_footer"></a><dl>
<dt><b>LVGF_FOOTER</b></dt>
</dl>
</td>
<td width="60%">
<b>pszFooter</b> and <b>cchFooter</b> members are valid. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVGF_STATE"></a><a id="lvgf_state"></a><dl>
<dt><b>LVGF_STATE</b></dt>
</dl>
</td>
<td width="60%">
<b>state</b> and <b>stateMask</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_ALIGN</dt>
</dl>
</td>
<td width="60%">
<b>uAlign</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_GROUPID</dt>
</dl>
</td>
<td width="60%">
<b>iGroupId</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_SUBTITLE</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>pszSubtitle</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_TASK</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>pszTask</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_DESCRIPTIONTOP</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>pszDescriptionTop</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_DESCRIPTIONBOTTOM</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>pszDescriptionBottom</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_TITLEIMAGE</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>iTitleImage</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_EXTENDEDIMAGE</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>iExtendedImage</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_ITEMS</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>cItems</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_SUBSET</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>pszSubsetTitle</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGF_SUBSETITEMS</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The <b>cchSubsetTitle</b> member is valid.

</td>
</tr>
</table>

### -field pszHeader

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a null-terminated string that contains the header text when item information is being set. If group information is being retrieved, this member specifies the address of the buffer that receives the header text.

### -field cchHeader

Type: <b>int</b>

Size in <b>TCHAR</b>s of the buffer pointed to by the <b>pszHeader</b> member. If the structure is not receiving information about a group, this member is ignored.

### -field pszFooter

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a null-terminated string that contains the footer text when item information is being set. If group information is being retrieved, this member specifies the address of the buffer that receives the footer text.

### -field cchFooter

Type: <b>int</b>

Size in <b>TCHAR</b>s of the buffer pointed to by the <b>pszFooter</b> member. If the structure is not receiving information about a group, this member is ignored.

### -field iGroupId

Type: <b>int</b>

ID of the group.

### -field stateMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Mask used with <a href="/windows/desktop/Controls/lvm-getgroupinfo">LVM_GETGROUPINFO</a>  and <a href="/windows/desktop/Controls/lvm-setgroupinfo">LVM_SETGROUPINFO</a> to specify which flags in the <b>state</b> value are being retrieved or set.

### -field state

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flag that can have one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_NORMAL</dt>
</dl>
</td>
<td width="60%">
Groups are expanded, the group name is displayed, and all items in the group are displayed.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_COLLAPSED</dt>
</dl>
</td>
<td width="60%">
 The group is collapsed.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_HIDDEN</dt>
</dl>
</td>
<td width="60%">
 The group is hidden.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_NOHEADER</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The group does not display a header.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_COLLAPSIBLE</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The group can be collapsed.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_FOCUSED</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The group has keyboard focus.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_SELECTED</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The group is selected.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_SUBSETED</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The group displays only a portion of its items.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGS_SUBSETLINKFOCUSED</dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.00 and later</a>. The subset link of the group has keyboard focus.

</td>
</tr>
</table>

### -field uAlign

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Indicates the alignment of the header or footer text for the group. It can have one or more of the following values. Use one of the header flags. Footer flags are optional. 
                    
                    



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGA_FOOTER_CENTER</dt>
</dl>
</td>
<td width="60%">
Footer text is centered horizontally in the window. 

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGA_FOOTER_LEFT</dt>
</dl>
</td>
<td width="60%">
Footer text is aligned at the left of the window. 
 

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGA_FOOTER_RIGHT</dt>
</dl>
</td>
<td width="60%">
Footer text is aligned at the right of the window.
 

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGA_HEADER_CENTER</dt>
</dl>
</td>
<td width="60%">
 Header text is centered horizontally in the window.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGA_HEADER_LEFT</dt>
</dl>
</td>
<td width="60%">
Header text is aligned at the left of the window.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVGA_HEADER_RIGHT</dt>
</dl>
</td>
<td width="60%">
 Header text is aligned at the right of the window.

</td>
</tr>
</table>

### -field pszSubtitle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a null-terminated string that contains the subtitle text when item information is being set. If group information is being retrieved, this member specifies the address of the buffer that receives the subtitle text. This element is drawn under the header text.

### -field cchSubtitle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size, in <b>TCHAR</b>s, of the buffer pointed to by the <b>pszSubtitle</b> member. If the structure is not receiving information about a group, this member is ignored.

### -field pszTask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a null-terminated string that contains the text for a task link when item information is being set. If group information is being retrieved, this member specifies the address of the buffer that receives the task text. This item is drawn right-aligned opposite the header text. When clicked by the user, the task link generates an <a href="/windows/desktop/Controls/lvn-linkclick">LVN_LINKCLICK</a> notification.

### -field cchTask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size in <b>TCHAR</b>s of the buffer pointed to by the <b>pszTask</b> member. If the structure is not receiving information about a group, this member is ignored.

### -field pszDescriptionTop

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a null-terminated string that contains the top description text when item information is being set. If group information is being retrieved, this member specifies the address of the buffer that receives the top description text. This item is drawn opposite the title image when there is a title image, no extended image, and <b>uAlign</b>==<b>LVGA_HEADER_CENTER</b>.

### -field cchDescriptionTop

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size in <b>TCHAR</b>s of the buffer pointed to by the <b>pszDescriptionTop</b> member. If the structure is not receiving information about a group, this member is ignored.

### -field pszDescriptionBottom

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

Pointer to a null-terminated string that contains the bottom description text when item information is being set. If group information is being retrieved, this member specifies the address of the buffer that receives the bottom description text. This item is drawn under the top description text when there is a title image, no extended image, and <b>uAlign</b>==<b>LVGA_HEADER_CENTER</b>.

### -field cchDescriptionBottom

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size in <b>TCHAR</b>s of the buffer pointed to by the <b>pszDescriptionBottom</b> member. If the structure is not receiving information about a group, this member is ignored.

### -field iTitleImage

Type: <b>int</b>

Index of the title image in the control imagelist.

### -field iExtendedImage

Type: <b>int</b>

Index of the extended image in the control imagelist.

### -field iFirstItem

Type: <b>int</b>

Read-only.

### -field cItems

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Read-only in non-owner data mode.

### -field pszSubsetTitle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPWSTR</a></b>

<b>NULL</b> if group is not a subset. Pointer to a null-terminated string that contains the subset title text when item information is being set. If group information is being retrieved, this member specifies the address of the buffer that receives the subset title text.

### -field cchSubsetTitle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size in <b>TCHAR</b>s of the buffer pointed to by the <b>pszSubsetTitle</b> member. If the structure is not receiving information about a group, this member is ignored.

## -remarks

All strings returned in this structure should be treated as read-only.
	

The creation of subsets is not currently supported, and <b>pszSubsetTitle</b> cannot be set by applications.