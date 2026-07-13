---
UID: NF:commctrl.Edit_GetExtendedStyle
title: Edit_GetExtendedStyle macro (commctrl.h)
description: Gets the extended styles that are currently in use for a given edit control. You can use this macro or send the EM_GETEXTENDEDSTYLE message explicitly.
helpviewer_keywords: ["Edit_GetExtendedStyle","Edit_GetExtendedStyle macro [Windows Controls]","commctrl/Edit_GetExtendedStyle","controls.edit_getextendedstyle"]
old-location: controls\edit_getextendedstyle.htm
tech.root: Controls
ms.assetid: 6E29C7FE-A0D4-4A4D-B10A-2E2B2211D6C3
ms.date: 07/01/2025
ms.keywords: Edit_GetExtendedStyle, Edit_GetExtendedStyle macro [Windows Controls], commctrl/Edit_GetExtendedStyle, controls.edit_getextendedstyle
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
 - Edit_GetExtendedStyle
 - commctrl/Edit_GetExtendedStyle
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
 - Edit_GetExtendedStyle
---

# Edit_GetExtendedStyle macro

## -syntax

```cpp
DWORD Edit_GetExtendedStyle(
    HWND hwndCtl
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a **DWORD** value that represents the styles currently in use for a given edit control.


## -description



Gets the extended styles that are currently in use for a given edit control. You can use this macro or send the <a href="/windows/desktop/controls/em-getextendedstyle">EM_GETEXTENDEDSTYLE</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to a list-view control.
