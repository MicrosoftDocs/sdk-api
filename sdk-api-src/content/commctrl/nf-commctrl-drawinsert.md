---
UID: NF:commctrl.DrawInsert
title: DrawInsert function (commctrl.h)
description: Draws the insert icon in the parent window of the specified drag list box.
helpviewer_keywords: ["DrawInsert","DrawInsert function [Windows Controls]","_win32_DrawInsert","_win32_DrawInsert_cpp","commctrl/DrawInsert","controls.DrawInsert","controls._win32_DrawInsert"]
old-location: controls\DrawInsert.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\draglb\functions\drawinsert.htm
ms.date: 12/05/2018
ms.keywords: DrawInsert, DrawInsert function [Windows Controls], _win32_DrawInsert, _win32_DrawInsert_cpp, commctrl/DrawInsert, controls.DrawInsert, controls._win32_DrawInsert
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DrawInsert
 - commctrl/DrawInsert
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - DrawInsert
---

# DrawInsert function


## -description

Draws the insert icon in the parent window of the specified drag list box.

## -parameters

### -param handParent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the parent window of the drag list box.

### -param hLB

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the drag list box.

### -param nItem

Type: <b>int</b>

The identifier of the icon item to be drawn.