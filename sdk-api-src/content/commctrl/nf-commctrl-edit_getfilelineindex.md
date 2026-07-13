---
UID: NF:commctrl.Edit_GetFileLineIndex
title: Edit_GetFileLineIndex macro (commctrl.h)
description: Gets the index of the file (or logical) line of text based on the specified visible line. You can use this macro or send the EM_FILELINEINDEX message explicitly.
helpviewer_keywords: ["Edit_GetFileLineIndex","Edit_GetFileLineIndex macro [Windows Controls]","commctrl/Edit_GetFileLineIndex","controls.edit_getfilelineindex"]
old-location: controls\edit_getfilelineindex.htm
tech.root: Controls
ms.assetid: FC119B71-BC5C-437E-9DBE-DD907F459D45
ms.date: 07/01/2025
ms.keywords: Edit_GetFileLineIndex, Edit_GetFileLineIndex macro [Windows Controls], commctrl/Edit_GetFileLineIndex, controls.edit_getfilelineindex
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
 - Edit_GetFileLineIndex
 - commctrl/Edit_GetFileLineIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - Edit_GetFileLineIndex
---

# Edit_GetFileLineIndex macro

## -syntax

```cpp
UINT Edit_GetFileLineIndex(
    HWND hwndCtl,
    UINT lineNumber
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The logical line index.


## -description



Gets the index of the file (or logical) line of text based on the specified visible line. You can use this macro or send the <a href="/windows/desktop/controls/em-filelineindex">EM_FILELINEINDEX</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.

### -param lineNumber

The file line number, where the number of the first line is 0. If lineNumber = -1, the file line with the caret is used.

## -remarks

The logical line index is a zero-based index from the beginning of the edit control. 

This macro and corresponding message do not recognize text wrapping (visible lines) and, instead, recognize file (logical) lines with an end-of-line delimiter. When text wrap is turned off, visible lines are equivalent to file lines.

The <a href="/windows/desktop/Controls/em-linefromchar">EM_LINEFROMCHAR</a>, <a href="/windows/desktop/controls/em-lineindex">EM_LINEINDEX</a>, <a href="/windows/desktop/Controls/em-linelength">EM_LINELENGTH</a>, <a href="/windows/desktop/Controls/em-getline">EM_GETLINE</a>, and <a href="/windows/desktop/Controls/em-getlinecount">EM_GETLINECOUNT</a> messages recognize visible line text wrapping and provide information for the line of text up to the wrapping line break. (Each subsequent line is delimited by the next text wrap break.)
