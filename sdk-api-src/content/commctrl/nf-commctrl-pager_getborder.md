---
UID: NF:commctrl.Pager_GetBorder
title: Pager_GetBorder macro (commctrl.h)
description: Retrieves the current border size for the pager control. You can use this macro or send the PGM_GETBORDER message explicitly.
helpviewer_keywords: ["Pager_GetBorder","Pager_GetBorder macro [Windows Controls]","_win32_Pager_GetBorder","_win32_Pager_GetBorder_cpp","commctrl/Pager_GetBorder","controls.Pager_GetBorder","controls._win32_Pager_GetBorder"]
old-location: controls\Pager_GetBorder.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getborder.htm
ms.date: 10/21/2024
ms.keywords: Pager_GetBorder, Pager_GetBorder macro [Windows Controls], _win32_Pager_GetBorder, _win32_Pager_GetBorder_cpp, commctrl/Pager_GetBorder, controls.Pager_GetBorder, controls._win32_Pager_GetBorder
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
 - Pager_GetBorder
 - commctrl/Pager_GetBorder
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
 - Pager_GetBorder
---

# Pager_GetBorder macro

## -syntax

```cpp
int Pager_GetBorder(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns an <b>int</b> value that contains the current border size, in pixels.


## -description

Retrieves the current border size for the pager control. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-getborder">PGM_GETBORDER</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.
