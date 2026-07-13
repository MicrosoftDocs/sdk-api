---
UID: NF:commctrl.Edit_GetHilite
title: Edit_GetHilite macro (commctrl.h)
description: This macro is not implemented. (Edit_GetHilite)
helpviewer_keywords: ["Edit_GetHilite","Edit_GetHilite macro [Windows Controls]","_shell_Edit_GetHilite","_shell_Edit_GetHilite_cpp","commctrl/Edit_GetHilite","controls.Edit_GetHilite","controls._shell_Edit_GetHilite"]
old-location: controls\Edit_GetHilite.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_gethilite.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetHilite, Edit_GetHilite macro [Windows Controls], _shell_Edit_GetHilite, _shell_Edit_GetHilite_cpp, commctrl/Edit_GetHilite, controls.Edit_GetHilite, controls._shell_Edit_GetHilite
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - Edit_GetHilite
 - commctrl/Edit_GetHilite
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
 - Edit_GetHilite
---

# Edit_GetHilite macro

## -syntax

```cpp
DWORD Edit_GetHilite(
   HWND hwndCtl
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

The starting and ending indexes that are highlighted. This value was created with the <b>MAKELONG</b> macro, with the starting index as the low word and the ending index as the high word. So, to get the starting index, call the <b>LOWORD</b> macro with the return value and to get the ending index, call the <b>HIWORD</b> macro with the return value.


## -description

This macro is not implemented.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the edit control.
