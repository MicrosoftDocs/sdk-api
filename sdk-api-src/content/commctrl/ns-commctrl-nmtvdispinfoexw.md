---
UID: NS:commctrl.tagTVDISPINFOEXW
title: NMTVDISPINFOEXW (commctrl.h)
description: Contains information pertaining to extended TreeView notification information.
old-location: controls\NMTVDISPINFOEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvdispinfoex.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTVDISPINFOEXW, LPNMTVDISPINFOEX, LPNMTVDISPINFOEX structure pointer [Windows Controls], NMTVDISPINFOEX, NMTVDISPINFOEX structure [Windows Controls], NMTVDISPINFOEXA, NMTVDISPINFOEXW, _shell_NMTVDISPINFOEX, _shell_NMTVDISPINFOEX_cpp, commctrl/LPNMTVDISPINFOEX, commctrl/NMTVDISPINFOEX, commctrl/NMTVDISPINFOEXA, commctrl/NMTVDISPINFOEXW, controls.NMTVDISPINFOEX, controls._shell_NMTVDISPINFOEX'
f1_keywords:
- commctrl/NMTVDISPINFOEX
dev_langs:
- c++
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: NMTVDISPINFOEXW (Unicode) and NMTVDISPINFOEXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- NMTVDISPINFOEX
- NMTVDISPINFOEXA
- NMTVDISPINFOEXW
targetos: Windows
req.typenames: NMTVDISPINFOEXW, *LPNMTVDISPINFOEXW
req.redist: 
ms.custom: 19H1
---

# NMTVDISPINFOEXW structure


## -description


Contains information pertaining to extended TreeView notification information.


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification.


### -field item

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-tvitemexa">TVITEMEX</a></b>

Specifies or receives attributes of a TreeView item.

