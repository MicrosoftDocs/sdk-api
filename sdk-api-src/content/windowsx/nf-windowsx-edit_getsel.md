---
UID: NF:windowsx.Edit_GetSel
title: Edit_GetSel macro (windowsx.h)
description: Gets the starting and ending character positions of the current selection in an edit or rich edit control. You can use this macro or send the EM_GETSEL message explicitly.
helpviewer_keywords: ["Edit_GetSel","Edit_GetSel macro [Windows Controls]","_win32_Edit_GetSel","_win32_Edit_GetSel_cpp","controls.Edit_GetSel","controls._win32_Edit_GetSel","windowsx/Edit_GetSel"]
old-location: controls\Edit_GetSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getsel.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetSel, Edit_GetSel macro [Windows Controls], _win32_Edit_GetSel, _win32_Edit_GetSel_cpp, controls.Edit_GetSel, controls._win32_Edit_GetSel, windowsx/Edit_GetSel
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
 - Edit_GetSel
 - windowsx/Edit_GetSel
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
 - Edit_GetSel
---

# Edit_GetSel macro

## -syntax

```cpp
DWORD Edit_GetSel(
   HWND hwndCtl
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

The return value is a zero-based value with the starting position of the selection in the <b>LOWORD</b> and the position of the first character after the last selected character in the <b>HIWORD</b>. If either of these values exceeds 65,535, the return value is &#8211;1.


## -description

Gets the starting and ending character positions of the current selection in an edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-getsel">EM_GETSEL</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

This macro does not have the complete functionality of the <a href="/windows/desktop/Controls/em-getsel">EM_GETSEL</a> message, because it does not receive the 32-bit return values in the parameters of <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>.
