---
UID: NS:commctrl.tagNMLVCUSTOMDRAW
title: NMLVCUSTOMDRAW (commctrl.h)
description: Contains information specific to an NM_CUSTOMDRAW (list view) notification code sent by a list-view control.
helpviewer_keywords: ["*LPNMLVCUSTOMDRAW","LPNMLVCUSTOMDRAW","LPNMLVCUSTOMDRAW structure pointer [Windows Controls]","LVCDI_GROUP","LVCDI_ITEM","LVCDI_ITEMSLIST","LVGA_HEADER_CENTER","LVGA_HEADER_LEFT","LVGA_HEADER_RIGHT","NMLVCUSTOMDRAW","NMLVCUSTOMDRAW structure [Windows Controls]","_win32_NMLVCUSTOMDRAW","_win32_NMLVCUSTOMDRAW_cpp","commctrl/LPNMLVCUSTOMDRAW","commctrl/NMLVCUSTOMDRAW","controls.NMLVCUSTOMDRAW","controls._win32_NMLVCUSTOMDRAW"]
old-location: controls\NMLVCUSTOMDRAW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvcustomdraw.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMLVCUSTOMDRAW, LPNMLVCUSTOMDRAW, LPNMLVCUSTOMDRAW structure pointer [Windows Controls], LVCDI_GROUP, LVCDI_ITEM, LVCDI_ITEMSLIST, LVGA_HEADER_CENTER, LVGA_HEADER_LEFT, LVGA_HEADER_RIGHT, NMLVCUSTOMDRAW, NMLVCUSTOMDRAW structure [Windows Controls], _win32_NMLVCUSTOMDRAW, _win32_NMLVCUSTOMDRAW_cpp, commctrl/LPNMLVCUSTOMDRAW, commctrl/NMLVCUSTOMDRAW, controls.NMLVCUSTOMDRAW, controls._win32_NMLVCUSTOMDRAW'
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
req.typenames: NMLVCUSTOMDRAW, *LPNMLVCUSTOMDRAW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMLVCUSTOMDRAW
 - commctrl/tagNMLVCUSTOMDRAW
 - LPNMLVCUSTOMDRAW
 - commctrl/LPNMLVCUSTOMDRAW
 - NMLVCUSTOMDRAW
 - commctrl/NMLVCUSTOMDRAW
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
 - NMLVCUSTOMDRAW
---

# NMLVCUSTOMDRAW structure


## -description

Contains information specific to an <a href="/windows/desktop/Controls/nm-customdraw-list-view">NM_CUSTOMDRAW (list view)</a> notification code sent by a list-view control.

## -struct-fields

### -field nmcd

Type: <b><a href="/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw">NMCUSTOMDRAW</a></b>


<a href="/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw">NMCUSTOMDRAW</a> structure that contains general custom draw information.

### -field clrText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

<b>COLORREF</b> value representing the color that will be used to display text foreground in the list-view control.

### -field clrTextBk

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

<b>COLORREF</b> value representing the color that will be used to display text background in the list-view control. In <a href="/windows/desktop/Controls/common-control-versions">Version 6.0., </a> this member is ignored if the background image is set with the <a href="/windows/desktop/Controls/lvm-setbkimage">LVM_SETBKIMAGE</a> message.

### -field iSubItem

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 4.71.</a> Index of the subitem that is being drawn. If the main item is being drawn, this member will be zero.

### -field dwItemType

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0. </a> 
					<b>DWORD</b> that contains the type of the item to draw. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVCDI_ITEM"></a><a id="lvcdi_item"></a><dl>
<dt><b>LVCDI_ITEM</b></dt>
</dl>
</td>
<td width="60%">
An item is to be drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCDI_GROUP"></a><a id="lvcdi_group"></a><dl>
<dt><b>LVCDI_GROUP</b></dt>
</dl>
</td>
<td width="60%">
A group is to be drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="LVCDI_ITEMSLIST"></a><a id="lvcdi_itemslist"></a><dl>
<dt><b>LVCDI_ITEMSLIST</b></dt>
</dl>
</td>
<td width="60%">
Every item is to be drawn.

</td>
</tr>
</table>

### -field clrFace

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0.</a> 
					<b>COLORREF</b> value representing the color that will be used to display the face of an item.

### -field iIconEffect

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0.</a>  
					Value of type <b>int</b> that specifies the effect that is applied to an icon, such as Glow, Shadow, or Pulse.

### -field iIconPhase

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0.</a>  
					Value of type <b>int</b> that specifies the phase of an icon.

### -field iPartId

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0.</a>  
					Value of type <b>int</b> that specifies the ID of the part of an item to draw.

### -field iStateId

Type: <b>int</b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0.</a>  
					Value of type <b>int</b> that specifies the ID of the state of an item to draw.

### -field rcText

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0.</a>  
					<b>RECT</b> that specifies the rectangle in which the text is to be drawn.

### -field uAlign

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="/windows/desktop/Controls/common-control-versions">Version 6.0.</a>  
					<b>UINT</b> that specifies how a group should be aligned. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVGA_HEADER_CENTER"></a><a id="lvga_header_center"></a><dl>
<dt><b>LVGA_HEADER_CENTER</b></dt>
</dl>
</td>
<td width="60%">
Center the group.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGA_HEADER_LEFT"></a><a id="lvga_header_left"></a><dl>
<dt><b>LVGA_HEADER_LEFT</b></dt>
</dl>
</td>
<td width="60%">
Align the group on the left.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGA_HEADER_RIGHT"></a><a id="lvga_header_right"></a><dl>
<dt><b>LVGA_HEADER_RIGHT</b></dt>
</dl>
</td>
<td width="60%">
Align the group on the right.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  Comctl32.dll version 6 is not redistributable but it is included in Windows XP or later. To use Comctl32.dll version 6, specify it in a manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>
