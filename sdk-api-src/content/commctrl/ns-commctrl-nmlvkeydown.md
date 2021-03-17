---
UID: NS:commctrl.tagLVKEYDOWN
title: NMLVKEYDOWN (commctrl.h)
description: Contains information used in processing the LVN_KEYDOWN notification code. This structure is the same as the NMLVKEYDOWN structure but has been renamed to fit standard naming conventions.
helpviewer_keywords: ["*LPNMLVKEYDOWN","LPNMLVKEYDOWN","LPNMLVKEYDOWN structure pointer [Windows Controls]","NMLVKEYDOWN","NMLVKEYDOWN structure [Windows Controls]","_win32_NMLVKEYDOWN","_win32_NMLVKEYDOWN_cpp","commctrl/LPNMLVKEYDOWN","commctrl/NMLVKEYDOWN","controls.NMLVKEYDOWN","controls._win32_NMLVKEYDOWN"]
old-location: controls\NMLVKEYDOWN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\structures\nmlvkeydown.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMLVKEYDOWN, LPNMLVKEYDOWN, LPNMLVKEYDOWN structure pointer [Windows Controls], NMLVKEYDOWN, NMLVKEYDOWN structure [Windows Controls], _win32_NMLVKEYDOWN, _win32_NMLVKEYDOWN_cpp, commctrl/LPNMLVKEYDOWN, commctrl/NMLVKEYDOWN, controls.NMLVKEYDOWN, controls._win32_NMLVKEYDOWN'
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
req.typenames: NMLVKEYDOWN, *LPNMLVKEYDOWN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagLVKEYDOWN
 - commctrl/tagLVKEYDOWN
 - LPNMLVKEYDOWN
 - commctrl/LPNMLVKEYDOWN
 - NMLVKEYDOWN
 - commctrl/NMLVKEYDOWN
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
 - NMLVKEYDOWN
---

# NMLVKEYDOWN structure


## -description

Contains information used in processing the <a href="/windows/desktop/Controls/lvn-keydown">LVN_KEYDOWN</a> notification code. This structure is the same as the 
			<b>NMLVKEYDOWN</b> structure but has been renamed to fit standard naming conventions.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains additional information about the notification.

### -field wVKey

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>


<a href="/windows/desktop/inputdev/virtual-key-codes">Virtual key code</a>.

### -field flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

This member must always be zero.