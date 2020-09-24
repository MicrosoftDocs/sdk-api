---
UID: NS:commctrl.tagTRBTHUMBPOSCHANGING
title: NMTRBTHUMBPOSCHANGING (commctrl.h)
description: Contains information about a trackbar change notification. This message is sent with the TRBN_THUMBPOSCHANGING notification.
helpviewer_keywords: ["NMTRBTHUMBPOSCHANGING","NMTRBTHUMBPOSCHANGING structure [Windows Controls]","_shell_NMTRBTHUMBPOSCHANGING","_shell_NMTRBTHUMBPOSCHANGING_cpp","commctrl/NMTRBTHUMBPOSCHANGING","controls.NMTRBTHUMBPOSCHANGING","controls._shell_NMTRBTHUMBPOSCHANGING"]
old-location: controls\NMTRBTHUMBPOSCHANGING.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\trackbar\structures\nmtrbthumbposchanging.htm
ms.date: 12/05/2018
ms.keywords: NMTRBTHUMBPOSCHANGING, NMTRBTHUMBPOSCHANGING structure [Windows Controls], _shell_NMTRBTHUMBPOSCHANGING, _shell_NMTRBTHUMBPOSCHANGING_cpp, commctrl/NMTRBTHUMBPOSCHANGING, controls.NMTRBTHUMBPOSCHANGING, controls._shell_NMTRBTHUMBPOSCHANGING
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
req.typenames: NMTRBTHUMBPOSCHANGING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTRBTHUMBPOSCHANGING
 - commctrl/tagTRBTHUMBPOSCHANGING
 - NMTRBTHUMBPOSCHANGING
 - commctrl/NMTRBTHUMBPOSCHANGING
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
 - NMTRBTHUMBPOSCHANGING
---

# NMTRBTHUMBPOSCHANGING structure


## -description

Contains information about a trackbar change notification. This message is sent with the <a href="/windows/desktop/Controls/trbn-thumbposchanging">TRBN_THUMBPOSCHANGING</a> notification.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

A <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that describes the notification.

### -field dwPos

Type: <b>DWORD</b>

Position on trackbar.

### -field nReason

Type: <b>int</b>

Type of movement as one of the following values: TB_LINEUP, TB_LINEDOWN, TB_PAGEUP, TB_PAGEDOWN, TB_THUMBPOSITION, TB_THUMBTRACK,
                TB_TOP, TB_BOTTOM, or TB_ENDTRACK.