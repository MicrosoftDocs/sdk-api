---
UID: NS:winuser.tagCWPSTRUCT
title: CWPSTRUCT (winuser.h)
description: Defines the message parameters passed to a WH_CALLWNDPROC hook procedure, CallWndProc.
helpviewer_keywords: ["*LPCWPSTRUCT","*NPCWPSTRUCT","*PCWPSTRUCT","CWPSTRUCT","CWPSTRUCT structure [Windows and Messages]","LPCWPSTRUCT","LPCWPSTRUCT structure pointer [Windows and Messages]","PCWPSTRUCT","PCWPSTRUCT structure pointer [Windows and Messages]","_win32_CWPSTRUCT_str","_win32_cwpstruct_str_cpp","winmsg.cwpstruct","winui._win32_cwpstruct_str","winuser/CWPSTRUCT","winuser/LPCWPSTRUCT","winuser/PCWPSTRUCT"]
old-location: winmsg\cwpstruct.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\hooks\hookreference\hookstructures\cwpstruct.htm
ms.date: 12/05/2018
ms.keywords: '*LPCWPSTRUCT, *NPCWPSTRUCT, *PCWPSTRUCT, CWPSTRUCT, CWPSTRUCT structure [Windows and Messages], LPCWPSTRUCT, LPCWPSTRUCT structure pointer [Windows and Messages], PCWPSTRUCT, PCWPSTRUCT structure pointer [Windows and Messages], _win32_CWPSTRUCT_str, _win32_cwpstruct_str_cpp, winmsg.cwpstruct, winui._win32_cwpstruct_str, winuser/CWPSTRUCT, winuser/LPCWPSTRUCT, winuser/PCWPSTRUCT'
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: CWPSTRUCT, *PCWPSTRUCT, *NPCWPSTRUCT, *LPCWPSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagCWPSTRUCT
 - winuser/tagCWPSTRUCT
 - PCWPSTRUCT
 - winuser/PCWPSTRUCT
 - CWPSTRUCT
 - winuser/CWPSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winuser.h
api_name:
 - CWPSTRUCT
---

# CWPSTRUCT structure


## -description

Defines the message parameters passed to a <b>WH_CALLWNDPROC</b> hook procedure, <a href="/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)">CallWndProc</a>.

## -struct-fields

### -field lParam

Type: <b>LPARAM</b>

Additional information about the message. The exact meaning depends on the 
					<b>message</b> value.

### -field wParam

Type: <b>WPARAM</b>

Additional information about the message. The exact meaning depends on the 
					<b>message</b> value.

### -field message

Type: <b>UINT</b>

The message.

### -field hwnd

Type: <b>HWND</b>

A handle to the window to receive the message.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)">CallWndProc</a>



<b>Conceptual</b>



<a href="/windows/desktop/winmsg/hooks">Hooks</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-setwindowshookexa">SetWindowsHookEx</a>