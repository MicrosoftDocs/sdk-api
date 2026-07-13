---
UID: NS:commctrl.tagNMMOUSE
title: NMMOUSE (commctrl.h)
description: Contains information used with mouse notification messages.
helpviewer_keywords: ["*LPNMMOUSE","LPNMMOUSE","LPNMMOUSE structure pointer [Windows Controls]","NMCLICK","NMMOUSE","NMMOUSE structure [Windows Controls]","_win32_NMMOUSE","_win32_NMMOUSE_cpp","commctrl/LPNMMOUSE","commctrl/NMMOUSE","controls.NMMOUSE","controls._win32_NMMOUSE"]
old-location: controls\NMMOUSE.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmmouse.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMMOUSE, LPNMMOUSE, LPNMMOUSE structure pointer [Windows Controls], NMCLICK, NMMOUSE, NMMOUSE structure [Windows Controls], _win32_NMMOUSE, _win32_NMMOUSE_cpp, commctrl/LPNMMOUSE, commctrl/NMMOUSE, controls.NMMOUSE, controls._win32_NMMOUSE'
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
req.typenames: NMMOUSE, *LPNMMOUSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMMOUSE
 - commctrl/tagNMMOUSE
 - LPNMMOUSE
 - commctrl/LPNMMOUSE
 - NMMOUSE
 - commctrl/NMMOUSE
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
 - NMMOUSE
---

# NMMOUSE structure


## -description

Contains information used with mouse notification messages.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about this notification.

### -field dwItemSpec

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

A control-specific item identifier.

### -field dwItemData

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD_PTR</a></b>

A control-specific item data.

### -field pt

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

A <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that contains the client coordinates of the mouse when the click occurred.

### -field dwHitInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Carries information about where on the item or control the cursor is pointing.