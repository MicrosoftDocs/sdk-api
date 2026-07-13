---
UID: NS:winuser.tagNMHDR
title: NMHDR (winuser.h)
description: The NMHDR structure contains information about a notification message. (NMHDR structure)
helpviewer_keywords: ["*LPNMHDR","NMHDR","NMHDR structure [Windows Controls]","_win32_NMHDR_str","_win32_NMHDR_str_cpp","controls.NMHDR","controls._win32_NMHDR_str","richedit/NMHDR"]
old-location: controls\NMHDR.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\structures\nmhdr.htm
ms.date: 08/02/2022
ms.keywords: '*LPNMHDR, NMHDR, NMHDR structure [Windows Controls], _win32_NMHDR_str, _win32_NMHDR_str_cpp, controls.NMHDR, controls._win32_NMHDR_str, richedit/NMHDR'
req.header: winuser.h
req.include-header: Winuser.h
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
req.typenames: NMHDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNMHDR
 - winuser/tagNMHDR
 - NMHDR
 - winuser/NMHDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - richedit.h
api_name:
 - NMHDR
---

# NMHDR structure


## -description

Contains information about a notification message.

## -struct-fields

### -field hwndFrom

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A window handle to the control sending the message.

### -field idFrom

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT_PTR</a></b>

An identifier of the control sending the message.

### -field code

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A notification code. This member can be one of the common notification codes (see Notifications under <a href="/windows/desktop/Controls/common-control-reference">General Control Reference</a>), or it can be a control-specific notification code.
