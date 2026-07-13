---
UID: NF:commctrl.Pager_GetPos
title: Pager_GetPos macro (commctrl.h)
description: Retrieves the current scroll position of the pager control. You can use this macro or send the PGM_GETPOS message explicitly.
helpviewer_keywords: ["Pager_GetPos","Pager_GetPos macro [Windows Controls]","_win32_Pager_GetPos","_win32_Pager_GetPos_cpp","commctrl/Pager_GetPos","controls.Pager_GetPos","controls._win32_Pager_GetPos"]
old-location: controls\Pager_GetPos.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_getpos.htm
ms.date: 10/21/2024
ms.keywords: Pager_GetPos, Pager_GetPos macro [Windows Controls], _win32_Pager_GetPos, _win32_Pager_GetPos_cpp, commctrl/Pager_GetPos, controls.Pager_GetPos, controls._win32_Pager_GetPos
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
 - Pager_GetPos
 - commctrl/Pager_GetPos
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
 - Pager_GetPos
---

# Pager_GetPos macro

## -syntax

```cpp
int Pager_GetPos(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns an <b>int</b> value that contains the current scroll position, in pixels.


## -description

Retrieves the current scroll position of the pager control. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-getpos">PGM_GETPOS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.
