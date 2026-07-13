---
UID: NF:windowsx.Edit_SetPasswordChar
title: Edit_SetPasswordChar macro (windowsx.h)
description: Sets or removes the password character for an edit or rich edit control. When a password character is set, that character is displayed in place of the characters typed by the user. You can use this macro or send the EM_SETPASSWORDCHAR message explicitly.
helpviewer_keywords: ["Edit_SetPasswordChar","Edit_SetPasswordChar macro [Windows Controls]","_win32_Edit_SetPasswordChar","_win32_Edit_SetPasswordChar_cpp","controls.Edit_SetPasswordChar","controls._win32_Edit_SetPasswordChar","windowsx/Edit_SetPasswordChar"]
old-location: controls\Edit_SetPasswordChar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setpasswordchar.htm
ms.date: 10/21/2024
ms.keywords: Edit_SetPasswordChar, Edit_SetPasswordChar macro [Windows Controls], _win32_Edit_SetPasswordChar, _win32_Edit_SetPasswordChar_cpp, controls.Edit_SetPasswordChar, controls._win32_Edit_SetPasswordChar, windowsx/Edit_SetPasswordChar
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
 - Edit_SetPasswordChar
 - windowsx/Edit_SetPasswordChar
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
 - Edit_SetPasswordChar
---

# Edit_SetPasswordChar macro

## -syntax

```cpp
void Edit_SetPasswordChar(
   HWND hwndCtl,
   UINT ch
);
```


## -description

Sets or removes the password character for an edit or rich edit control. When a password character is set, that character is displayed in place of the characters typed by the user. You can use this macro or send the <a href="/windows/desktop/Controls/em-setpasswordchar">EM_SETPASSWORDCHAR</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param ch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The character to be displayed in place of the characters typed by the user. If this parameter is zero, the control removes the current password character and displays the characters typed by the user.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-setpasswordchar">EM_SETPASSWORDCHAR</a>.
