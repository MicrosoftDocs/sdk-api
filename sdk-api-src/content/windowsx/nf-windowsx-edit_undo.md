---
UID: NF:windowsx.Edit_Undo
title: Edit_Undo macro (windowsx.h)
description: Undoes the last operation in the undo queue of an edit or rich edit control. You can use this macro or send the EM_UNDO message explicitly.
helpviewer_keywords: ["Edit_Undo","Edit_Undo macro [Windows Controls]","_win32_Edit_Undo","_win32_Edit_Undo_cpp","controls.Edit_Undo","controls._win32_Edit_Undo","windowsx/Edit_Undo"]
old-location: controls\Edit_Undo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_undo.htm
ms.date: 10/21/2024
ms.keywords: Edit_Undo, Edit_Undo macro [Windows Controls], _win32_Edit_Undo, _win32_Edit_Undo_cpp, controls.Edit_Undo, controls._win32_Edit_Undo, windowsx/Edit_Undo
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
 - Edit_Undo
 - windowsx/Edit_Undo
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
 - Edit_Undo
---

# Edit_Undo macro

## -syntax

```cpp
BOOL Edit_Undo(
   HWND hwndCtl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

For a single-line control, the return value is always <b>TRUE</b>. For a multiline control, the return value is <b>TRUE</b> if the undo operation is successful, or <b>FALSE</b> otherwise.


## -description

Undoes the last operation in the undo queue of an edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-undo">EM_UNDO</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-undo">EM_UNDO</a>.
