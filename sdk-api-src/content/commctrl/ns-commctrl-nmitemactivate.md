---
UID: NS:commctrl.tagNMITEMACTIVATE
title: NMITEMACTIVATE (commctrl.h)
description: Contains information about an LVN_ITEMACTIVATE notification code.
helpviewer_keywords: ["*LPNMITEMACTIVATE","LPNMITEMACTIVATE","LPNMITEMACTIVATE structure pointer [Windows Controls]","LVKF_ALT","LVKF_CONTROL","LVKF_SHIFT","NMITEMACTIVATE","NMITEMACTIVATE structure [Windows Controls]","_win32_NMITEMACTIVATE","_win32_NMITEMACTIVATE_cpp","commctrl/LPNMITEMACTIVATE","commctrl/NMITEMACTIVATE","controls.NMITEMACTIVATE","controls._win32_NMITEMACTIVATE"]
old-location: controls\NMITEMACTIVATE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmitemactivate.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMITEMACTIVATE, LPNMITEMACTIVATE, LPNMITEMACTIVATE structure pointer [Windows Controls], LVKF_ALT, LVKF_CONTROL, LVKF_SHIFT, NMITEMACTIVATE, NMITEMACTIVATE structure [Windows Controls], _win32_NMITEMACTIVATE, _win32_NMITEMACTIVATE_cpp, commctrl/LPNMITEMACTIVATE, commctrl/NMITEMACTIVATE, controls.NMITEMACTIVATE, controls._win32_NMITEMACTIVATE'
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
req.typenames: NMITEMACTIVATE, *LPNMITEMACTIVATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMITEMACTIVATE
 - commctrl/tagNMITEMACTIVATE
 - LPNMITEMACTIVATE
 - commctrl/LPNMITEMACTIVATE
 - NMITEMACTIVATE
 - commctrl/NMITEMACTIVATE
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
 - NMITEMACTIVATE
---

# NMITEMACTIVATE structure


## -description

Contains information about an <a href="/windows/desktop/Controls/lvn-itemactivate">LVN_ITEMACTIVATE</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification code.

### -field iItem

Type: <b>int</b>

Index of the list-view item. If the item index is not used for the notification, this member will contain -1.

### -field iSubItem

Type: <b>int</b>

One-based index of the subitem. If the subitem index is not used for the notification or the notification does not apply to a subitem, this member will contain zero.

### -field uNewState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

New item state. This member is zero for notification codes that do not use it.

### -field uOldState

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Old item state. This member is zero for notification codes that do not use it.

### -field uChanged

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Set of flags that indicate the item attributes that have changed. This member is zero for notifications that do not use it. Otherwise, it can have the same values as the 
					<b>mask</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure.

### -field ptAction

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>


<a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that indicates the location at which the event occurred, in client coordinates. This member is undefined for notification codes that do not use it.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined value of the item. This member is undefined for notification codes that do not use it.

### -field uKeyFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Modifier keys that were pressed at the time of the activation. This member contains zero or a combination of the following flags: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVKF_ALT"></a><a id="lvkf_alt"></a><dl>
<dt><b>LVKF_ALT</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVKF_CONTROL"></a><a id="lvkf_control"></a><dl>
<dt><b>LVKF_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVKF_SHIFT"></a><a id="lvkf_shift"></a><dl>
<dt><b>LVKF_SHIFT</b></dt>
</dl>
</td>
<td width="60%">
The  key is pressed. 

</td>
</tr>
</table>