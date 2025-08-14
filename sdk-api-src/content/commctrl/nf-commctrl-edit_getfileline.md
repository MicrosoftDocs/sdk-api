---
UID: NF:commctrl.Edit_GetFileLine
title: Edit_GetFileLine macro (commctrl.h)
description: Gets the text of the specified file (or logical) line (text wrap delimiters are ignored). You can use this macro or send the EM_GETFILELINE message explicitly.
helpviewer_keywords: ["Edit_GetFileLine","Edit_GetFileLine macro [Windows Controls]","commctrl/Edit_GetFileLine","controls.edit_getfileline"]
old-location: controls\edit_getfileline.htm
tech.root: Controls
ms.assetid: F59ECED6-5584-43A9-A5F8-5502D66A29B6
ms.date: 07/01/2025
ms.keywords: Edit_GetFileLine, Edit_GetFileLine macro [Windows Controls], commctrl/Edit_GetFileLine, controls.edit_getfileline
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
 - Edit_GetFileLine
 - commctrl/Edit_GetFileLine
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
 - Edit_GetFileLine
---

# Edit_GetFileLine macro

## -syntax

```cpp
void Edit_GetFileLine(
    HWND hwndCtl,
    UINT lineNumber,
    LPSTR textBuffer
);
```


## -description



Gets the text of the specified file (or logical) line (text wrap delimiters are ignored). You can use this macro or send the <a href="/windows/desktop/controls/em-getfileline">EM_GETFILELINE</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.

### -param lineNumber

The logical line number.

### -param textBuffer

The buffer that receives the text.

## -remarks

This macro and corresponding message do not recognize text wrapping (visible lines) and, instead, recognize file (logical) lines with an end-of-line delimiter. When text wrap is turned off, visible lines are equivalent to file lines.

The <a href="/windows/desktop/Controls/em-linefromchar">EM_LINEFROMCHAR</a>, <a href="/windows/desktop/controls/em-lineindex">EM_LINEINDEX</a>, <a href="/windows/desktop/Controls/em-linelength">EM_LINELENGTH</a>, <a href="/windows/desktop/Controls/em-getline">EM_GETLINE</a>, and <a href="/windows/desktop/Controls/em-getlinecount">EM_GETLINECOUNT</a> messages recognize visible line text wrapping and provide information for the line of text up to the wrapping line break. (Each subsequent line is delimited by the next text wrap break.)
