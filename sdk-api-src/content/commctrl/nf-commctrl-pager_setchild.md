---
UID: NF:commctrl.Pager_SetChild
title: Pager_SetChild macro (commctrl.h)
description: Sets the contained window for the pager control.
helpviewer_keywords: ["Pager_SetChild","Pager_SetChild macro [Windows Controls]","_win32_Pager_SetChild","_win32_Pager_SetChild_cpp","commctrl/Pager_SetChild","controls.Pager_SetChild","controls._win32_Pager_SetChild"]
old-location: controls\Pager_SetChild.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_setchild.htm
ms.date: 10/21/2024
ms.keywords: Pager_SetChild, Pager_SetChild macro [Windows Controls], _win32_Pager_SetChild, _win32_Pager_SetChild_cpp, commctrl/Pager_SetChild, controls.Pager_SetChild, controls._win32_Pager_SetChild
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Pager_SetChild
 - commctrl/Pager_SetChild
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
 - Pager_SetChild
---

# Pager_SetChild macro

## -syntax

```cpp
void Pager_SetChild(
   HWND hwnd,
   HWND hwndChild
);
```


## -description

Sets the contained window for the pager control. This macro will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling. In most cases, the contained window will be a child window. If this is the case, the contained window should be a child of the pager control. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-setchild">PGM_SETCHILD</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.

### -param hwndChild

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the window to be contained.
