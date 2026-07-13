---
UID: NF:windowsx.Button_GetText
title: Button_GetText macro (windowsx.h)
description: Gets the text of a button.
helpviewer_keywords: ["Button_GetText","Button_GetText macro [Windows Controls]","_win32_Button_GetText","_win32_Button_GetText_cpp","controls.Button_GetText","controls._win32_Button_GetText","windowsx/Button_GetText"]
old-location: controls\Button_GetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\buttons\buttonreference\buttonmacros\button_gettext.htm
ms.date: 10/21/2024
ms.keywords: Button_GetText, Button_GetText macro [Windows Controls], _win32_Button_GetText, _win32_Button_GetText_cpp, controls.Button_GetText, controls._win32_Button_GetText, windowsx/Button_GetText
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
 - Button_GetText
 - windowsx/Button_GetText
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
 - Button_GetText
---

# Button_GetText macro

## -syntax

```cpp
int Button_GetText(
   HWND   hwndCtl,
   LPTSTR lpch,
   int    cchMax
);
```

## -returns

Type: **int**

The length, in characters, of the copied string, not including the terminating NULL character.


## -description

Gets the text of a button.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the button control.

### -param lpch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

Pointer to the buffer that will receive the text.

### -param cchMax

Type: <b>int</b>

The maximum number of characters to copy to the buffer, including the NULL terminator.

## -remarks

The macro expands to a call to <a href="/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>.
