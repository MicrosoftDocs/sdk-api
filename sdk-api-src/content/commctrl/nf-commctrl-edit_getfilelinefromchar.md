---
UID: NF:commctrl.Edit_GetFileLineFromChar
title: Edit_GetFileLineFromChar macro (commctrl.h)
description: Gets the index of the file (or logical) line of text that includes the specified character index (text wrap delimiters are ignored). You can use this macro or send the EM_FILELINEFROMCHAR message explicitly.
helpviewer_keywords: ["Edit_GetFileLineFromChar","Edit_GetFileLineFromChar macro [Windows Controls]","commctrl/Edit_GetFileLineFromChar","controls.edit_getfilelinefromchar"]
old-location: controls\edit_getfilelinefromchar.htm
tech.root: Controls
ms.assetid: 1427DEB0-2B15-4DC5-AD0B-D4F9BA12CB2C
ms.date: 07/01/2025
ms.keywords: Edit_GetFileLineFromChar, Edit_GetFileLineFromChar macro [Windows Controls], commctrl/Edit_GetFileLineFromChar, controls.edit_getfilelinefromchar
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
 - Edit_GetFileLineFromChar
 - commctrl/Edit_GetFileLineFromChar
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
 - Edit_GetFileLineFromChar
---

# Edit_GetFileLineFromChar macro

## -syntax

```cpp
UINT Edit_GetFileLineFromChar(
    HWND hwndCtl,
    UINT characterIndex
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

The logical line index.


## -description



Gets the index of the file (or logical) line of text that includes the specified character index  (text wrap delimiters are ignored). You can use this macro or send the <a href="/windows/desktop/controls/em-filelinefromchar">EM_FILELINEFROMCHAR</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.

### -param characterIndex

The 0-based character index. If characterIndex = -1, the caret location index is used.

## -remarks

The character index is the zero-based index of the character from the beginning of the edit control. 

This macro and corresponding message do not recognize text wrapping (visible lines) and, instead, recognize file (logical) lines with an end-of-line delimiter. When text wrap is turned off, visible lines are equivalent to file lines.

The <a href="/windows/desktop/Controls/em-linefromchar">EM_LINEFROMCHAR</a>, <a href="/windows/desktop/controls/em-lineindex">EM_LINEINDEX</a>, <a href="/windows/desktop/Controls/em-linelength">EM_LINELENGTH</a>, <a href="/windows/desktop/Controls/em-getline">EM_GETLINE</a>, and <a href="/windows/desktop/Controls/em-getlinecount">EM_GETLINECOUNT</a> messages recognize visible line text wrapping and provide information for the line of text up to the wrapping line break. (Each subsequent line is delimited by the next text wrap break.)
