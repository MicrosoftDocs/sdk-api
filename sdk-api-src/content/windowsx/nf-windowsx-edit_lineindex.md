---
UID: NF:windowsx.Edit_LineIndex
title: Edit_LineIndex macro (windowsx.h)
description: Gets the character index of the first character of a specified line in a multiline edit or rich edit control. You can use this macro or send the EM_LINEINDEX message explicitly.
helpviewer_keywords: ["Edit_LineIndex","Edit_LineIndex macro [Windows Controls]","_win32_Edit_LineIndex","_win32_Edit_LineIndex_cpp","controls.Edit_LineIndex","controls._win32_Edit_LineIndex","windowsx/Edit_LineIndex"]
old-location: controls\Edit_LineIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_lineindex.htm
ms.date: 10/21/2024
ms.keywords: Edit_LineIndex, Edit_LineIndex macro [Windows Controls], _win32_Edit_LineIndex, _win32_Edit_LineIndex_cpp, controls.Edit_LineIndex, controls._win32_Edit_LineIndex, windowsx/Edit_LineIndex
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
 - Edit_LineIndex
 - windowsx/Edit_LineIndex
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
 - Edit_LineIndex
---

# Edit_LineIndex macro

## -syntax

```cpp
int Edit_LineIndex(
   HWND hwndCtl,
   int  line
);
```

## -returns

Type: **int**

The character index of the first character in the line, or &#8211;1 if the specified line number is greater than the number of lines in the edit control.


## -description

Gets the character index of the first character of a specified line in a multiline edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/controls/em-lineindex">EM_LINEINDEX</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param line

Type: <b>int</b>

The zero-based line number. A value of –1 specifies the current line number (the line that contains the caret).
