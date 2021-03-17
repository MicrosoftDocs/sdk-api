---
UID: NS:winuser.tagMEASUREITEMSTRUCT
title: MEASUREITEMSTRUCT (winuser.h)
description: Informs the system of the dimensions of an owner-drawn control or menu item. This allows the system to process user interaction with the control correctly.
helpviewer_keywords: ["*LPMEASUREITEMSTRUCT","*PMEASUREITEMSTRUCT","MEASUREITEMSTRUCT","MEASUREITEMSTRUCT structure [Windows Controls]","ODT_COMBOBOX","ODT_LISTBOX","ODT_LISTVIEW","ODT_MENU","_win32_MEASUREITEMSTRUCT_str","_win32_MEASUREITEMSTRUCT_str_cpp","controls.MEASUREITEMSTRUCT","controls._win32_MEASUREITEMSTRUCT_str","winuser/MEASUREITEMSTRUCT"]
old-location: controls\MEASUREITEMSTRUCT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxstructures\measureitemstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPMEASUREITEMSTRUCT, *PMEASUREITEMSTRUCT, MEASUREITEMSTRUCT, MEASUREITEMSTRUCT structure [Windows Controls], ODT_COMBOBOX, ODT_LISTBOX, ODT_LISTVIEW, ODT_MENU, _win32_MEASUREITEMSTRUCT_str, _win32_MEASUREITEMSTRUCT_str_cpp, controls.MEASUREITEMSTRUCT, controls._win32_MEASUREITEMSTRUCT_str, winuser/MEASUREITEMSTRUCT'
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
req.typenames: MEASUREITEMSTRUCT, *PMEASUREITEMSTRUCT, *LPMEASUREITEMSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMEASUREITEMSTRUCT
 - winuser/tagMEASUREITEMSTRUCT
 - PMEASUREITEMSTRUCT
 - winuser/PMEASUREITEMSTRUCT
 - MEASUREITEMSTRUCT
 - winuser/MEASUREITEMSTRUCT
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
 - MEASUREITEMSTRUCT
---

# MEASUREITEMSTRUCT structure


## -description

Informs the system of the dimensions of an owner-drawn control or menu item. This allows the system to process user interaction with the control correctly.

## -struct-fields

### -field CtlType

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The control type. This member can be one of the values shown in the following table. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
Owner-draw list-view control

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_MENU"></a><a id="odt_menu"></a><dl>
<dt><b>ODT_MENU</b></dt>
</dl>
</td>
<td width="60%">
Owner-drawn menu

</td>
</tr>
</table>

### -field CtlID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The identifier of the combo box or list box. This member is not used for a menu.

### -field itemID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The identifier for a menu item or the position of a list box or combo box item. This value is specified for a list box only if it has the <a href="/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWVARIABLE</a> style; this value is specified for a combo box only if it has the <a href="/windows/desktop/Controls/combo-box-styles">CBS_OWNERDRAWVARIABLE</a> style.

### -field itemWidth

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The width, in pixels, of a menu item. Before returning from the message, the owner of the owner-drawn menu item must fill this member.

### -field itemHeight

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The height, in pixels, of an individual item in a list box or a menu. Before returning from the message, the owner of the owner-drawn combo box, list box, or menu item must fill out this member.

### -field itemData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG_PTR</a></b>

The application-defined value associated with the menu item. For a control, this member specifies the value last assigned to the list box or combo box by the <a href="/windows/desktop/Controls/lb-setitemdata">LB_SETITEMDATA</a> or <a href="/windows/desktop/Controls/cb-setitemdata">CB_SETITEMDATA</a> message. If the list box or combo box has the LB_HASSTRINGS or CB_HASSTRINGS style, this value is initially zero. Otherwise, this value is initially the value passed to the list box or combo box in the 
					<i>lParam</i> parameter of one of the following messages: 
					

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

## -remarks

The owner window of an owner-drawn control receives a pointer to the <b>MEASUREITEMSTRUCT</b> structure as the <i>lParam</i> parameter of a <a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a> message. The owner-drawn control sends this message to its owner window when the control is created. The owner then fills in the appropriate members in the structure for the control and returns. This structure is common to all owner-drawn controls except the owner-drawn button control whose size is predetermined by its window. 

If an application does not fill the appropriate members of <b>MEASUREITEMSTRUCT</b>, the control or menu item may not be drawn properly.

## -see-also

<a href="/windows/desktop/Controls/cb-addstring">CB_ADDSTRING</a>



<a href="/windows/desktop/Controls/cb-insertstring">CB_INSERTSTRING</a>



<a href="/windows/desktop/Controls/cb-setitemdata">CB_SETITEMDATA</a>



<a href="/windows/desktop/Controls/lb-addstring">LB_ADDSTRING</a>



<a href="/windows/desktop/Controls/lb-insertstring">LB_INSERTSTRING</a>



<a href="/windows/desktop/Controls/lb-setitemdata">LB_SETITEMDATA</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/wm-measureitem">WM_MEASUREITEM</a>