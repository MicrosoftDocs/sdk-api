---
UID: NS:winuser.tagDRAWITEMSTRUCT
title: DRAWITEMSTRUCT (winuser.h)
description: Provides information that the owner window uses to determine how to paint an owner-drawn control or menu item.
helpviewer_keywords: ["*LPDRAWITEMSTRUCT","*PDRAWITEMSTRUCT","DRAWITEMSTRUCT","DRAWITEMSTRUCT structure [Windows Controls]","ODA_DRAWENTIRE","ODA_FOCUS","ODA_SELECT","ODS_CHECKED","ODS_COMBOBOXEDIT","ODS_DEFAULT","ODS_DISABLED","ODS_FOCUS","ODS_GRAYED","ODS_HOTLIGHT","ODS_INACTIVE","ODS_NOACCEL","ODS_NOFOCUSRECT","ODS_SELECTED","ODT_BUTTON","ODT_COMBOBOX","ODT_LISTBOX","ODT_LISTVIEW","ODT_MENU","ODT_STATIC","ODT_TAB","_win32_DRAWITEMSTRUCT_str","_win32_DRAWITEMSTRUCT_str_cpp","controls.DRAWITEMSTRUCT","controls._win32_DRAWITEMSTRUCT_str","winuser/DRAWITEMSTRUCT"]
old-location: controls\DRAWITEMSTRUCT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxstructures\drawitemstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPDRAWITEMSTRUCT, *PDRAWITEMSTRUCT, DRAWITEMSTRUCT, DRAWITEMSTRUCT structure [Windows Controls], ODA_DRAWENTIRE, ODA_FOCUS, ODA_SELECT, ODS_CHECKED, ODS_COMBOBOXEDIT, ODS_DEFAULT, ODS_DISABLED, ODS_FOCUS, ODS_GRAYED, ODS_HOTLIGHT, ODS_INACTIVE, ODS_NOACCEL, ODS_NOFOCUSRECT, ODS_SELECTED, ODT_BUTTON, ODT_COMBOBOX, ODT_LISTBOX, ODT_LISTVIEW, ODT_MENU, ODT_STATIC, ODT_TAB, _win32_DRAWITEMSTRUCT_str, _win32_DRAWITEMSTRUCT_str_cpp, controls.DRAWITEMSTRUCT, controls._win32_DRAWITEMSTRUCT_str, winuser/DRAWITEMSTRUCT'
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: DRAWITEMSTRUCT, *PDRAWITEMSTRUCT, *LPDRAWITEMSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDRAWITEMSTRUCT
 - winuser/tagDRAWITEMSTRUCT
 - PDRAWITEMSTRUCT
 - winuser/PDRAWITEMSTRUCT
 - DRAWITEMSTRUCT
 - winuser/DRAWITEMSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - DRAWITEMSTRUCT
---

# DRAWITEMSTRUCT structure


## -description

Provides information that the owner window uses to determine how to paint an owner-drawn control or menu item. The owner window of the owner-drawn control or menu item receives a pointer to this structure as the <i>lParam</i> parameter of the <a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a> message.

## -struct-fields

### -field CtlType

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The control type. This member can be one of the following values. See Remarks.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ODT_BUTTON"></a><a id="odt_button"></a><dl>
<dt><b>ODT_BUTTON</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn button

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_COMBOBOX"></a><a id="odt_combobox"></a><dl>
<dt><b>ODT_COMBOBOX</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn combo box

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_LISTBOX"></a><a id="odt_listbox"></a><dl>
<dt><b>ODT_LISTBOX</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn list box

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_LISTVIEW"></a><a id="odt_listview"></a><dl>
<dt><b>ODT_LISTVIEW</b></dt>
</dl>
</td>
<td width="60%">
List-view control

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_MENU"></a><a id="odt_menu"></a><dl>
<dt><b>ODT_MENU</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn menu item

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_STATIC"></a><a id="odt_static"></a><dl>
<dt><b>ODT_STATIC</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn static control

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_TAB"></a><a id="odt_tab"></a><dl>
<dt><b>ODT_TAB</b></dt>
</dl>
</td>
<td width="60%">
Tab control

</td>
</tr>
</table>

### -field CtlID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The identifier of the combo box, list box, button, or static control. This member is not used for a menu item.

### -field itemID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The menu item identifier for a menu item or the index of the item in a list box or combo box. For an empty list box or combo box, this member can be <code>-1</code>. This allows the application to draw only the focus rectangle at the coordinates specified by the <b>rcItem</b> member even though there are no items in the control. This indicates to the user whether the list box or combo box has the focus. How the bits are set in the <b>itemAction</b> member determines whether the rectangle is to be drawn as though the list box or combo box has the focus.

### -field itemAction

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The required drawing action. This member can be one or more of the values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ODA_DRAWENTIRE"></a><a id="oda_drawentire"></a><dl>
<dt><b>ODA_DRAWENTIRE</b></dt>
</dl>
</td>
<td width="60%">
The entire control needs to be drawn.

</td>
</tr>
<tr>
<td width="40%"><a id="ODA_FOCUS"></a><a id="oda_focus"></a><dl>
<dt><b>ODA_FOCUS</b></dt>
</dl>
</td>
<td width="60%">
The control has lost or gained the keyboard focus. The <b>itemState</b> member should be checked to determine whether the control has the focus.

</td>
</tr>
<tr>
<td width="40%"><a id="ODA_SELECT"></a><a id="oda_select"></a><dl>
<dt><b>ODA_SELECT</b></dt>
</dl>
</td>
<td width="60%">
The selection status has changed. The <b>itemState</b> member should be checked to determine the new selection state.

</td>
</tr>
</table>

### -field itemState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The visual state of the item after the current drawing action takes place. This member can be a combination of the values shown in the following table. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ODS_CHECKED"></a><a id="ods_checked"></a><dl>
<dt><b>ODS_CHECKED</b></dt>
</dl>
</td>
<td width="60%">
The menu item is to be checked. This bit is used only in a menu.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_COMBOBOXEDIT"></a><a id="ods_comboboxedit"></a><dl>
<dt><b>ODS_COMBOBOXEDIT</b></dt>
</dl>
</td>
<td width="60%">
The drawing takes place in the selection field (edit control) of an owner-drawn combo box.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_DEFAULT"></a><a id="ods_default"></a><dl>
<dt><b>ODS_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
The item is the default item.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_DISABLED"></a><a id="ods_disabled"></a><dl>
<dt><b>ODS_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The item is to be drawn as disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_FOCUS"></a><a id="ods_focus"></a><dl>
<dt><b>ODS_FOCUS</b></dt>
</dl>
</td>
<td width="60%">
The item has the keyboard focus.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_GRAYED"></a><a id="ods_grayed"></a><dl>
<dt><b>ODS_GRAYED</b></dt>
</dl>
</td>
<td width="60%">
The item is to be grayed. This bit is used only in a menu.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_HOTLIGHT"></a><a id="ods_hotlight"></a><dl>
<dt><b>ODS_HOTLIGHT</b></dt>
</dl>
</td>
<td width="60%">
The item is being hot-tracked, that is, the item will be highlighted when the mouse is on the item.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_INACTIVE"></a><a id="ods_inactive"></a><dl>
<dt><b>ODS_INACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The item is inactive and the window associated with the menu is inactive.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_NOACCEL"></a><a id="ods_noaccel"></a><dl>
<dt><b>ODS_NOACCEL</b></dt>
</dl>
</td>
<td width="60%">
The control is drawn without the keyboard accelerator cues.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_NOFOCUSRECT"></a><a id="ods_nofocusrect"></a><dl>
<dt><b>ODS_NOFOCUSRECT</b></dt>
</dl>
</td>
<td width="60%">
The control is drawn without focus indicator cues.

</td>
</tr>
<tr>
<td width="40%"><a id="ODS_SELECTED"></a><a id="ods_selected"></a><dl>
<dt><b>ODS_SELECTED</b></dt>
</dl>
</td>
<td width="60%">
The menu item's status is selected.

</td>
</tr>
</table>

### -field hwndItem

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control for combo boxes, list boxes, buttons, and static controls. For menus, this member is a handle to the menu that contains the item.

### -field hDC

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HDC</a></b>

A handle to a device context; this device context must be used when performing drawing operations on the control.

### -field rcItem

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

A rectangle that defines the boundaries of the control to be drawn. This rectangle is in the device context specified by the <b>hDC</b> member. The system automatically clips anything that the owner window draws in the device context for combo boxes, list boxes, and buttons, but does not clip menu items. When drawing menu items, the owner window must not draw outside the boundaries of the rectangle defined by the <b>rcItem</b> member.

### -field itemData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG_PTR</a></b>

The application-defined value associated with the menu item. For a control, this parameter specifies the value last assigned to the list box or combo box by the <a href="/windows/desktop/Controls/lb-setitemdata">LB_SETITEMDATA</a> or <a href="/windows/desktop/Controls/cb-setitemdata">CB_SETITEMDATA</a> message. If the list box or combo box has the <a href="/windows/desktop/Controls/list-box-styles">LBS_HASSTRINGS</a> or <a href="/windows/desktop/Controls/combo-box-styles">CBS_HASSTRINGS</a> style, this value is initially zero. Otherwise, this value is initially the value that was passed to the list box or combo box in the <i>lParam</i> parameter of one of the following messages: 
					

<ul>
<li>
<a href="/windows/desktop/Controls/cb-addstring">CB_ADDSTRING</a>
</li>
<li>
<a href="/windows/desktop/Controls/cb-insertstring">CB_INSERTSTRING</a>
</li>
<li>
<a href="/windows/desktop/Controls/lb-addstring">LB_ADDSTRING</a>
</li>
<li>
<a href="/windows/desktop/Controls/lb-insertstring">LB_INSERTSTRING</a>
</li>
</ul>
If <b>CtlType</b> is <b>ODT_BUTTON</b> or <b>ODT_STATIC</b>, <b>itemData</b> is zero.

## -remarks

Some control types, such as status bars, do not set the value of <b>CtlType</b>.

## -see-also

<a href="/windows/desktop/Controls/cb-addstring">CB_ADDSTRING</a>



<a href="/windows/desktop/Controls/cb-insertstring">CB_INSERTSTRING</a>



<a href="/windows/desktop/Controls/cb-setitemdata">CB_SETITEMDATA</a>



<a href="/windows/desktop/Controls/lb-addstring">LB_ADDSTRING</a>



<a href="/windows/desktop/Controls/lb-insertstring">LB_INSERTSTRING</a>



<a href="/windows/desktop/Controls/lb-setitemdata">LB_SETITEMDATA</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/wm-drawitem">WM_DRAWITEM</a>