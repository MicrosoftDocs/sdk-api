---
UID: NS:commctrl.tagNMKEY
title: NMKEY (commctrl.h)
description: Contains information used with key notification messages.
helpviewer_keywords: ["*LPNMKEY","LPNMKEY","LPNMKEY structure pointer [Windows Controls]","NMKEY","NMKEY structure [Windows Controls]","_win32_NMKEY","_win32_NMKEY_cpp","commctrl/LPNMKEY","commctrl/NMKEY","controls.NMKEY","controls._win32_NMKEY"]
old-location: controls\NMKEY.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmkey.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMKEY, LPNMKEY, LPNMKEY structure pointer [Windows Controls], NMKEY, NMKEY structure [Windows Controls], _win32_NMKEY, _win32_NMKEY_cpp, commctrl/LPNMKEY, commctrl/NMKEY, controls.NMKEY, controls._win32_NMKEY'
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
req.typenames: NMKEY, *LPNMKEY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMKEY
 - commctrl/tagNMKEY
 - LPNMKEY
 - commctrl/LPNMKEY
 - NMKEY
 - commctrl/NMKEY
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
 - NMKEY
---

# NMKEY structure


## -description

Contains information used with key notification messages.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about this notification.

### -field nVKey

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A virtual key code of the key that caused the event.

### -field uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags associated with the key. These are the same flags that are passed in the high word of the 
					<i>lParam</i> parameter of the <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> message.