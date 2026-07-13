---
UID: NS:commctrl.tagTVDISPINFOEXW
title: NMTVDISPINFOEXW (commctrl.h)
description: Contains information pertaining to extended TreeView notification information. (Unicode)
helpviewer_keywords: ["*LPNMTVDISPINFOEXW","LPNMTVDISPINFOEX","LPNMTVDISPINFOEX structure pointer [Windows Controls]","NMTVDISPINFOEX","NMTVDISPINFOEX structure [Windows Controls]","NMTVDISPINFOEXA","NMTVDISPINFOEXW","_shell_NMTVDISPINFOEX","_shell_NMTVDISPINFOEX_cpp","commctrl/LPNMTVDISPINFOEX","commctrl/NMTVDISPINFOEX","commctrl/NMTVDISPINFOEXA","commctrl/NMTVDISPINFOEXW","controls.NMTVDISPINFOEX","controls._shell_NMTVDISPINFOEX"]
old-location: controls\NMTVDISPINFOEX.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvdispinfoex.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTVDISPINFOEXW, LPNMTVDISPINFOEX, LPNMTVDISPINFOEX structure pointer [Windows Controls], NMTVDISPINFOEX, NMTVDISPINFOEX structure [Windows Controls], NMTVDISPINFOEXA, NMTVDISPINFOEXW, _shell_NMTVDISPINFOEX, _shell_NMTVDISPINFOEX_cpp, commctrl/LPNMTVDISPINFOEX, commctrl/NMTVDISPINFOEX, commctrl/NMTVDISPINFOEXA, commctrl/NMTVDISPINFOEXW, controls.NMTVDISPINFOEX, controls._shell_NMTVDISPINFOEX'
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
targetos: Windows
req.typenames: NMTVDISPINFOEXW, *LPNMTVDISPINFOEXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTVDISPINFOEXW
 - commctrl/tagTVDISPINFOEXW
 - LPNMTVDISPINFOEXW
 - commctrl/LPNMTVDISPINFOEXW
 - NMTVDISPINFOEXW
 - commctrl/NMTVDISPINFOEXW
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
 - NMTVDISPINFOEX
 - NMTVDISPINFOEXA
 - NMTVDISPINFOEXW
---

# NMTVDISPINFOEXW structure


## -description

Contains information pertaining to extended TreeView notification information.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification.

### -field item

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-tvitemexa">TVITEMEX</a></b>

Specifies or receives attributes of a TreeView item.

## -remarks

> [!NOTE]
> The commctrl.h header defines NMTVDISPINFOEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
