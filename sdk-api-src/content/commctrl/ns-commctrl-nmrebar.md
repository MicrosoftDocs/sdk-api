---
UID: NS:commctrl.tagNMREBAR
title: NMREBAR (commctrl.h)
description: Contains information used in handling various rebar notifications.
helpviewer_keywords: ["*LPNMREBAR","LPNMREBAR","LPNMREBAR structure pointer [Windows Controls]","NMREBAR","NMREBAR structure [Windows Controls]","RBNM_ID","RBNM_LPARAM","RBNM_STYLE","_win32_NMREBAR","_win32_NMREBAR_cpp","commctrl/LPNMREBAR","commctrl/NMREBAR","controls.NMREBAR","controls._win32_NMREBAR"]
old-location: controls\NMREBAR.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\rebar\structures\nmrebar.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMREBAR, LPNMREBAR, LPNMREBAR structure pointer [Windows Controls], NMREBAR, NMREBAR structure [Windows Controls], RBNM_ID, RBNM_LPARAM, RBNM_STYLE, _win32_NMREBAR, _win32_NMREBAR_cpp, commctrl/LPNMREBAR, commctrl/NMREBAR, controls.NMREBAR, controls._win32_NMREBAR'
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
req.typenames: NMREBAR, *LPNMREBAR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMREBAR
 - commctrl/tagNMREBAR
 - LPNMREBAR
 - commctrl/LPNMREBAR
 - NMREBAR
 - commctrl/NMREBAR
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
 - NMREBAR
---

# NMREBAR structure


## -description

Contains information used in handling various rebar notifications.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field dwMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Set of flags that define which members of this structure contain valid information. This can be one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RBNM_ID"></a><a id="rbnm_id"></a><dl>
<dt><b>RBNM_ID</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>wID</b> member contains valid information. 

</td>
</tr>
<tr>
<td width="40%"><a id="RBNM_LPARAM"></a><a id="rbnm_lparam"></a><dl>
<dt><b>RBNM_LPARAM</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>lParam</b> member contains valid information. 

</td>
</tr>
<tr>
<td width="40%"><a id="RBNM_STYLE"></a><a id="rbnm_style"></a><dl>
<dt><b>RBNM_STYLE</b></dt>
</dl>
</td>
<td width="60%">
The 
						<b>fStyle</b> member contains valid information. 

</td>
</tr>
</table>

### -field uBand

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Zero-based index of the band affected by the notification. This will be -1 if no band is affected.

### -field fStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The style of the band. This is one or more of the RBBS_ styles detailed in the 
					<b>fStyle</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-rebarbandinfoa">REBARBANDINFO</a> structure. This member is only valid if 
					<b>dwMask</b> contains RBNM_STYLE.

### -field wID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Application-defined identifier of the band. This member is only valid if 
					<b>dwMask</b> contains RBNM_ID.

### -field lParam

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined value associated with the band. This member is only valid if 
					<b>dwMask</b> contains RBNM_LPARAM.