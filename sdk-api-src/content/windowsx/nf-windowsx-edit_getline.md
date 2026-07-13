---
UID: NF:windowsx.Edit_GetLine
title: Edit_GetLine macro (windowsx.h)
description: Retrieves a line of text from an edit or rich edit control. You can use this macro or send the EM_GETLINE message explicitly.
helpviewer_keywords: ["Edit_GetLine","Edit_GetLine macro [Windows Controls]","_win32_Edit_GetLine","_win32_Edit_GetLine_cpp","controls.Edit_GetLine","controls._win32_Edit_GetLine","windowsx/Edit_GetLine"]
old-location: controls\Edit_GetLine.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getline.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetLine, Edit_GetLine macro [Windows Controls], _win32_Edit_GetLine, _win32_Edit_GetLine_cpp, controls.Edit_GetLine, controls._win32_Edit_GetLine, windowsx/Edit_GetLine
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
 - Edit_GetLine
 - windowsx/Edit_GetLine
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
 - Edit_GetLine
---

# Edit_GetLine macro

## -syntax

```cpp
int Edit_GetLine(
   HWND   hwndCtl,
   int    line,
   LPTSTR lpch,
   int    cchMax
);
```

## -returns

Type: **int**

The return value is the number of <b>TCHAR</b>s copied. The return value is zero if the line number specified by the <i>line</i> parameter is greater than the number of lines in the edit control.


## -description

Retrieves a line of text from an edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-getline">EM_GETLINE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param line

Type: <b>int</b>

The zero-based index of the line. This parameter is ignored by a single-line edit control.

### -param lpch

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a buffer that receives the string.

### -param cchMax

Type: <b>int</b>

The maximum number of characters to be copied to the buffer.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-getline">EM_GETLINE</a>
