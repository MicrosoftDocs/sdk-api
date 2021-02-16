---
UID: NS:commctrl.tagNMLVEMPTYMARKUP
title: NMLVEMPTYMARKUP (commctrl.h)
description: Contains information used with the LVN_GETEMPTYMARKUP notification code.
helpviewer_keywords: ["EMF_CENTERED","NMLVEMPTYMARKUP","NMLVEMPTYMARKUP structure [Windows Controls]","commctrl/NMLVEMPTYMARKUP","controls.NMLVEMPTYMARKUP","controls.shell_NMLVEMPTYMARKUP","shell_NMLVEMPTYMARKUP","shell_NMLVEMPTYMARKUP_cpp"]
old-location: controls\NMLVEMPTYMARKUP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvemptymarkup.htm
ms.date: 12/05/2018
ms.keywords: EMF_CENTERED, NMLVEMPTYMARKUP, NMLVEMPTYMARKUP structure [Windows Controls], commctrl/NMLVEMPTYMARKUP, controls.NMLVEMPTYMARKUP, controls.shell_NMLVEMPTYMARKUP, shell_NMLVEMPTYMARKUP, shell_NMLVEMPTYMARKUP_cpp
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: NMLVEMPTYMARKUP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMLVEMPTYMARKUP
 - commctrl/tagNMLVEMPTYMARKUP
 - NMLVEMPTYMARKUP
 - commctrl/NMLVEMPTYMARKUP
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
 - NMLVEMPTYMARKUP
---

# NMLVEMPTYMARKUP structure


## -description

Contains information used with the <a href="/windows/desktop/Controls/lvn-getemptymarkup">LVN_GETEMPTYMARKUP</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

Info on the notification message.

### -field dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

One of the following values. If <b>NULL</b>, markup is rendered left-justified in the listview area.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EMF_CENTERED"></a><a id="emf_centered"></a><dl>
<dt><b>EMF_CENTERED</b></dt>
</dl>
</td>
<td width="60%">
Render markup centered in the listview area.

</td>
</tr>
</table>

### -field szMarkup

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WCHAR</a>[L_MAX_URL_LENGTH]</b>

Markup to display.