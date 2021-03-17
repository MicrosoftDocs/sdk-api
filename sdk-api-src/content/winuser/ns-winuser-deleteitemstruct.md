---
UID: NS:winuser.tagDELETEITEMSTRUCT
title: DELETEITEMSTRUCT (winuser.h)
description: Describes a deleted list box or combo box item.
helpviewer_keywords: ["*LPDELETEITEMSTRUCT","*PDELETEITEMSTRUCT","DELETEITEMSTRUCT","DELETEITEMSTRUCT structure [Windows Controls]","ODT_COMBOBOX","ODT_LISTBOX","PDELETEITEMSTRUCT","PDELETEITEMSTRUCT structure pointer [Windows Controls]","_win32_DELETEITEMSTRUCT_str","_win32_DELETEITEMSTRUCT_str_cpp","controls.DELETEITEMSTRUCT","controls._win32_DELETEITEMSTRUCT_str","winuser/DELETEITEMSTRUCT","winuser/PDELETEITEMSTRUCT"]
old-location: controls\DELETEITEMSTRUCT.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxstructures\deleteitemstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPDELETEITEMSTRUCT, *PDELETEITEMSTRUCT, DELETEITEMSTRUCT, DELETEITEMSTRUCT structure [Windows Controls], ODT_COMBOBOX, ODT_LISTBOX, PDELETEITEMSTRUCT, PDELETEITEMSTRUCT structure pointer [Windows Controls], _win32_DELETEITEMSTRUCT_str, _win32_DELETEITEMSTRUCT_str_cpp, controls.DELETEITEMSTRUCT, controls._win32_DELETEITEMSTRUCT_str, winuser/DELETEITEMSTRUCT, winuser/PDELETEITEMSTRUCT'
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
req.typenames: DELETEITEMSTRUCT, *PDELETEITEMSTRUCT, *LPDELETEITEMSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDELETEITEMSTRUCT
 - winuser/tagDELETEITEMSTRUCT
 - PDELETEITEMSTRUCT
 - winuser/PDELETEITEMSTRUCT
 - DELETEITEMSTRUCT
 - winuser/DELETEITEMSTRUCT
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
 - DELETEITEMSTRUCT
---

# DELETEITEMSTRUCT structure


## -description

Describes a deleted list box or combo box item. The <i>lParam</i> parameter of a <a href="/windows/desktop/Controls/wm-deleteitem">WM_DELETEITEM</a> message contains a pointer to this structure. When an item is removed from a list box or combo box or when a list box or combo box is destroyed, the system sends the <b>WM_DELETEITEM</b> message to the owner for each deleted item. 


The system sends a <a href="/windows/desktop/Controls/wm-deleteitem">WM_DELETEITEM</a> message only for items deleted from an owner-drawn list box (with the <a href="/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWFIXED</a> or <a href="/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWVARIABLE</a> style) or owner-drawn combo box (with the <a href="/windows/desktop/Controls/combo-box-styles">CBS_OWNERDRAWFIXED</a> or <a href="/windows/desktop/Controls/combo-box-styles">CBS_OWNERDRAWVARIABLE</a> style).

## -struct-fields

### -field CtlType

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies whether the item was deleted from a list box or a combo box. One of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ODT_LISTBOX"></a><a id="odt_listbox"></a><dl>
<dt><b>ODT_LISTBOX</b></dt>
</dl>
</td>
<td width="60%">
A list box.

</td>
</tr>
<tr>
<td width="40%"><a id="ODT_COMBOBOX"></a><a id="odt_combobox"></a><dl>
<dt><b>ODT_COMBOBOX</b></dt>
</dl>
</td>
<td width="60%">
A combo box.

</td>
</tr>
</table>

### -field CtlID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The identifier of the list box or combo box.

### -field itemID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the item in the list box or combo box being removed.

### -field hwndItem

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -field itemData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG_PTR</a></b>

Application-defined data for the item. This value is passed to the control in the <i>lParam</i> parameter of the message that adds the item to the list box or combo box.

## -see-also

<a href="/windows/desktop/Controls/wm-deleteitem">WM_DELETEITEM</a>