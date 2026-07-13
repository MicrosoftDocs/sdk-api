---
UID: NF:commctrl.Pager_RecalcSize
title: Pager_RecalcSize macro (commctrl.h)
description: Forces the pager control to recalculate the size of the contained window. Using this macro will result in a PGN_CALCSIZE notification being sent. You can use this macro or send the PGM_RECALCSIZE message explicitly.
helpviewer_keywords: ["Pager_RecalcSize","Pager_RecalcSize macro [Windows Controls]","_win32_Pager_RecalcSize","_win32_Pager_RecalcSize_cpp","commctrl/Pager_RecalcSize","controls.Pager_RecalcSize","controls._win32_Pager_RecalcSize"]
old-location: controls\Pager_RecalcSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\pager\macros\pager_recalcsize.htm
ms.date: 10/21/2024
ms.keywords: Pager_RecalcSize, Pager_RecalcSize macro [Windows Controls], _win32_Pager_RecalcSize, _win32_Pager_RecalcSize_cpp, commctrl/Pager_RecalcSize, controls.Pager_RecalcSize, controls._win32_Pager_RecalcSize
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
 - Pager_RecalcSize
 - commctrl/Pager_RecalcSize
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
 - Pager_RecalcSize
---

# Pager_RecalcSize macro

## -syntax

```cpp
void Pager_RecalcSize(
   HWND hwnd
);
```


## -description

Forces the pager control to recalculate the size of the contained window. Using this macro will result in a <a href="/windows/desktop/Controls/pgn-calcsize">PGN_CALCSIZE</a> notification being sent. You can use this macro or send the <a href="/windows/desktop/Controls/pgm-recalcsize">PGM_RECALCSIZE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the pager control.
