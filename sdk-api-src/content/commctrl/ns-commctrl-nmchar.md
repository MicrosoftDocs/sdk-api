---
UID: NS:commctrl.tagNMCHAR
title: NMCHAR (commctrl.h)
description: Contains information used with character notification messages.
helpviewer_keywords: ["*LPNMCHAR","LPNMCHAR","LPNMCHAR structure pointer [Windows Controls]","NMCHAR","NMCHAR structure [Windows Controls]","_win32_NMCHAR","_win32_NMCHAR_cpp","commctrl/LPNMCHAR","commctrl/NMCHAR","controls.NMCHAR","controls._win32_NMCHAR"]
old-location: controls\NMCHAR.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmchar.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMCHAR, LPNMCHAR, LPNMCHAR structure pointer [Windows Controls], NMCHAR, NMCHAR structure [Windows Controls], _win32_NMCHAR, _win32_NMCHAR_cpp, commctrl/LPNMCHAR, commctrl/NMCHAR, controls.NMCHAR, controls._win32_NMCHAR'
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
req.typenames: NMCHAR, *LPNMCHAR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMCHAR
 - commctrl/tagNMCHAR
 - LPNMCHAR
 - commctrl/LPNMCHAR
 - NMCHAR
 - commctrl/NMCHAR
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
 - NMCHAR
---

# NMCHAR structure


## -description

Contains information used with character notification messages.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>

An <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about this notification.

### -field ch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The character that is being processed.

### -field dwItemPrev

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A 32-bit value that is determined by the control that is sending the notification.

### -field dwItemNext

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A 32-bit value that is determined by the control that is sending the notification.