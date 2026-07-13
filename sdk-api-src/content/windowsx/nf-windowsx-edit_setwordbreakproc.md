---
UID: NF:windowsx.Edit_SetWordBreakProc
title: Edit_SetWordBreakProc macro (windowsx.h)
description: Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function. You can use this macro or send the EM_SETWORDBREAKPROC message explicitly.
helpviewer_keywords: ["Edit_SetWordBreakProc","Edit_SetWordBreakProc macro [Windows Controls]","_win32_Edit_SetWordBreakProc","_win32_Edit_SetWordBreakProc_cpp","controls.Edit_SetWordBreakProc","controls._win32_Edit_SetWordBreakProc","windowsx/Edit_SetWordBreakProc"]
old-location: controls\Edit_SetWordBreakProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setwordbreakproc.htm
ms.date: 10/21/2024
ms.keywords: Edit_SetWordBreakProc, Edit_SetWordBreakProc macro [Windows Controls], _win32_Edit_SetWordBreakProc, _win32_Edit_SetWordBreakProc_cpp, controls.Edit_SetWordBreakProc, controls._win32_Edit_SetWordBreakProc, windowsx/Edit_SetWordBreakProc
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
 - Edit_SetWordBreakProc
 - windowsx/Edit_SetWordBreakProc
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
 - Edit_SetWordBreakProc
---

# Edit_SetWordBreakProc macro

## -syntax

```cpp
void Edit_SetWordBreakProc(
   HWND              hwndCtl,
   EDITWORDBREAKPROC lpfnWordBreak
);
```


## -description

Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function. You can use this macro or send the <a href="/windows/desktop/Controls/em-setwordbreakproc">EM_SETWORDBREAKPROC</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lpfnWordBreak

Type: <b>EDITWORDBREAKPROC</b>

The address of the application-defined Wordwrap function. For more information about breaking lines, see the description of the <a href="/windows/desktop/api/winuser/nc-winuser-editwordbreakproca">EditWordBreakProc</a> callback function.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-setwordbreakproc">EM_SETWORDBREAKPROC</a>.
