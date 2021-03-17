---
UID: NS:commctrl.tagNMPGHOTITEM
title: NMPGHOTITEM (commctrl.h)
description: Contains information used with the PGN_HOTITEMCHANGE notification code.
helpviewer_keywords: ["*LPNMPGHOTITEM","LPNMPGHOTITEM","LPNMPGHOTITEM structure pointer [Windows Controls]","NMPGHOTITEM","NMPGHOTITEM structure [Windows Controls]","commctrl/LPNMPGHOTITEM","commctrl/NMPGHOTITEM","controls.NMPGHOTITEM","controls.inet_NMPGHOTITEM","inet_NMPGHOTITEM","inet_NMPGHOTITEM_cpp"]
old-location: controls\NMPGHOTITEM.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\structures\nmpghotitem.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMPGHOTITEM, LPNMPGHOTITEM, LPNMPGHOTITEM structure pointer [Windows Controls], NMPGHOTITEM, NMPGHOTITEM structure [Windows Controls], commctrl/LPNMPGHOTITEM, commctrl/NMPGHOTITEM, controls.NMPGHOTITEM, controls.inet_NMPGHOTITEM, inet_NMPGHOTITEM, inet_NMPGHOTITEM_cpp'
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
req.typenames: NMPGHOTITEM, *LPNMPGHOTITEM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMPGHOTITEM
 - commctrl/tagNMPGHOTITEM
 - LPNMPGHOTITEM
 - commctrl/LPNMPGHOTITEM
 - NMPGHOTITEM
 - commctrl/NMPGHOTITEM
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
 - NMPGHOTITEM
---

# NMPGHOTITEM structure


## -description

Contains information used with the <a href="/windows/desktop/Controls/pgn-hotitemchange">PGN_HOTITEMCHANGE</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field idOld

Type: <b>int</b>

Value of type <b>int</b> that specifies the command identifier of the previously highlighted item.

### -field idNew

Type: <b>int</b>

Value of type <b>int</b> that specifies the command identifier of the highlighted item.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<b>DWORD</b> that contains flags that indicate why the hot item has changed. This can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>HICF_ENTERING</dt>
</dl>
</td>
<td width="60%">
If this flag is set, there is no previous hot item and <b>idOld</b> does not contain valid information.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>HICF_LEAVING</dt>
</dl>
</td>
<td width="60%">
If this flag is set, there is no new hot item and <b>idNew</b> does not contain valid information.

</td>
</tr>
</table>