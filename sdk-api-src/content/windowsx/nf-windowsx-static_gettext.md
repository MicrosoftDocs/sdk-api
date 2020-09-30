---
UID: NF:windowsx.Static_GetText
title: Static_GetText macro (windowsx.h)
description: Gets the text of a static control.
helpviewer_keywords: ["Static_GetText","Static_GetText macro [Windows Controls]","_win32_Static_GetText","_win32_Static_GetText_cpp","controls.Static_GetText","controls._win32_Static_GetText","windowsx/Static_GetText"]
old-location: controls\Static_GetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\staticcontrols\staticcontrolreference\staticcontrolmacros\static_gettext.htm
ms.date: 12/05/2018
ms.keywords: Static_GetText, Static_GetText macro [Windows Controls], _win32_Static_GetText, _win32_Static_GetText_cpp, controls.Static_GetText, controls._win32_Static_GetText, windowsx/Static_GetText
req.header: windowsx.h
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
 - Static_GetText
 - windowsx/Static_GetText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - Static_GetText
---

# Static_GetText macro


## -description

Gets the text of a static control.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lpch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to the buffer that will receive the text.

### -param cchMax

Type: <b>int</b>

The maximum number of characters to copy to the buffer, including the NULL terminator.

## -remarks

The macro expands to a call to <a href="/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>.