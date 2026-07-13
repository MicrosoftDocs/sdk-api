---
UID: NF:windowsx.Edit_GetWordBreakProc
title: Edit_GetWordBreakProc macro (windowsx.h)
description: Retrieves the address of an edit or rich edit control's Wordwrap function. You can use this macro or send the EM_GETWORDBREAKPROC message explicitly.
helpviewer_keywords: ["Edit_GetWordBreakProc","Edit_GetWordBreakProc macro [Windows Controls]","_win32_Edit_GetWordBreakProc","_win32_Edit_GetWordBreakProc_cpp","controls.Edit_GetWordBreakProc","controls._win32_Edit_GetWordBreakProc","windowsx/Edit_GetWordBreakProc"]
old-location: controls\Edit_GetWordBreakProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getwordbreakproc.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetWordBreakProc, Edit_GetWordBreakProc macro [Windows Controls], _win32_Edit_GetWordBreakProc, _win32_Edit_GetWordBreakProc_cpp, controls.Edit_GetWordBreakProc, controls._win32_Edit_GetWordBreakProc, windowsx/Edit_GetWordBreakProc
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
 - Edit_GetWordBreakProc
 - windowsx/Edit_GetWordBreakProc
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
 - Edit_GetWordBreakProc
---

# Edit_GetWordBreakProc macro

## -syntax

```cpp
EDITWORDBREAKPROC Edit_GetWordBreakProc(
   HWND hwndCtl
);
```

## -returns

Type: **EDITWORDBREAKPROC**

The address of the application-defined Wordwrap function, or <b>NULL</b> if no function has been set.


## -description

Retrieves the address of an edit or rich edit control's Wordwrap function. You can use this macro or send the <a href="/windows/desktop/Controls/em-getwordbreakproc">EM_GETWORDBREAKPROC</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-getwordbreakproc">EM_GETWORDBREAKPROC</a>.
