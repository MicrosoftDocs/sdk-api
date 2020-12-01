---
UID: NS:commctrl.tagTVKEYDOWN
title: NMTVKEYDOWN (commctrl.h)
description: Contains information about a keyboard event in a tree-view control. This structure is used with the TVN_KEYDOWN notification code. The structure is identical to the TV_KEYDOWN structure, but it has been renamed to follow current naming conventions.
helpviewer_keywords: ["*LPNMTVKEYDOWN","LPNMTVKEYDOWN","LPNMTVKEYDOWN structure pointer [Windows Controls]","NMTVKEYDOWN","NMTVKEYDOWN structure [Windows Controls]","_win32_NMTVKEYDOWN","_win32_NMTVKEYDOWN_cpp","commctrl/LPNMTVKEYDOWN","commctrl/NMTVKEYDOWN","controls.NMTVKEYDOWN","controls._win32_NMTVKEYDOWN"]
old-location: controls\NMTVKEYDOWN.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\structures\nmtvkeydown.htm
ms.date: 12/05/2018
ms.keywords: '*LPNMTVKEYDOWN, LPNMTVKEYDOWN, LPNMTVKEYDOWN structure pointer [Windows Controls], NMTVKEYDOWN, NMTVKEYDOWN structure [Windows Controls], _win32_NMTVKEYDOWN, _win32_NMTVKEYDOWN_cpp, commctrl/LPNMTVKEYDOWN, commctrl/NMTVKEYDOWN, controls.NMTVKEYDOWN, controls._win32_NMTVKEYDOWN'
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
req.typenames: NMTVKEYDOWN, *LPNMTVKEYDOWN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTVKEYDOWN
 - commctrl/tagTVKEYDOWN
 - LPNMTVKEYDOWN
 - commctrl/LPNMTVKEYDOWN
 - NMTVKEYDOWN
 - commctrl/NMTVKEYDOWN
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
 - NMTVKEYDOWN
---

# NMTVKEYDOWN structure


## -description

Contains information about a keyboard event in a tree-view control. This structure is used with the <a href="/windows/desktop/Controls/tvn-keydown">TVN_KEYDOWN</a> notification code. The structure is identical to the 
			<b>TV_KEYDOWN</b> structure, but it has been renamed to follow current naming conventions.

## -struct-fields

### -field hdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a></b>


<a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains information about this notification.

### -field wVKey

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">WORD</a></b>

Virtual key code.

### -field flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Always zero.

## -see-also

<a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a>