---
UID: NS:commctrl.tagNMKEY
title: NMKEY (commctrl.h)
description: Contains information used with key notification messages.
old-location: controls\NMKEY.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmkey.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMKEY, LPNMKEY, LPNMKEY structure pointer [Windows Controls], NMKEY, NMKEY structure [Windows Controls], _win32_NMKEY, _win32_NMKEY_cpp, commctrl/LPNMKEY, commctrl/NMKEY, controls.NMKEY, controls._win32_NMKEY'
f1_keywords:
- commctrl/NMKEY
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- NMKEY
targetos: Windows
req.typenames: NMKEY, *LPNMKEY
req.redist: 
ms.custom: 19H1
---

# NMKEY structure


## -description


Contains information used with key notification messages. 


## -struct-fields




### -field hdr

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="https://docs.microsoft.com/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about this notification. 


### -field nVKey

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A virtual key code of the key that caused the event. 


### -field uFlags

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags associated with the key. These are the same flags that are passed in the high word of the 
					<i>lParam</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> message.

