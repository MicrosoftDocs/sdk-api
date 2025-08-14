---
UID: NF:commctrl.Edit_SetEndOfLine
title: Edit_SetEndOfLine macro (commctrl.h)
description: Sets the end of line character used for the content of the edit control. You can use this macro or send the EM_SETENDOFLINE message explicitly.
helpviewer_keywords: ["Edit_SetEndOfLine","Edit_SetEndOfLine macro [Windows Controls]","commctrl/Edit_SetEndOfLine","controls.edit_setendofline"]
old-location: controls\edit_setendofline.htm
tech.root: Controls
ms.assetid: D143B914-5F68-4957-9D1F-C55977E27C8B
ms.date: 07/01/2025
ms.keywords: Edit_SetEndOfLine, Edit_SetEndOfLine macro [Windows Controls], commctrl/Edit_SetEndOfLine, controls.edit_setendofline
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
 - Edit_SetEndOfLine
 - commctrl/Edit_SetEndOfLine
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
 - Edit_SetEndOfLine
---

# Edit_SetEndOfLine macro

## -syntax

```cpp
void Edit_SetEndOfLine(
    HWND hwndCtl,
    EC_ENDOFLINE eolType
);
```


## -description



Sets the end of line character used for the content of the edit control. You can use this macro or send the <a href="/windows/desktop/controls/em-setendofline">EM_SETENDOFLINE</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.

### -param eolType

The end of line character to use.
