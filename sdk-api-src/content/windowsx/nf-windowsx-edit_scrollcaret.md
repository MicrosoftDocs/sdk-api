---
UID: NF:windowsx.Edit_ScrollCaret
title: Edit_ScrollCaret macro (windowsx.h)
description: Scrolls the caret into view in an edit or rich edit control. You can use this macro or send the EM_SCROLLCARET message explicitly.
helpviewer_keywords: ["Edit_ScrollCaret","Edit_ScrollCaret macro [Windows Controls]","_win32_Edit_ScrollCaret","_win32_Edit_ScrollCaret_cpp","controls.Edit_ScrollCaret","controls._win32_Edit_ScrollCaret","windowsx/Edit_ScrollCaret"]
old-location: controls\Edit_ScrollCaret.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_scrollcaretl.htm
ms.date: 10/21/2024
ms.keywords: Edit_ScrollCaret, Edit_ScrollCaret macro [Windows Controls], _win32_Edit_ScrollCaret, _win32_Edit_ScrollCaret_cpp, controls.Edit_ScrollCaret, controls._win32_Edit_ScrollCaret, windowsx/Edit_ScrollCaret
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
 - Edit_ScrollCaret
 - windowsx/Edit_ScrollCaret
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
 - Edit_ScrollCaret
---

# Edit_ScrollCaret macro

## -syntax

```cpp
BOOL Edit_ScrollCaret(
   HWND hwndCtl
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

The return value is not meaningful.


## -description

Scrolls the caret into view in an edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-scrollcaret">EM_SCROLLCARET</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.
