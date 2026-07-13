---
UID: NF:windowsx.Edit_GetModify
title: Edit_GetModify macro (windowsx.h)
description: Gets the state of an edit or rich edit control's modification flag. The flag indicates whether the contents of the control have been modified. You can use this macro or send the EM_GETMODIFY message explicitly.
helpviewer_keywords: ["Edit_GetModify","Edit_GetModify macro [Windows Controls]","_win32_Edit_GetModify","_win32_Edit_GetModify_cpp","controls.Edit_GetModify","controls._win32_Edit_GetModify","windowsx/Edit_GetModify"]
old-location: controls\Edit_GetModify.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getmodify.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetModify, Edit_GetModify macro [Windows Controls], _win32_Edit_GetModify, _win32_Edit_GetModify_cpp, controls.Edit_GetModify, controls._win32_Edit_GetModify, windowsx/Edit_GetModify
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
 - Edit_GetModify
 - windowsx/Edit_GetModify
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
 - Edit_GetModify
---

# Edit_GetModify macro

## -syntax

```cpp
BOOL Edit_GetModify(
   HWND hwndCtl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the contents of edit control have been modified, the return value is nonzero; otherwise, it is zero.


## -description

Gets the state of an edit or rich edit control's modification flag. The flag indicates whether the contents of the control have been modified. You can use this macro or send the <a href="/windows/desktop/Controls/em-getmodify">EM_GETMODIFY</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-getmodify">EM_GETMODIFY</a>.
