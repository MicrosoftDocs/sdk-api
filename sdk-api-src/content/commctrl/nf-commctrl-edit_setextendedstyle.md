---
UID: NF:commctrl.Edit_SetExtendedStyle
title: Edit_SetExtendedStyle macro (commctrl.h)
description: Sets extended styles for edit controls using the style mask. You can use this macro or send the EM_SETEXTENDEDSTYLE message explicitly.
helpviewer_keywords: ["Edit_SetExtendedStyle","Edit_SetExtendedStyle macro [Windows Controls]","commctrl/Edit_SetExtendedStyle","controls.edit_setextendedstyle"]
old-location: controls\edit_setextendedstyle.htm
tech.root: Controls
ms.assetid: 4ECAA174-A9C5-4A01-9341-CF6C8777E0F5
ms.date: 07/01/2025
ms.keywords: Edit_SetExtendedStyle, Edit_SetExtendedStyle macro [Windows Controls], commctrl/Edit_SetExtendedStyle, controls.edit_setextendedstyle
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
 - Edit_SetExtendedStyle
 - commctrl/Edit_SetExtendedStyle
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
 - Edit_SetExtendedStyle
---

# Edit_SetExtendedStyle macro

## -syntax

```cpp
void Edit_SetExtendedStyle(
    HWND hwndCtl,
    DWORD dw,
    DWORD dwMask
);
```


## -description



Sets extended styles for edit controls using the style mask. You can use this macro or send the <a href="/windows/desktop/controls/em-setextendedstyle">EM_SETEXTENDEDSTYLE</a> message explicitly.

## -parameters

### -param hwndCtl

A handle to the edit control.

### -param dw

A <a href="/windows/desktop/WinProg/windows-data-types">DWORD</a> value that specifies the extended edit control styles to set.

### -param dwMask

A <a href="/windows/desktop/WinProg/windows-data-types">DWORD</a> value that specifies which styles are to be affected.
