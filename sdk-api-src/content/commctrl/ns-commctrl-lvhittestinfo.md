---
UID: NS:commctrl.tagLVHITTESTINFO
title: LVHITTESTINFO (commctrl.h)
description: Contains information about a hit test.
helpviewer_keywords: ["*LPLVHITTESTINFO","LPLVHITTESTINFO","LPLVHITTESTINFO structure pointer [Windows Controls]","LVHITTESTINFO","LVHITTESTINFO structure [Windows Controls]","LVHT_ABOVE","LVHT_BELOW","LVHT_EX_FOOTER","LVHT_EX_GROUP","LVHT_EX_GROUP_BACKGROUND","LVHT_EX_GROUP_COLLAPSE","LVHT_EX_GROUP_FOOTER","LVHT_EX_GROUP_HEADER","LVHT_EX_GROUP_STATEICON","LVHT_EX_GROUP_SUBSETLINK","LVHT_EX_ONCONTENTS","LVHT_NOWHERE","LVHT_ONITEMICON","LVHT_ONITEMLABEL","LVHT_ONITEMSTATEICON","LVHT_TOLEFT","LVHT_TORIGHT","_win32_LVHITTESTINFO","_win32_LVHITTESTINFO_cpp","commctrl/LPLVHITTESTINFO","commctrl/LVHITTESTINFO","controls.LVHITTESTINFO","controls._win32_LVHITTESTINFO"]
old-location: controls\LVHITTESTINFO.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\lvhittestinfo.htm
ms.date: 12/05/2018
ms.keywords: '*LPLVHITTESTINFO, LPLVHITTESTINFO, LPLVHITTESTINFO structure pointer [Windows Controls], LVHITTESTINFO, LVHITTESTINFO structure [Windows Controls], LVHT_ABOVE, LVHT_BELOW, LVHT_EX_FOOTER, LVHT_EX_GROUP, LVHT_EX_GROUP_BACKGROUND, LVHT_EX_GROUP_COLLAPSE, LVHT_EX_GROUP_FOOTER, LVHT_EX_GROUP_HEADER, LVHT_EX_GROUP_STATEICON, LVHT_EX_GROUP_SUBSETLINK, LVHT_EX_ONCONTENTS, LVHT_NOWHERE, LVHT_ONITEMICON, LVHT_ONITEMLABEL, LVHT_ONITEMSTATEICON, LVHT_TOLEFT, LVHT_TORIGHT, _win32_LVHITTESTINFO, _win32_LVHITTESTINFO_cpp, commctrl/LPLVHITTESTINFO, commctrl/LVHITTESTINFO, controls.LVHITTESTINFO, controls._win32_LVHITTESTINFO'
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
req.typenames: LVHITTESTINFO, *LPLVHITTESTINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVHITTESTINFO
 - commctrl/tagLVHITTESTINFO
 - LPLVHITTESTINFO
 - commctrl/LPLVHITTESTINFO
 - LVHITTESTINFO
 - commctrl/LVHITTESTINFO
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
 - LVHITTESTINFO
---

# LVHITTESTINFO structure


## -description

Contains information about a hit test. This structure has been extended to accommodate subitem hit-testing. It is used in association with the <a href="/windows/desktop/Controls/lvm-hittest">LVM_HITTEST</a> and <a href="/windows/desktop/Controls/lvm-subitemhittest">LVM_SUBITEMHITTEST</a> messages and their related macros. This structure supersedes the 
			<b>LVHITTESTINFO</b> structure.

## -struct-fields

### -field pt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

The position to hit test, in client coordinates.

### -field flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The variable that receives information about the results of a hit test. This member can be one or more of the following values:

You can use LVHT_ABOVE, LVHT_BELOW, LVHT_TOLEFT, and LVHT_TORIGHT to determine whether to scroll the contents of a list-view control. Two of these values may be combined. For example, if the position is above and to the left of the client area, you could use both LVHT_ABOVE and LVHT_TOLEFT. 

You can test for LVHT_ONITEM to determine whether a specified position is over a list-view item. This value is a bitwise-OR operation on LVHT_ONITEMICON, LVHT_ONITEMLABEL, and LVHT_ONITEMSTATEICON.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVHT_ABOVE"></a><a id="lvht_above"></a><dl>
<dt><b>LVHT_ABOVE</b></dt>
</dl>
</td>
<td width="60%">
The position is above the control's client area.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_BELOW"></a><a id="lvht_below"></a><dl>
<dt><b>LVHT_BELOW</b></dt>
</dl>
</td>
<td width="60%">
The position is below the control's client area.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_NOWHERE"></a><a id="lvht_nowhere"></a><dl>
<dt><b>LVHT_NOWHERE</b></dt>
</dl>
</td>
<td width="60%">
The position is inside the list-view control's client window, but it is not over a list item.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_ONITEMICON"></a><a id="lvht_onitemicon"></a><dl>
<dt><b>LVHT_ONITEMICON</b></dt>
</dl>
</td>
<td width="60%">
The position is over a list-view item's icon.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_ONITEMLABEL"></a><a id="lvht_onitemlabel"></a><dl>
<dt><b>LVHT_ONITEMLABEL</b></dt>
</dl>
</td>
<td width="60%">
The position is over a list-view item's text.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_ONITEMSTATEICON"></a><a id="lvht_onitemstateicon"></a><dl>
<dt><b>LVHT_ONITEMSTATEICON</b></dt>
</dl>
</td>
<td width="60%">
The position is over the state image of a list-view item.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_TOLEFT"></a><a id="lvht_toleft"></a><dl>
<dt><b>LVHT_TOLEFT</b></dt>
</dl>
</td>
<td width="60%">
The position is to the left of the list-view control's client area.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_TORIGHT"></a><a id="lvht_toright"></a><dl>
<dt><b>LVHT_TORIGHT</b></dt>
</dl>
</td>
<td width="60%">
The position is to the right of the list-view control's client area.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_GROUP_HEADER"></a><a id="lvht_ex_group_header"></a><dl>
<dt><b>LVHT_EX_GROUP_HEADER</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b> The point is within the group header.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_GROUP_FOOTER"></a><a id="lvht_ex_group_footer"></a><dl>
<dt><b>LVHT_EX_GROUP_FOOTER</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b> The point is within the group footer.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_GROUP_COLLAPSE"></a><a id="lvht_ex_group_collapse"></a><dl>
<dt><b>LVHT_EX_GROUP_COLLAPSE</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b> The point is within the collapse/expand button of the group.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_GROUP_BACKGROUND"></a><a id="lvht_ex_group_background"></a><dl>
<dt><b>LVHT_EX_GROUP_BACKGROUND</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b> The point is within the area of the group where items are displayed.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_GROUP_STATEICON"></a><a id="lvht_ex_group_stateicon"></a><dl>
<dt><b>LVHT_EX_GROUP_STATEICON</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b>  The point is within the state icon of the group.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_GROUP_SUBSETLINK"></a><a id="lvht_ex_group_subsetlink"></a><dl>
<dt><b>LVHT_EX_GROUP_SUBSETLINK</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b> The point is within the subset link of the group.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_GROUP"></a><a id="lvht_ex_group"></a><dl>
<dt><b>LVHT_EX_GROUP</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b> LVHT_EX_GROUP_BACKGROUND | LVHT_EX_GROUP_COLLAPSE | LVHT_EX_GROUP_FOOTER | LVHT_EX_GROUP_HEADER | LVHT_EX_GROUP_STATEICON | LVHT_EX_GROUP_SUBSETLINK.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_ONCONTENTS"></a><a id="lvht_ex_oncontents"></a><dl>
<dt><b>LVHT_EX_ONCONTENTS</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b> The point is within the icon or text content of the item and not on the background.

</td>
</tr>
<tr>
<td width="40%"><a id="LVHT_EX_FOOTER"></a><a id="lvht_ex_footer"></a><dl>
<dt><b>LVHT_EX_FOOTER</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista.</b> The point is within the footer of the list-view control.

</td>
</tr>
</table>

### -field iItem

Type: <b>int</b>

Receives the index of the matching item. Or if hit-testing a subitem, this value represents the subitem's parent item.

### -field iSubItem

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.70</a>. Receives the index of the matching subitem. When hit-testing an item, this member will be zero.

### -field iGroup

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Windows Vista</a>. Group index of the item hit (read only). Valid only for owner data. If the point is within an item that is displayed in multiple groups then <b>iGroup</b> will specify the group index of the item.