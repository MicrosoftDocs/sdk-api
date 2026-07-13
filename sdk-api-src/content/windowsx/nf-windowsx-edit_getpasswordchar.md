---
UID: NF:windowsx.Edit_GetPasswordChar
title: Edit_GetPasswordChar macro (windowsx.h)
description: Gets the password character for an edit or rich edit control. You can use this macro or send the EM_GETPASSWORDCHAR message explicitly.
helpviewer_keywords: ["Edit_GetPasswordChar","Edit_GetPasswordChar macro [Windows Controls]","_win32_Edit_GetPasswordChar","_win32_Edit_GetPasswordChar_cpp","controls.Edit_GetPasswordChar","controls._win32_Edit_GetPasswordChar","windowsx/Edit_GetPasswordChar"]
old-location: controls\Edit_GetPasswordChar.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getpasswordchar.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetPasswordChar, Edit_GetPasswordChar macro [Windows Controls], _win32_Edit_GetPasswordChar, _win32_Edit_GetPasswordChar_cpp, controls.Edit_GetPasswordChar, controls._win32_Edit_GetPasswordChar, windowsx/Edit_GetPasswordChar
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
 - Edit_GetPasswordChar
 - windowsx/Edit_GetPasswordChar
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
 - Edit_GetPasswordChar
---

# Edit_GetPasswordChar macro

## -syntax

```cpp
TCHAR Edit_GetPasswordChar(
   HWND hwndCtl
);
```

## -returns

Type: **[TCHAR](/windows/desktop/winprog/windows-data-types)**

The password character.


## -description

Gets the password character for an edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-getpasswordchar">EM_GETPASSWORDCHAR</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-getpasswordchar">EM_GETPASSWORDCHAR</a>.
