---
UID: NF:commctrl.Edit_GetFileLineLength
title: Edit_GetFileLineLength macro (commctrl.h)
description: Gets the length of the file (or logical) line of text from the specified character index (text wrap delimiters are ignored). You can use this macro or send the EM_FILELINELENGTH message explicitly.
helpviewer_keywords: ["Edit_GetFileLineLength","Edit_GetFileLineLength macro [Windows Controls]","commctrl/Edit_GetFileLineLength","controls.edit_getfilelinelength"]
old-location: controls\edit_getfilelinelength.htm
tech.root: Controls
ms.assetid: 04315431-FC5C-41FB-9806-7904F71C19FD
ms.date: 07/01/2025
ms.keywords: Edit_GetFileLineLength, Edit_GetFileLineLength macro [Windows Controls], commctrl/Edit_GetFileLineLength, controls.edit_getfilelinelength
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
 - Edit_GetFileLineLength
 - commctrl/Edit_GetFileLineLength
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
 - Edit_GetFileLineLength
---

# Edit_GetFileLineLength macro

## -syntax

```cpp
UINT Edit_GetFileLineLength(
    HWND hwndCtl,
    UINT characterIndex
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The logical line length, from the specified character index.


## -description



Gets the length of the file (or logical) line of text from the specified character index  (text wrap delimiters are ignored). You can use this macro or send the <a href="/windows/desktop/controls/em-filelinelength">EM_FILELINELENGTH</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.

### -param characterIndex

The character index. If characterIndex = -1, the caret location index is used, not including the length of any selected text.

## -remarks

The character index is the zero-based index of the character from the beginning of the edit control. 

This macro and corresponding message do not recognize text wrapping (visible lines) and, instead, recognize file (logical) lines with an end-of-line delimiter. When text wrap is turned off, visible lines are equivalent to file lines.

The <a href="/windows/desktop/Controls/em-linefromchar">EM_LINEFROMCHAR</a>, <a href="/windows/desktop/controls/em-lineindex">EM_LINEINDEX</a>, <a href="/windows/desktop/Controls/em-linelength">EM_LINELENGTH</a>, <a href="/windows/desktop/Controls/em-getline">EM_GETLINE</a>, and <a href="/windows/desktop/Controls/em-getlinecount">EM_GETLINECOUNT</a> messages recognize visible line text wrapping and provide information for the line of text up to the wrapping line break. (Each subsequent line is delimited by the next text wrap break.)
