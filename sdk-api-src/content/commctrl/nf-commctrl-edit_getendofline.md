---
UID: NF:commctrl.Edit_GetEndOfLine
title: Edit_GetEndOfLine macro (commctrl.h)
description: Gets the end of line character used for the content of the edit control. You can use this macro or send the EM_GETENDOFLINE message explicitly.
helpviewer_keywords: ["Edit_GetEndOfLine","Edit_GetEndOfLine macro [Windows Controls]","commctrl/Edit_GetEndOfLine","controls.edit_getendofline"]
old-location: controls\edit_getendofline.htm
tech.root: Controls
ms.assetid: 27B0CB7B-08BE-48FD-BF65-4F2B9C481A9C
ms.date: 07/01/2025
ms.keywords: Edit_GetEndOfLine, Edit_GetEndOfLine macro [Windows Controls], commctrl/Edit_GetEndOfLine, controls.edit_getendofline
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
 - Edit_GetEndOfLine
 - commctrl/Edit_GetEndOfLine
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
 - Edit_GetEndOfLine
---

# Edit_GetEndOfLine macro

## -syntax

```cpp
EC_ENDOFLINE Edit_GetEndOfLine(
    HWND hwndCtl
);
```

## -returns

Type: **EC_ENDOFLINE**

Returns an [EC_ENDOFLINE](/windows/win32/api/commctrl/ne-commctrl-ec_endofline) value that represents the end of line character currently in use for a given edit control.

It can be one of the following **EC_ENDOFLINE** values.

| Value | Meaning |
|-|-|
| **EC_ENDOFLINE_CRLF** | The end-of-line character used for new linebreaks is carriage return followed by linefeed (CRLF). |
| **EC_ENDOFLINE_CR** | The end-of-line character used for new linebreaks is carriage return (CR). |
| **EC_ENDOFLINE_LF** | The end-of-line character used for new linebreaks is linefeed (LF). |

## -description

Gets the end of line character used for the content of the edit control. You can use this macro or send the <a href="/windows/desktop/controls/em-getendofline">EM_GETENDOFLINE</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.
