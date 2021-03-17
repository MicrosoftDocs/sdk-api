---
UID: NS:commctrl.tagNMLVLINK
title: NMLVLINK (commctrl.h)
description: Contains information about an LVN_LINKCLICK notification code.
helpviewer_keywords: ["*PNMLVLINK","LPNMLVLINK","LPNMLVLINK structure pointer [Windows Controls]","NMLVLINK","NMLVLINK structure [Windows Controls]","commctrl/LPNMLVLINK","commctrl/NMLVLINK","controls.NMLVLINK","controls.shell_NMLVLINK","shell_NMLVLINK","shell_NMLVLINK_cpp"]
old-location: controls\NMLVLINK.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvlink.htm
ms.date: 12/05/2018
ms.keywords: '*PNMLVLINK, LPNMLVLINK, LPNMLVLINK structure pointer [Windows Controls], NMLVLINK, NMLVLINK structure [Windows Controls], commctrl/LPNMLVLINK, commctrl/NMLVLINK, controls.NMLVLINK, controls.shell_NMLVLINK, shell_NMLVLINK, shell_NMLVLINK_cpp'
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
req.typenames: NMLVLINK, *PNMLVLINK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMLVLINK
 - commctrl/tagNMLVLINK
 - PNMLVLINK
 - commctrl/PNMLVLINK
 - NMLVLINK
 - commctrl/NMLVLINK
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
 - NMLVLINK
---

# NMLVLINK structure


## -description

Contains information about an <a href="/windows/desktop/Controls/lvn-linkclick">LVN_LINKCLICK</a> notification code.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains basic information about the notification code.

### -field link

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-litem">LITEM</a></b>


<a href="/windows/desktop/api/commctrl/ns-commctrl-litem">LITEM</a> structure that contains information about the link that was clicked.

### -field iItem

Type: <b>int</b>

Index of the item that contains the link.

### -field iSubItem

Type: <b>int</b>

Subitem, if any. This member may be <b>NULL</b>. For a link in a group header, this is the group identifier, as set in <a href="/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a>.