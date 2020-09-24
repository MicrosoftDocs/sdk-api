---
UID: NS:commctrl.tagTCKEYDOWN
title: NMTCKEYDOWN (commctrl.h)
description: Contains information about a key press in a tab control. It is used with the TCN_KEYDOWN notification code. This structure supersedes the TC_KEYDOWN structure.
helpviewer_keywords: ["NMTCKEYDOWN","NMTCKEYDOWN structure [Windows Controls]","_win32_NMTCKEYDOWN","_win32_NMTCKEYDOWN_cpp","commctrl/NMTCKEYDOWN","controls.NMTCKEYDOWN","controls._win32_NMTCKEYDOWN"]
old-location: controls\NMTCKEYDOWN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\tab\structures\nmtckeydown.htm
ms.date: 12/05/2018
ms.keywords: NMTCKEYDOWN, NMTCKEYDOWN structure [Windows Controls], _win32_NMTCKEYDOWN, _win32_NMTCKEYDOWN_cpp, commctrl/NMTCKEYDOWN, controls.NMTCKEYDOWN, controls._win32_NMTCKEYDOWN
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
req.typenames: NMTCKEYDOWN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTCKEYDOWN
 - commctrl/tagTCKEYDOWN
 - NMTCKEYDOWN
 - commctrl/NMTCKEYDOWN
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
 - NMTCKEYDOWN
---

# NMTCKEYDOWN structure


## -description

Contains information about a key press in a tab control. It is used with the <a href="/windows/desktop/Controls/tcn-keydown">TCN_KEYDOWN</a> notification code. This structure supersedes the
<b>TC_KEYDOWN</b> structure.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about the notification.

### -field wVKey

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Virtual key code.

### -field flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Value that is identical to the 
					<i>lParam</i> parameter of the <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> message.