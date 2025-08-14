---
UID: NF:commctrl.Edit_GetCaretIndex
title: Edit_GetCaretIndex macro (commctrl.h)
description: Gets the character index of the caret location for a given edit control. You can use this macro or send the EM_GETCARETINDEX message explicitly.
helpviewer_keywords: ["Edit_GetCaretIndex","Edit_GetCaretIndex macro [Windows Controls]","commctrl/Edit_GetCaretIndex","controls.edit_getcaretindex"]
old-location: controls\edit_getcaretindex.htm
tech.root: Controls
ms.assetid: 548EAC06-9127-493D-BE0E-8982DCA52895
ms.date: 07/01/2025
ms.keywords: Edit_GetCaretIndex, Edit_GetCaretIndex macro [Windows Controls], commctrl/Edit_GetCaretIndex, controls.edit_getcaretindex
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
 - Edit_GetCaretIndex
 - commctrl/Edit_GetCaretIndex
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
 - Edit_GetCaretIndex
---

# Edit_GetCaretIndex macro

## -syntax

```cpp
int Edit_GetCaretIndex(
    HWND hwndCtl
);
```

## -returns

Type: **int**

The character index.


## -description



Gets the character index of the caret location for a given edit control. You can use this macro or send the <a href="/windows/desktop/controls/em-getcaretindex">EM_GETCARETINDEX</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.
