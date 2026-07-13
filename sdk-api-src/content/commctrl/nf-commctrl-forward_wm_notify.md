---
UID: NF:commctrl.FORWARD_WM_NOTIFY
title: FORWARD_WM_NOTIFY macro (commctrl.h)
description: Sends or posts the WM_NOTIFY message.
helpviewer_keywords: ["FORWARD_WM_NOTIFY","FORWARD_WM_NOTIFY macro [Windows Controls]","_win32_FORWARD_WM_NOTIFY","_win32_FORWARD_WM_NOTIFY_cpp","commctrl/FORWARD_WM_NOTIFY","controls.FORWARD_WM_NOTIFY","controls._win32_FORWARD_WM_NOTIFY"]
old-location: controls\FORWARD_WM_NOTIFY.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\macros\forward_wm_notify.htm
ms.date: 10/21/2024
ms.keywords: FORWARD_WM_NOTIFY, FORWARD_WM_NOTIFY macro [Windows Controls], _win32_FORWARD_WM_NOTIFY, _win32_FORWARD_WM_NOTIFY_cpp, commctrl/FORWARD_WM_NOTIFY, controls.FORWARD_WM_NOTIFY, controls._win32_FORWARD_WM_NOTIFY
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FORWARD_WM_NOTIFY
 - commctrl/FORWARD_WM_NOTIFY
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
 - FORWARD_WM_NOTIFY
---

# FORWARD_WM_NOTIFY macro

## -syntax

```cpp
VOID FORWARD_WM_NOTIFY(
   HWND     hwnd,
   int      idFrom,
   NMHDR    *pnmhdr,
   function fn
);
```

## -returns

Type: **[VOID](/windows/desktop/winprog/windows-data-types)**

Returns a value whose meaning depends on the <i>fn</i> parameter.

## -description

Sends or posts the <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a> message.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that receives the <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a> message.

### -param idFrom

Type: <b>int</b>

The identifier of the control sending the message.

### -param pnmhdr

Type: <b><a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a>*</b>

A pointer to an <a href="/windows/desktop/api/richedit/ns-richedit-nmhdr">NMHDR</a> structure that contains the notification code and additional information. For some notification codes, this parameter points to a larger structure that has the <b>NMHDR</b> structure as its first member.

### -param fn

Type: <b>function</b>

The function that sends or posts the <a href="/windows/desktop/Controls/wm-notify">WM_NOTIFY</a> message. This parameter can be either the <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> or <a href="/windows/desktop/api/winuser/nf-winuser-postmessagea">PostMessage</a> function.

## -remarks

The <b>FORWARD_WM_NOTIFY</b> macro is defined as follows. 


``` syntax
#define FORWARD_WM_NOTIFY(hwnd, idFrom, pnmhdr, fn) \ 

    (void)(fn)((hwnd), WM_NOTIFY, (WPARAM)(int)(id), \ 
    (LPARAM)(NMHDR*)(pnmhdr)) 
```

