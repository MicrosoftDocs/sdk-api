---
UID: NF:windowsx.Edit_CanUndo
title: Edit_CanUndo macro (windowsx.h)
description: Determines whether there are any actions in the undo queue of an edit or rich edit control. You can use this macro or send the EM_CANUNDO message explicitly.
helpviewer_keywords: ["Edit_CanUndo","Edit_CanUndo macro [Windows Controls]","_win32_Edit_CanUndo","_win32_Edit_CanUndo_cpp","controls.Edit_CanUndo","controls._win32_Edit_CanUndo","windowsx/Edit_CanUndo"]
old-location: controls\Edit_CanUndo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_canundo.htm
ms.date: 10/21/2024
ms.keywords: Edit_CanUndo, Edit_CanUndo macro [Windows Controls], _win32_Edit_CanUndo, _win32_Edit_CanUndo_cpp, controls.Edit_CanUndo, controls._win32_Edit_CanUndo, windowsx/Edit_CanUndo
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
 - Edit_CanUndo
 - windowsx/Edit_CanUndo
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
 - Edit_CanUndo
---

# Edit_CanUndo macro

## -syntax

```cpp
BOOL Edit_CanUndo(
   HWND hwndCtl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if there are actions in the undo queue; otherwise <b>FALSE</b>.


## -description

Determines whether there are any actions in the undo queue of an edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-canundo">EM_CANUNDO</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-canundo">EM_CANUNDO</a>.
