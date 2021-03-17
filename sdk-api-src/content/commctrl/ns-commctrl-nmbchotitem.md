---
UID: NS:commctrl.tagNMBCHOTITEM
title: NMBCHOTITEM (commctrl.h)
description: Contains information about the movement of the mouse over a button control.
helpviewer_keywords: ["*LPNMBCHOTITEM","HICF_ENTERING","HICF_LEAVING","LPNMBCHOTITEM","LPNMBCHOTITEM structure pointer [Windows Controls]","NMBCHOTITEM","NMBCHOTITEM structure [Windows Controls]","_win32_NMBCHOTITEM_str","_win32_NMBCHOTITEM_str_cpp","commctrl/LPNMBCHOTITEM","commctrl/NMBCHOTITEM","controls.NMBCHOTITEM","controls._win32_NMBCHOTITEM_str"]
old-location: controls\NMBCHOTITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonstructures\nmbchotitem.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMBCHOTITEM, HICF_ENTERING, HICF_LEAVING, LPNMBCHOTITEM, LPNMBCHOTITEM structure pointer [Windows Controls], NMBCHOTITEM, NMBCHOTITEM structure [Windows Controls], _win32_NMBCHOTITEM_str, _win32_NMBCHOTITEM_str_cpp, commctrl/LPNMBCHOTITEM, commctrl/NMBCHOTITEM, controls.NMBCHOTITEM, controls._win32_NMBCHOTITEM_str'
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
req.typenames: NMBCHOTITEM, *LPNMBCHOTITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMBCHOTITEM
 - commctrl/tagNMBCHOTITEM
 - LPNMBCHOTITEM
 - commctrl/LPNMBCHOTITEM
 - NMBCHOTITEM
 - commctrl/NMBCHOTITEM
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
 - NMBCHOTITEM
---

# NMBCHOTITEM structure


## -description

Contains information about the movement of the mouse over a button control.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The action of the mouse. This parameter can be one of the following values combined with HICF_MOUSE. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HICF_ENTERING"></a><a id="hicf_entering"></a><dl>
<dt><b>HICF_ENTERING</b></dt>
</dl>
</td>
<td width="60%">
The mouse is entering the button.

</td>
</tr>
<tr>
<td width="40%"><a id="HICF_LEAVING"></a><a id="hicf_leaving"></a><dl>
<dt><b>HICF_LEAVING</b></dt>
</dl>
</td>
<td width="60%">
The mouse is leaving the button.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Controls/bcn-hotitemchange">BCN_HOTITEMCHANGE</a>



<a href="/windows/desktop/Controls/buttons">Buttons</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a>



<b>Reference</b>