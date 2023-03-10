---
UID: NS:commctrl.tagNMCUSTOMDRAWINFO
title: NMCUSTOMDRAW (commctrl.h)
description: Contains information specific to an NM_CUSTOMDRAW notification code.
helpviewer_keywords: ["*LPNMCUSTOMDRAW","CDDS_ITEM","CDDS_ITEMPOSTERASE","CDDS_ITEMPOSTPAINT","CDDS_ITEMPREERASE","CDDS_ITEMPREPAINT","CDDS_POSTERASE","CDDS_POSTPAINT","CDDS_PREERASE","CDDS_PREPAINT","CDDS_SUBITEM","CDIS_CHECKED","CDIS_DEFAULT","CDIS_DISABLED","CDIS_DROPHILITED","CDIS_FOCUS","CDIS_GRAYED","CDIS_HOT","CDIS_INDETERMINATE","CDIS_MARKED","CDIS_NEARHOT","CDIS_OTHERSIDEHOT","CDIS_SELECTED","CDIS_SHOWKEYBOARDCUES","Global Values:","Item-specific Values:","LPNMCUSTOMDRAW","LPNMCUSTOMDRAW structure pointer [Windows Controls]","NMCUSTOMDRAW","NMCUSTOMDRAW structure [Windows Controls]","_win32_NMCUSTOMDRAW","_win32_NMCUSTOMDRAW_cpp","commctrl/LPNMCUSTOMDRAW","commctrl/NMCUSTOMDRAW","controls.NMCUSTOMDRAW","controls._win32_NMCUSTOMDRAW"]
old-location: controls\NMCUSTOMDRAW.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\custdraw\structures\nmcustomdraw.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMCUSTOMDRAW, CDDS_ITEM, CDDS_ITEMPOSTERASE, CDDS_ITEMPOSTPAINT, CDDS_ITEMPREERASE, CDDS_ITEMPREPAINT, CDDS_POSTERASE, CDDS_POSTPAINT, CDDS_PREERASE, CDDS_PREPAINT, CDDS_SUBITEM, CDIS_CHECKED, CDIS_DEFAULT, CDIS_DISABLED, CDIS_DROPHILITED, CDIS_FOCUS, CDIS_GRAYED, CDIS_HOT, CDIS_INDETERMINATE, CDIS_MARKED, CDIS_NEARHOT, CDIS_OTHERSIDEHOT, CDIS_SELECTED, CDIS_SHOWKEYBOARDCUES, Global Values:, Item-specific Values:, LPNMCUSTOMDRAW, LPNMCUSTOMDRAW structure pointer [Windows Controls], NMCUSTOMDRAW, NMCUSTOMDRAW structure [Windows Controls], _win32_NMCUSTOMDRAW, _win32_NMCUSTOMDRAW_cpp, commctrl/LPNMCUSTOMDRAW, commctrl/NMCUSTOMDRAW, controls.NMCUSTOMDRAW, controls._win32_NMCUSTOMDRAW'
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
req.typenames: NMCUSTOMDRAW, *LPNMCUSTOMDRAW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMCUSTOMDRAWINFO
 - commctrl/tagNMCUSTOMDRAWINFO
 - LPNMCUSTOMDRAW
 - commctrl/LPNMCUSTOMDRAW
 - NMCUSTOMDRAW
 - commctrl/NMCUSTOMDRAW
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
 - NMCUSTOMDRAW
---

# NMCUSTOMDRAW structure


## -description

Contains information specific to an <a href="/windows/desktop/Controls/nm-customdraw">NM_CUSTOMDRAW</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification code.

### -field dwDrawStage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The current drawing stage. This is one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Global_Values_"></a><a id="global_values_"></a><a id="GLOBAL_VALUES_"></a><dl>
<dt><b>Global Values:</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="CDDS_POSTERASE"></a><a id="cdds_posterase"></a><dl>
<dt><b>CDDS_POSTERASE</b></dt>
</dl>
</td>
<td width="60%">
After the erasing cycle is complete.

</td>
</tr>
<tr>
<td width="40%"><a id="CDDS_POSTPAINT"></a><a id="cdds_postpaint"></a><dl>
<dt><b>CDDS_POSTPAINT</b></dt>
</dl>
</td>
<td width="60%">
After the painting cycle is complete.

</td>
</tr>
<tr>
<td width="40%"><a id="CDDS_PREERASE"></a><a id="cdds_preerase"></a><dl>
<dt><b>CDDS_PREERASE</b></dt>
</dl>
</td>
<td width="60%">
Before the erasing cycle begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CDDS_PREPAINT"></a><a id="cdds_prepaint"></a><dl>
<dt><b>CDDS_PREPAINT</b></dt>
</dl>
</td>
<td width="60%">
Before the painting cycle begins.



</td>
</tr>
<tr>
<td width="40%"><a id="Item-specific_Values_"></a><a id="item-specific_values_"></a><a id="ITEM-SPECIFIC_VALUES_"></a><dl>
<dt><b>Item-specific Values:</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id="CDDS_ITEM"></a><a id="cdds_item"></a><dl>
<dt><b>CDDS_ITEM</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <b>dwItemSpec</b>, 
						<b>uItemState</b>, and <b>lItemlParam</b> members are valid.

</td>
</tr>
<tr>
<td width="40%"><a id="CDDS_ITEMPOSTERASE"></a><a id="cdds_itemposterase"></a><dl>
<dt><b>CDDS_ITEMPOSTERASE</b></dt>
</dl>
</td>
<td width="60%">
After an item has been erased.

</td>
</tr>
<tr>
<td width="40%"><a id="CDDS_ITEMPOSTPAINT"></a><a id="cdds_itempostpaint"></a><dl>
<dt><b>CDDS_ITEMPOSTPAINT</b></dt>
</dl>
</td>
<td width="60%">
After an item has been drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="CDDS_ITEMPREERASE"></a><a id="cdds_itempreerase"></a><dl>
<dt><b>CDDS_ITEMPREERASE</b></dt>
</dl>
</td>
<td width="60%">
Before an item is erased.

</td>
</tr>
<tr>
<td width="40%"><a id="CDDS_ITEMPREPAINT"></a><a id="cdds_itemprepaint"></a><dl>
<dt><b>CDDS_ITEMPREPAINT</b></dt>
</dl>
</td>
<td width="60%">
Before an item is drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="CDDS_SUBITEM"></a><a id="cdds_subitem"></a><dl>
<dt><b>CDDS_SUBITEM</b></dt>
</dl>
</td>
<td width="60%">
Flag combined with CDDS_ITEMPREPAINT or CDDS_ITEMPOSTPAINT if a subitem is being drawn. This will only be set if <a href="/windows/desktop/Controls/cdrf-constants">CDRF_NOTIFYITEMDRAW</a> is returned from CDDS_PREPAINT.

</td>
</tr>
</table>

### -field hdc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

A handle to the control's device context. Use this HDC to perform any GDI functions.

### -field rc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

The <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes the bounding rectangle of the area being drawn. This member is initialized only by the CDDS_ITEMPREPAINT notification. <a href="/windows/desktop/Controls/common-control-versions">Version 5.80.</a> This member is also initialized by the CDDS_PREPAINT notification.

### -field dwItemSpec

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

The item number. What is contained in this member will depend on the type of control that is sending the notification. See the <a href="/windows/desktop/Controls/nm-customdraw">NM_CUSTOMDRAW</a> notification reference for the specific control to determine what, if anything, is contained in this member.

### -field uItemState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The current item state. This value is a combination of the following flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CDIS_CHECKED"></a><a id="cdis_checked"></a><dl>
<dt><b>CDIS_CHECKED</b></dt>
</dl>
</td>
<td width="60%">
The item is checked.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_DEFAULT"></a><a id="cdis_default"></a><dl>
<dt><b>CDIS_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The item is in its default state.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_DISABLED"></a><a id="cdis_disabled"></a><dl>
<dt><b>CDIS_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The item is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_FOCUS"></a><a id="cdis_focus"></a><dl>
<dt><b>CDIS_FOCUS</b></dt>
</dl>
</td>
<td width="60%">
The item is in focus.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_GRAYED"></a><a id="cdis_grayed"></a><dl>
<dt><b>CDIS_GRAYED</b></dt>
</dl>
</td>
<td width="60%">
The item is grayed.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_HOT"></a><a id="cdis_hot"></a><dl>
<dt><b>CDIS_HOT</b></dt>
</dl>
</td>
<td width="60%">
The item is currently under the pointer ("hot").

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_INDETERMINATE"></a><a id="cdis_indeterminate"></a><dl>
<dt><b>CDIS_INDETERMINATE</b></dt>
</dl>
</td>
<td width="60%">
The item is in an indeterminate state.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_MARKED"></a><a id="cdis_marked"></a><dl>
<dt><b>CDIS_MARKED</b></dt>
</dl>
</td>
<td width="60%">
The item is marked. The meaning of this is determined by the implementation.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_SELECTED"></a><a id="cdis_selected"></a><dl>
<dt><b>CDIS_SELECTED</b></dt>
</dl>
</td>
<td width="60%">
The item is selected.
                    

<div class="alert"><b>Note</b>  This flag does not work correctly for owner-drawn list-view controls that have the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_SHOWSELALWAYS</a> style. For these controls, you can determine whether an item is selected by using <a href="/windows/desktop/Controls/lvm-getitemstate">LVM_GETITEMSTATE</a> (or <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_getitemstate">ListView_GetItemState</a>) and checking for the <b>LVIS_SELECTED</b> flag.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_SHOWKEYBOARDCUES"></a><a id="cdis_showkeyboardcues"></a><dl>
<dt><b>CDIS_SHOWKEYBOARDCUES</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/Controls/common-control-versions">Version 6.0.</a>The item is showing its keyboard cues. 

                        

Note that Comctl32 version 6 is not redistributable. operating systems. To use Comctl32.dll version 6, specify it in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_NEARHOT"></a><a id="cdis_nearhot"></a><dl>
<dt><b>CDIS_NEARHOT</b></dt>
</dl>
</td>
<td width="60%">
The item is part of a control that is currently under the mouse pointer ("hot"), but the item is not "hot" itself.  The meaning of this is determined by the implementation.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_OTHERSIDEHOT"></a><a id="cdis_othersidehot"></a><dl>
<dt><b>CDIS_OTHERSIDEHOT</b></dt>
</dl>
</td>
<td width="60%">
The item is part of a splitbutton that is currently under the mouse pointer ("hot"), but the item is not "hot" itself.  The meaning of this is determined by the implementation.

</td>
</tr>
<tr>
<td width="40%"><a id="CDIS_DROPHILITED"></a><a id="cdis_drophilited"></a><dl>
<dt><b>CDIS_DROPHILITED</b></dt>
</dl>
</td>
<td width="60%">
The item is currently the drop target of a drag-and-drop operation.

</td>
</tr>
</table>

### -field lItemlParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined item data.

## -remarks

The value your application returns depends on the current drawing stage. The <b>dwDrawStage</b> member of the associated <b>NMCUSTOMDRAW</b> structure holds a value that specifies the drawing stage. When the <b>dwDrawStage</b> member equals CDDS_PREPAINT and CDDS_PREERASE, some controls send the CDDS_PREERASE message first and expect the return value to indicate which subsequent messages will be sent. For a code sample that illustrates states and drawing stages, see <a href="/windows/desktop/Controls/custom-draw">Customizing a Control's Appearance Using Custom Draw</a>.